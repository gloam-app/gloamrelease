# Changelog

Release notes for every published Gloam build. Each entry matches a [GitHub Release](https://github.com/gloam-app/gloamrelease/releases).

## [0.0.3](https://github.com/gloam-app/gloamrelease/releases/tag/v0.0.3) — 2026-09-02

### Fixed

- Scene deletion now commits its library update atomically, so cleanup errors cannot leave stale cards behind.
- Removing the final scene now clears staged lock-screen media and restores Apple’s built-in wallpaper.

### Changed

- Feedback releases now use `0.0.x`; `1.0.0` is reserved for the production-ready MVP.
- The DMG now opens with a branded drag-to-Applications installer layout.

### Download

[Gloam.dmg](https://github.com/gloam-app/gloamrelease/releases/download/v0.0.3/Gloam.dmg)

## [0.0.2](https://github.com/gloam-app/gloamrelease/releases/tag/v0.0.2) — 2026-09-02

### Fixed

- Restored the live wallpaper catalog for public builds.
- Scene deletion now removes the item immediately and switches away from a deleted active scene.
- Deleting the final active scene now returns the desktop to the user’s Apple wallpaper.

### Changed

- Discover is included in Gloam without API-key setup in the app.

### Download

[Gloam.dmg](https://github.com/gloam-app/gloamrelease/releases/download/v0.0.2/Gloam.dmg)

## [0.0.1](https://github.com/gloam-app/gloamrelease/releases/tag/v0.0.1) — 2026-08-31

First small-audience feedback release. Signed and notarized Mac installer (`Gloam.dmg`).

### Highlights

- Live video wallpapers on the desktop
- Optional lock screen video (requires Full Disk Access)
- Import your own clips
- Browse stock video in Discover
- No account — files stay on your Mac

### Requirements

- macOS 14 (Sonoma) or later

### Download

[Gloam.dmg](https://github.com/gloam-app/gloamrelease/releases/download/v0.0.1/Gloam.dmg)
