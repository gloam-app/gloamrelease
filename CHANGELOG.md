# Changelog

Release notes for every published Gloam build. Each entry matches a [GitHub Release](https://github.com/gloam-app/gloamrelease/releases).

## [1.0.2](https://github.com/gloam-app/gloamrelease/releases/tag/v1.0.2) — 2026-09-02

### Fixed

- Scene deletion now commits its library update atomically, so cleanup errors cannot leave stale cards behind.
- Removing the final scene now clears staged lock-screen media and restores Apple’s built-in wallpaper.

### Download

[Gloam.dmg](https://github.com/gloam-app/gloamrelease/releases/download/v1.0.2/Gloam.dmg)

## [1.0.1](https://github.com/gloam-app/gloamrelease/releases/tag/v1.0.1) — 2026-09-02

### Fixed

- Restored the live wallpaper catalog for public builds.
- Scene deletion now removes the item immediately and switches away from a deleted active scene.
- Deleting the final active scene now returns the desktop to the user’s Apple wallpaper.

### Changed

- Discover is included in Gloam without API-key setup in the app.

### Download

[Gloam.dmg](https://github.com/gloam-app/gloamrelease/releases/download/v1.0.1/Gloam.dmg)

## [1.0.0](https://github.com/gloam-app/gloamrelease/releases/tag/v1.0.0) — 2026-08-31

First public release. Signed and notarized Mac installer (`Gloam.dmg`).

### Highlights

- Live video wallpapers on the desktop
- Optional lock screen video (requires Full Disk Access)
- Import your own clips
- Browse stock video from Pexels
- No account — files stay on your Mac

### Requirements

- macOS 14 (Sonoma) or later

### Download

[Gloam.dmg](https://github.com/gloam-app/gloamrelease/releases/download/v1.0.0/Gloam.dmg)
