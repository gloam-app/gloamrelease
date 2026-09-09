# Changelog

Release notes for every published Gloam build. Each entry matches a [GitHub Release](https://github.com/gloam-app/gloamrelease/releases).

## [0.0.3](https://github.com/gloam-app/gloamrelease/releases/tag/v0.0.3) — 2026-09-08

### Changed

- The main navigation is now Desktop, Discover, and My Scenes: Desktop shows what is playing and what is already on this Mac, while Discover is clearly for finding new online wallpapers.
- Desktop no longer repeats the scene list from My Scenes. It now shows what is on your desktop, moods suggested for right now, and a single link into My Scenes for the full library.
- Every page now explains its purpose in place. My Scenes focuses only on managing local media, mood pages distinguish local and online results, collections explain what they contain, and the Discover settings category is now clearly named Online Catalog.
- The Desktop banner groups its title and Set as Wallpaper action over the artwork, while staying short enough to keep the scene grid visible.
- The menu-bar popover now uses a single transport row rather than stacked menu rows, and reserves colour for readings that need attention rather than routine ones.
- The scene details panel now uses one label style for every field, credits a photographer once instead of twice, shows the favourite control on the artwork, and keeps Delete Scene at the end away from the primary button.
- First-run setup is tighter: Welcome and All Set play the live scene behind the text as one centred block, and setup copy now uses the same system typeface as the rest of the app.
- Settings rows are held to a readable width instead of stretching a label and its control across the whole window, and preferences use switches like System Settings.
- The library window opens at 920×600 with a shorter Desktop banner and a denser three-across card grid, instead of a wide 1120×700 gallery.
- Page tabs, mood chips, Favourites, and My Scenes are plain text controls. Collections, All moods, and the Add-scene plus-menu are gone; adding a scene uses a two-choice sheet.
- Scene cards scale and dim on press, hover still previews, and tapping the idle Desktop banner sets the wallpaper.
- The status icon’s right-click menu is now a small fallback containing only Open Gloam, Settings, and Quit.
- The menu-bar popover is now just what is playing, Pause and Next, and the way into Gloam, Settings, or Quit. Quick Switch, the display and lock-screen switches, the context and CPU readings, and Shuffle are gone from the menu bar; each of those decisions is made in the window or Settings, where the artwork and explanations are.
- Automatic scene switching now has a proper home in Settings under Playback, with an explanation of what it does, instead of an Auto/Manual chip in the menu bar.
- The duplicate macOS View menu was removed; appearance remains available in Settings.
- Creating a photo slideshow now uses the reliable native photo picker, and media pickers wait for the Add sheet to close before presenting.
- Local videos and photo slideshows preview while hovered and set as the wallpaper with one click; scene details remain available from the card’s context menu.
- Settings is now one compact, scrollable page like the rest of the app, with no category sidebar or nested detail page. Related options share consistent rows and short explanations.
- Settings uses one set of headings, row heights, switches, and sliders instead of mixing custom cards with grouped forms.
- The Displays page dropped its Follow-main-display/Off picker, whose two options repeated the switch next to it, and now names each screen's resolution instead.
- Scene cards no longer show a passive “Click to set” label. Clicking still applies the scene, and Gloam now confirms the scene is your wallpaper only after the apply operation succeeds.

### Fixed

- Search is now visible and scoped to the current page, with page-specific prompts, result counts, Command-F focus, Escape-to-clear, and clear loading, empty, and error states.
- Discover search results now fill the window in a grid that reflows with the window width, instead of four cards per row followed by empty space, and a Load More button fetches further pages.
- Discover search no longer displays stale results from an earlier query, and retry now repeats the failed search instead of refreshing the general catalog.
- Load More now reveals another set of Discover results, including results already cached locally, and skips duplicate API pages instead of appearing to do nothing.
- Video Upload now opens a reliable native picker from every My Scenes entry point, accepts all supported video formats, and understands the URL forms used by Finder and other drag sources.
- Deleting a personal video or photo slideshow now uses a visible confirmation alert before removing it from My Scenes.
- Live video is back on the lock screen. Gloam checked the wallpaper store for both the lock screen slot and the screen saver slot, and macOS keeps removing the screen saver one — so Gloam decided the lock screen was broken, rewrote the store, and restarted the system wallpaper engine over and over.
- The Lock Screen switch in Settings now stages the current scene when you turn it on, and Restart re-links it, instead of only recording the preference.
- The lock screen keeps its live wallpaper. Staging a clip for one scene deleted the staged clips of every other scene, so importing or switching scenes could delete the very clip the lock screen was playing — macOS was left pointing at a wallpaper that no longer existed.
- Gloam now notices when its lock screen clip disappears from Apple's wallpaper catalog and stages it again, instead of leaving a lock screen that looks configured but plays nothing.
- Staging two scenes at once no longer loses one of them. Gloam edits Apple's wallpaper catalog one change at a time, so overlapping edits cannot drop each other's entry.
- Running Gloam's own tests no longer takes the live wallpaper off your lock screen: tests now use a throwaway copy of the wallpaper store instead of the real one.
- Desktop video resumes immediately after the Mac wakes. Sleep no longer gets mistaken for a manual pause, and Gloam reasserts playback while displays reconnect.
- Gloam rebuilds Apple's aerial extension after wake instead of trusting a process that survived sleep but stopped producing video frames.
- Locking and unlocking repeatedly keeps the live wallpaper. Gloam used to restart Apple's wallpaper agents while the screen was locked, which killed the process painting the lock screen — the wallpaper survived the first lock and vanished on the next one. A locked session cannot start that process again, so Gloam now leaves it alone across a lock and only nudges it when it has gone missing.
- The lock screen no longer goes black after an unlock. Apple's aerial extension loses its video reader while the lock screen tears down, and nothing inside it recovers: the same process stayed alive producing no frames, so every later lock was black. Gloam now replaces that extension while the Mac is unlocked, leaving one that can play ready for the next lock.
- Gloam stopped rewriting the screen saver slot on every lock and unlock. macOS strips it again within seconds, and rewriting it mid-lock made Apple's extension re-resolve its video and lose its sample reader.
- Gloam and macOS no longer trade writes over the wallpaper store. Gloam ignores the file changes it makes itself and repairs the store at a measured pace, instead of turning one rewrite by macOS into a chain of repairs that reloaded the lock screen each time.
- Setting a scene as the lock screen restarts Apple's wallpaper agents once rather than three times in quick succession.
- After each unlock Gloam confirms the lock screen clip is still staged and gets Apple's aerial extension running again, so every following lock has a wallpaper ready.
- Gloam keeps watching Apple's wallpaper store after macOS replaces the file, instead of missing every later change.
- Gloam's diagnostic log is readable in a released build. Every line it wrote was recorded as `<private>`, so a report about the lock screen came with no record of what Gloam had actually done.

### Download

[Gloam.dmg](https://github.com/gloam-app/gloamrelease/releases/download/v0.0.3/Gloam.dmg)

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
