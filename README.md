<div align="center">

<img src="./public/favicon.svg" alt="Lasmium Pulse logo" width="84" height="84" />

# LASMIUM *Pulse* `04`

**Modern Twitch viewer • Multi-view up to 9 screens • Ad-free HLS proxy • Hybrid chat • Twitch account**

[![Latest release](https://img.shields.io/github/v/release/lasme-ephrem/lasmium-pulse-releases?style=flat-square&label=Latest&color=1EC988)](https://github.com/lasme-ephrem/lasmium-pulse-releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/lasme-ephrem/lasmium-pulse-releases/total?style=flat-square&color=141413)](https://github.com/lasme-ephrem/lasmium-pulse-releases/releases)
[![Windows · macOS · Linux](https://img.shields.io/badge/Windows%20%C2%B7%20macOS%20%C2%B7%20Linux-141413?style=flat-square)](#download)
[![License: AGPL-3.0](https://img.shields.io/badge/License-AGPL--3.0-F4F1EA?style=flat-square&labelColor=141413&color=FF3E1D)](LICENSE)

<p align="center">
  <em>All your Twitch lives without ad breaks, up to 9 screens at once, in an editorial interface inspired by industrial design (light, dark and OLED themes).</em>
</p>

<p align="center"><a href="README.fr.md">🇫🇷 Version française</a></p>

</div>

---

This repository hosts the **official desktop builds** of Lasmium Pulse (Windows, macOS, Linux), the feed the app updates itself from, the changelog and the documentation. It is also the place to [report a bug or suggest a feature](https://github.com/lasme-ephrem/lasmium-pulse-releases/issues/new/choose). The source code is developed in a separate repository.

Lasmium Pulse runs on your own machine. It is **not affiliated with Twitch**. Filtering ads goes against Twitch's terms of service: use it at your own risk, and subscribe to the streamers you want to support.

## <img src="docs/icons/rocket.svg" width="24" height="24" alt="" align="absmiddle"> Download

**[Get the latest release →](https://github.com/lasme-ephrem/lasmium-pulse-releases/releases/latest)**

| System | File to download | Notes |
| :--- | :--- | :--- |
| **Windows** 10 / 11 (64-bit) | `Lasmium-Pulse-x.y.z-win-x64.exe` | Installer; you choose the folder. Desktop and Start menu shortcuts are created. |
| **macOS** Apple Silicon (M1 and later) | `Lasmium-Pulse-x.y.z-mac-arm64.dmg` | Open the DMG and drag the app to *Applications*. |
| **macOS** Intel | `Lasmium-Pulse-x.y.z-mac-x64.dmg` | Same as above. |
| **Ubuntu / Debian** and derivatives | `Lasmium-Pulse-x.y.z-linux-amd64.deb` | `sudo apt install ./Lasmium-Pulse-x.y.z-linux-amd64.deb`: installs the menu entry and the dock icon. |
| **Other Linux** (64-bit) | `Lasmium-Pulse-x.y.z-linux-x86_64.AppImage` | `chmod +x` then run. Integrate it with [Gear Lever](https://github.com/mijorus/gearlever) or AppImageLauncher to get the menu entry and icon; run as is, it shows a generic icon. |

The other files of a release (`.zip`, `.blockmap`, `latest*.yml`) are used by the automatic updater: you do not need them.

Everything is embedded: no terminal and no Node.js to install. The app keeps the Twitch session in the system keychain and shows an icon in the notification area to reopen the window or quit.

### First launch

Builds are not code-signed yet, so each system shows a warning the first time:

- **Windows** SmartScreen: *More info* → *Run anyway*.
- **macOS** Gatekeeper: right click (or Control-click) the app → *Open*, once.
- **Linux**: nothing to do.

Signing in with Twitch needs no configuration: click **Sign in with Twitch** in the sidebar, then enter the code shown on `twitch.tv/activate`. Each person signs in with their own account; the app uses Twitch's official Device Code Flow and never sees your password.

### Updates

The app checks for a new version at launch and every 24 hours (Windows: *Help* → *Check for updates…* as well). When one is downloaded an **Update ready** toast offers to **Restart**; otherwise it installs on the next launch. Only the latest version is maintained.

## <img src="docs/icons/package.svg" width="24" height="24" alt="" align="absmiddle"> Docker (self-hosting)

To reach Lasmium Pulse from several devices (phone included) on your network or your own server, use [compose.yml](compose.yml) with the image published on GHCR for every version:

```bash
PULSE_SECRET='a-long-random-string' PULSE_PASSWORD='choose-a-password' docker compose up -d
# → http://<machine>:3001
```

| Variable | Role |
| :--- | :--- |
| `PULSE_SECRET` | Key (16+ characters) that encrypts the Twitch session on the volume. Required. |
| `PULSE_PASSWORD` | Password (8+ characters) asked by the browser before any access. A must as soon as another machine can reach the server. |
| `TWITCH_APP_CLIENT_ID` | Optional: the Client ID of your own "Public" Twitch application instead of the one shipped with the app. |
| `PULSE_ALLOWED_HOSTS` | Optional: extra host names the app may be reached by (e.g. `pulse.local`). |

Image: `ghcr.io/lasme-ephrem/lasmium-pulse:<version>` (`latest` follows the newest release). The browser then offers **Install Lasmium Pulse** as a web app, which opens in its own window.

## <img src="docs/icons/sparkles.svg" width="24" height="24" alt="" align="absmiddle"> What you get

- **PulseShield™ ad-free playback**: a local proxy strips the ad segments from the live stream in real time.
- **Multi-view up to 9 screens** with 5 layouts (Grid, Spotlight, Theater, Columns, Studio), drag and drop, quality cap on secondary screens, **audio solo** in one click.
- **Rewind inside the live**, per-screen offsets with an **Align** button, local clips of the last seconds, screenshots, always-on-top floating window.
- **Hybrid chat**: fast mode with Twitch + 7TV / BTTV / FFZ emotes, a **Mix** tab merging every chat, filters, mention alerts, viewer cards and moderation tools, messages sent with your account; or the official Twitch chat in one click.
- **Twitch account**: followed channels that are live, recommendations, **live notifications**, raids, real-time title and category changes, Twitch clips.
- **Past broadcasts (VOD)** with chapters and the chat replay synchronized with the video; categories and most viewed clips inside the app.
- **Saved multi-views**, session history, shareable links, command palette (`Ctrl+K`), customizable keyboard shortcuts.
- **English / French** interface, light, dark and OLED black themes, 8 accent colours.

The complete [user guide](docs/GUIDE_UTILISATEUR.md) (French) covers every feature.

## <img src="docs/icons/lock.svg" width="24" height="24" alt="" align="absmiddle"> Privacy & security

Your Twitch session never leaves your machine (or your server): it is encrypted on disk, and the local server only answers your own browser (loopback only, `Host` / `Origin` checks, per-launch session token). Error reports are **off by default** and never contain identifiers, tokens or channel names. Details and the vulnerability reporting process: [SECURITY.md](SECURITY.md).

## <img src="docs/icons/book-open.svg" width="24" height="24" alt="" align="absmiddle"> Help & feedback

- <img src="docs/icons/book-open.svg" width="18" height="18" alt="" align="absmiddle"> **[User guide](docs/GUIDE_UTILISATEUR.md)** (French) · **[Technical notes](docs/ARCHITECTURE.md)** (French)
- <img src="docs/icons/history.svg" width="18" height="18" alt="" align="absmiddle"> **[Changelog](CHANGELOG.md)**: what changed in each version
- <img src="docs/icons/flag.svg" width="18" height="18" alt="" align="absmiddle"> **[Report a bug / request a feature](https://github.com/lasme-ephrem/lasmium-pulse-releases/issues/new/choose)**
- <img src="docs/icons/scale.svg" width="18" height="18" alt="" align="absmiddle"> **[AGPL-3.0 licence](LICENSE)**

Built with Electron, React, HLS.js and Node.js.
