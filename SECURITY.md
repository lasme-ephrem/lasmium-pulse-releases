# Security

## Reporting a vulnerability

Use GitHub's private reporting (**Security** tab → **Report a vulnerability**) rather than a public issue. Describe the scenario, the affected version and, if possible, a reproduction. You will get an answer within a few days; the fix is published in a patch release and mentioned in the changelog.

Only the latest published version is maintained.

## Threat model

Lasmium Pulse is a personal server: it runs on the viewer's machine (or their own server) and holds their Twitch session. The protections target three risks:

- **Another website** trying to use the local server from the browser: `Host` header check (DNS rebinding), refusal of cross-site state-changing requests (`Origin` / `Sec-Fetch-Site`), and a per-launch session token (`X-Pulse-Token`) required on every write. No CORS.
- **Another machine**: the server listens on `127.0.0.1` by default; `PULSE_ALLOW_LAN=1` opens it and `PULSE_PASSWORD` adds HTTP authentication (the server warns when one goes without the other).
- **The disk**: the Twitch session is encrypted (AES-256-GCM with `PULSE_SECRET`, or the system keychain in the desktop app).

The proxy only relays known Twitch hosts (playlists, past-broadcast segments, emotes of the three providers); every URL supplied by the client is checked against this allow-list. Chat content is rendered without HTML, links only open over `http(s)`, and a strict Content-Security-Policy ships with the built client.

## What the app never does without you

Sending a message, creating a clip, blocking or moderating someone only happens after an explicit click, then a confirmation for moderation. Error reports (Sentry) are off by default and contain neither identifiers nor tokens.
