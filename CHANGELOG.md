# Changelog

Release notes for every published Gloam build. Each entry matches a [GitHub Release](https://github.com/gloam-app/gloamrelease/releases).

## [0.0.5](https://github.com/gloam-app/gloamrelease/releases/tag/v0.0.5) — 2026-09-02

### Added

- Assign any personal video or photo-slideshow scene to a built-in or custom mood.
- Override Gloam’s suggested mood, remove a mood assignment, or return to automatic suggestions from the scene inspector.
- Review, reorder, or remove photos before creating a slideshow.
- Choose any 2–60 second photo interval, see the total runtime, and select fill-screen or fit-whole-photo framing.
- Rename personal scenes directly from Details.

### Fixed

- Quick Switch keeps every scene in a stable position and moves the checkmark instead of moving the selected row.
- Favourite ordering now survives app relaunches and catalog refreshes.
- Active-scene deletion now chooses its replacement from the same stable Quick Switch order.
- Dragging media onto My Scenes now performs the import instead of only showing the drop highlight.
- Photo slideshows are identified correctly as locally built slideshows in scene details.
- Add Scene consistently offers videos and photo slideshows throughout Home and My Scenes.
- Video pickers and drag-and-drop now accept the same supported formats.
- Multi-video imports report partial failures instead of silently ignoring them.
- Long slideshow renders show per-photo progress and can be cancelled without leaving a partial scene.
- Successful imports open their new scene in My Scenes, where mood, playback, and lock-screen details are visible.
- Paused playback, favourites for Quick Switch, and Apple-wallpaper deletion fallback are clearer.

### Download

[Gloam.dmg](https://github.com/gloam-app/gloamrelease/releases/download/v0.0.5/Gloam.dmg)

## [0.0.4](https://github.com/gloam-app/gloamrelease/releases/tag/v0.0.4) — 2026-09-02

### Added

- Create live desktop and lock-screen slideshows from 2–100 image files with a configurable display interval.
- Added an in-app Privacy settings page and a complete website privacy policy.

### Privacy

- Photo slideshows are rendered entirely on the Mac from files explicitly selected with Apple’s file picker.
- Gloam does not request Photos-library access and never uploads personal videos or photos.
- Removed unused analytics and crash-reporting SDKs from the app.
- Location is no longer requested during onboarding; optional weather context explains its third-party processing.

### Download

[Gloam.dmg](https://github.com/gloam-app/gloamrelease/releases/download/v0.0.4/Gloam.dmg)

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
