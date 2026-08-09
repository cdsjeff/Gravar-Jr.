# Gravar Jr. v1.38 — Visible Frame Clip

This package contains the current standalone Gravar Jr. build.

## Files

- `index.html` — the Gravar Jr. application
- `help.html` — standalone help file
- `starting_up.html` — standalone startup guide
- `README.md` — this file

## v1.38 diagnostic repair

The prior zoom repair still allowed the visible media box to behave like the whole frame was growing. The fix separates the video display into three layers:

1. a fixed black video pane,
2. a fixed original visible picture rectangle,
3. an internal media layer that alone is scaled and panned.

The video/iframe itself is no longer directly transformed. The +/− buttons, Command-Option vertical drag, and pinch/trackpad pinch now transform only the internal media layer. The original picture boundary remains fixed and clips the enlarged image.


## v1.38 note

Frame Clip now captures the visible cropped picture area for local videos. When the picture is zoomed and panned, the exported clip matches what is visible inside the fixed picture boundary rather than the full original source frame.
