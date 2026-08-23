# Gravar Jr. v1.49

Repository-ready build of Gravar Jr.

## v1.49 local-video rebuild

This release replaces the accumulated local-video compatibility patches with a clean native playback path.

- Local files are chosen through a direct browser file input in the File menu; Gravar Jr. no longer relies on a scripted `.click()` to open the file picker.
- The native HTML5 `<video>` element is the primary visible local-video surface.
- The obsolete `video-source-hidden` class and its `opacity:0 !important` rule are removed.
- Brightness, Contrast, and Color/Saturation are `none` at neutral settings and are applied directly to the local video only when changed.
- The parent media layer is not filtered for local playback.
- RGB processing remains optional: the canvas overlay is hidden until R, G, or B differs from 100%.
- The local-video diagnostic strip now reports file acceptance, metadata decode, dimensions, duration, readyState, stalls, browser media errors, and playback-promise errors.
- The File menu closes automatically after a local file is selected.

## Verified sample file

`L_turn-taking.mp4` was tested through the actual `<input type="file">` change path. Chromium decoded it as 640×360, 56.13 seconds, reached readyState 4, displayed the native video at opacity 1 with no filter on the parent layer, and advanced playback successfully. RGB activation was also verified to turn on the optional canvas overlay without hiding the native video.

## GitHub Pages

Upload the contents of this folder to the repository root. `index.html` is the deployable Gravar Jr. page.

Files:
- `index.html` — GitHub Pages entry point
- `Gravar_Jr_v1.49.html` — named standalone copy
- `help.html` — concise Help page
- `starting_up.html` — concise Starting Up guide
- `shortcuts.html` — shortcuts reference
