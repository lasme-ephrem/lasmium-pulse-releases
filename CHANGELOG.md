# Changelog

## [1.2.1](https://github.com/lasme-ephrem/lasmium-pulse/compare/v1.2.0...v1.2.1) (2026-10-28)


### Bug Fixes

* **desktop:** keep title bar menus clickable and above the header ([a9bc7eb](https://github.com/lasme-ephrem/lasmium-pulse/commit/a9bc7eb5ad5223ab609841d92591927a0255fb3b))

## [1.2.0](https://github.com/lasme-ephrem/lasmium-pulse/compare/v1.1.0...v1.2.0) (2026-10-28)


### Features

* **desktop:** centre the title in the Windows title bar ([a41a92f](https://github.com/lasme-ephrem/lasmium-pulse/commit/a41a92f390b021402d143b8b85d149e6c7e65bc8))
* **desktop:** themed title bar on Windows ([35e543a](https://github.com/lasme-ephrem/lasmium-pulse/commit/35e543a09a42c47c48fcb6b02ce6817d904fedb8))
* **desktop:** View and Help menus in the Windows title bar, Linux desktop name ([d03da67](https://github.com/lasme-ephrem/lasmium-pulse/commit/d03da673b284daaddfa058b4314c2f76f7d1b306))


### Bug Fixes

* **desktop:** keep the embedded server on a stable port so settings survive a relaunch ([7f6c562](https://github.com/lasme-ephrem/lasmium-pulse/commit/7f6c562436c4b51ab168a3365b69160bee2bdc42))
* **desktop:** Linux dock icon and desktop entry ([6f0b804](https://github.com/lasme-ephrem/lasmium-pulse/commit/6f0b804a08809f6c76b19208455daa236dbcfbcc))

## [1.1.0](https://github.com/lasme-ephrem/lasmium-pulse/compare/v1.0.0...v1.1.0) (2026-10-28)


### Features

* **app:** client-side error reports switch and desktop bridge ([f07298f](https://github.com/lasme-ephrem/lasmium-pulse/commit/f07298fa0b13e7e26b22dccdb065aa71397b5a93))
* **app:** real-time updates, presets, session history, command palette, per-channel notifications and schedule ([e02a2bd](https://github.com/lasme-ephrem/lasmium-pulse/commit/e02a2bdd4d3037bea05f4e5a2233de2cebb43f75))
* **auth:** ship the public Twitch Client ID so sign-in needs no configuration ([436c62a](https://github.com/lasme-ephrem/lasmium-pulse/commit/436c62a2e21d483be6fc8b7804d615645f069a6c))
* build PulseTV modern Twitch viewer with 4x multi-view, hybrid chat, and HLS ad-blocker ([cf7bd7a](https://github.com/lasme-ephrem/lasmium-pulse/commit/cf7bd7a2d7eaefcedee1608b061c9eb68203eef5))
* **chat:** [@mention](https://github.com/mention) autocompletion and replies to a viewer's message in the fast chat ([42d7f82](https://github.com/lasme-ephrem/lasmium-pulse/commit/42d7f82ae38f263d0bd6d69585217aa749b1a586))
* **chat:** filters, safe links, mention detection, IRC and emote hooks, chat settings ([cdcc936](https://github.com/lasme-ephrem/lasmium-pulse/commit/cdcc936f718f54bcb438357b9c318263f099895a))
* **chat:** highlight only the signed-in viewer's own messages ([8bcaefd](https://github.com/lasme-ephrem/lasmium-pulse/commit/8bcaefdb32ea199cdc7dbc3664e1bc86e2019201))
* **chat:** parse subscriptions, raids, announcements, deletions and timeouts from IRC ([292dc70](https://github.com/lasme-ephrem/lasmium-pulse/commit/292dc70c1332e96507b9b5819761550f947be7c0))
* **chat:** virtualized list, events, emote picker, user card, viewers, detached window ([b0f40b6](https://github.com/lasme-ephrem/lasmium-pulse/commit/b0f40b66d418f352d5c422d0432d21577119db87))
* create Twitch clips from a tile (button or X key) ([a229ac5](https://github.com/lasme-ephrem/lasmium-pulse/commit/a229ac5adec93d1e2a84b0c24d81a55abbfda676))
* **desktop:** Electron shell with embedded server, OS keychain, auto-updates and installers ([2c80faa](https://github.com/lasme-ephrem/lasmium-pulse/commit/2c80faa92f7b6b84545bd64cc1ca976f503fb75b))
* **discovery:** category browser, clips browser, resume section and bigger directory pages ([ab28a7e](https://github.com/lasme-ephrem/lasmium-pulse/commit/ab28a7e68354a641ef8b7fc62bed12d93dff0764))
* followed channels, recommendations, stream-end handling and quality tooling ([44335ec](https://github.com/lasme-ephrem/lasmium-pulse/commit/44335ec7845a85b57bc47423935a7c235cad139a))
* **i18n:** choose the stream language of Top and recommendations independently of the interface ([04eda04](https://github.com/lasme-ephrem/lasmium-pulse/commit/04eda04f7d537066d2bd32947b0cb04651f27dde))
* **i18n:** French/English interface with automatic language detection ([75588c6](https://github.com/lasme-ephrem/lasmium-pulse/commit/75588c604938befce33eee1cb33e3ec31cc675be))
* **player:** quality cap per screen, audio only, stats, screenshot, rewind and per-screen offsets, local clips, floating window, drag-and-drop, up to 9 screens ([b55fcaa](https://github.com/lasme-ephrem/lasmium-pulse/commit/b55fcaaa22315e64c254af4f77ad6d273ce565bc))
* **pwa:** installable web app and chat drawer on small screens ([a6c56d3](https://github.com/lasme-ephrem/lasmium-pulse/commit/a6c56d3d2a5dc4ec54c9f254b9a6e323e5774b38))
* **server:** categories, clips, schedule, VOD chapters and chat replay, VOD segment relay ([a1dc625](https://github.com/lasme-ephrem/lasmium-pulse/commit/a1dc6255a58e345e7a140aef167b3884dbe0635b))
* **server:** chat routes for Twitch emotes, chatters, moderation, block list and history ([fda8a55](https://github.com/lasme-ephrem/lasmium-pulse/commit/fda8a5575340504e856f3db74f07cd5ff330cce6))
* **server:** optional HTTP password and opt-in anonymous error reports ([52679b4](https://github.com/lasme-ephrem/lasmium-pulse/commit/52679b47de566c6789f4118c62ee3cc9b8b5c5b7))
* **server:** Twitch EventSub relay (WebSocket) with SSE to the client ([e2e060a](https://github.com/lasme-ephrem/lasmium-pulse/commit/e2e060a49de1da7d327dcf301aa81d5a998f6f8d))
* **ui:** pulsing live badge on the favicon, no emoji in the tab title ([31cab6f](https://github.com/lasme-ephrem/lasmium-pulse/commit/31cab6fc776893ffb53a60aefe67f3242b9f72a0))
* **ui:** redesign with Gemini API (Nano Banana 2.1 logo + Swiss broadcast industrial Light & Dark theme) ([8c84d41](https://github.com/lasme-ephrem/lasmium-pulse/commit/8c84d4177d207e0d83dea21e39c91c8d362b3b57))
* **ui:** unified settings, system/OLED themes and accents, undo close, custom shortcuts, welcome tour, transitions, live tab title, accessibility ([74c5bb7](https://github.com/lasme-ephrem/lasmium-pulse/commit/74c5bb7c92c8e51c643dd22823c8ad741a00ed34))
* **vod:** playback speed, chapters, position bar and synchronized chat replay ([a4d03f4](https://github.com/lasme-ephrem/lasmium-pulse/commit/a4d03f469d6eb66aa660e51f2cc6edb02ea577b5))


### Bug Fixes

* **brand:** add full-bleed SVG favicon, dark-framed logo icon, and Lasmium Pulse branding ([402ddbd](https://github.com/lasme-ephrem/lasmium-pulse/commit/402ddbda66960c35b17732a3f35b119a1f4804f8))
* **clips:** wait until Twitch has finished the clip before linking to it ([b3d4d8f](https://github.com/lasme-ephrem/lasmium-pulse/commit/b3d4d8fc4bd13d2eac8132b5c8ede999db724a9b))
* **header:** control bank no longer overlaps the search bar ([bb1f0fc](https://github.com/lasme-ephrem/lasmium-pulse/commit/bb1f0fc46369aa8bd9b82867f1debaba64925fc5))
* **i18n:** home page copy says up to 9 screens ([63230b4](https://github.com/lasme-ephrem/lasmium-pulse/commit/63230b4f8a772b030158b0197d8358dc9ab848df))
* **player:** no reload on layout change or reorder, fMP4 clips start at zero ([9242b4b](https://github.com/lasme-ephrem/lasmium-pulse/commit/9242b4be34f69803360586fa5457f2fa7d1c5a76))
* the sound and the chat follow the stream set as main monitor (Focus) ([aaccd42](https://github.com/lasme-ephrem/lasmium-pulse/commit/aaccd42bc58adbf8ec29fd6c133dfb5e0b258465))
* turning Solo back on immediately keeps only the selected screen's sound ([eb1b21e](https://github.com/lasme-ephrem/lasmium-pulse/commit/eb1b21e334f84d1834ea0d78847a80cdcf1b4d65))
* **ui:** favicon badge large enough to read the live count at tab size ([5d5b51e](https://github.com/lasme-ephrem/lasmium-pulse/commit/5d5b51ee340392181fb216e9933f6ce4549f241f))
* **ui:** no more overlapping in tile bars and the top bar on narrow widths ([bf6a819](https://github.com/lasme-ephrem/lasmium-pulse/commit/bf6a819f43beacc223abff1ae17cecddb387adb4))
* **ui:** slower favicon pulse ([eb82bda](https://github.com/lasme-ephrem/lasmium-pulse/commit/eb82bdaa78f0a649069c21362b6cb40377c32e34))


### Performance Improvements

* **client:** split the bundle, load hls.js on demand, batch chat updates; add error boundaries, bundled fonts, sandboxed iframes ([d7d3671](https://github.com/lasme-ephrem/lasmium-pulse/commit/d7d36711b6f7e9fb88f4d2a1265b82f64cab346d))
* **player:** hold live playback ~4 s behind the edge instead of ~18 s ([4a12039](https://github.com/lasme-ephrem/lasmium-pulse/commit/4a1203930be8c8553acf50dcf0e489b09aaa9131))
