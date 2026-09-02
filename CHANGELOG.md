# Changelog

Release notes for every published Gloam build. Each entry matches a [GitHub Release](https://github.com/gloam-app/gloamrelease/releases).

## [0.0.2](https://github.com/gloam-app/gloamrelease/releases/tag/v0.0.2) — 2026-09-02

### Added

- Turn your own photos into a live desktop and lock-screen slideshow: pick 2–100 images, review and reorder them, choose a 2–60 second interval, and fill the screen or fit the whole photo.
- Assign any personal scene to a built-in or custom mood, override Gloam’s suggestion, or hand it back to automatic.
- Create and delete your own moods. Deleting one keeps its scenes in My Scenes.
- Rename personal scenes from the details panel.
- A Privacy page in Settings, plus a full privacy policy on the website.

### Changed

- Feedback builds now use `0.0.x`. `1.0.0` is reserved for the production-ready MVP.
- The installer opens with a branded drag-to-Applications layout.
- Discover works out of the box with no API key setup in the app.
- Adding a scene now lives only in My Scenes instead of being duplicated in the toolbar.
- Back navigation follows where you actually came from across Home, Discover, My Scenes, moods, and Settings.
- Scene details reflow beside the library instead of covering the scene cards.
- Import progress sits above the playback bar and says whether it is building a slideshow or importing a video.
- The menu bar explains why a scene is playing and reports imports or scene switches in progress.

### Fixed

- Restored the live wallpaper catalog for public builds, which had been empty.
- Deleting a scene now removes it immediately, commits atomically, and switches away from it if it was playing.
- Deleting your last scene restores your Apple wallpaper and clears staged lock-screen media.
- Quick Switch keeps every scene in a fixed position and moves a checkmark instead of shuffling the selected row.
- Favourite order survives relaunches and catalog refreshes.
- Dragging media onto My Scenes performs the import instead of only highlighting the drop zone.
- File pickers and drag-and-drop accept the same formats, and multi-file imports report partial failures as one combined result.
- Long slideshow renders show per-photo progress and can be cancelled without leaving a half-built scene.
- My Scenes search filters your scenes, and a stale search clears when you navigate away.
- The returning-session welcome no longer interrupts a file picker or slideshow setup.
- An empty Quick Switch menu now offers a way into the app.

### Privacy

- Photo slideshows are rendered entirely on your Mac from files you pick yourself.
- Gloam never asks for Photos-library access and never uploads your videos or photos.
- Removed the unused analytics and crash-reporting SDKs.
- Location is no longer requested during onboarding. Optional weather context explains its third-party processing.

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
