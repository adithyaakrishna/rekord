# Rekord Spotify Hardware Player

`rekord.html` is a standalone browser-based Spotify player widget styled like a compact hardware music device. It preserves the original chassis style interface while adding Spotify login, playback controls, haptics, animated playback feedback, and a physical feeling volume dial.

## Features

- Spotify login using Authorization Code with PKCE.
- Spotify Web Playback SDK integration.
- Play/pause, pause/stop, previous, and next controls.
- Live track title, artist, duration, and playback state display.
- Animated platter and waveform while music is playing.
- Smooth lower-right volume dial with pointer/touch drag and throttled Spotify volume updates.
- Mobile haptic feedback via `web-haptics`.
- Visual state lighting:
  - Green `CONNECT TO SPOTIFY` prompt before authentication.
  - Lit red record button before authentication.
  - Lit transport, arrow, and volume tick controls after authentication.

## Requirements

- A Spotify developer app.
- Spotify Premium for in-browser playback through the Web Playback SDK.
- A browser that supports modern JavaScript modules and the Web Crypto API.
- A mobile browser with Vibration API support for physical haptic feedback.

## Controls

- Red record button: connect to Spotify, or clear the stored session when already connected.
- Play button: toggle playback.
- Stop button: pause playback.
- Up arrow: previous track.
- Down arrow: next track.
- Lower-right dial: drag or scroll to adjust volume.

## Notes

- Spotify playback starts after login and device transfer to the browser player.
- If no Spotify playback is active, choose music in Spotify first, then use the widget controls.
- Haptics are best tested on a physical mobile device; desktop browsers may not provide tactile feedback.
- The waveform and platter animate only when Spotify reports that playback is active.
