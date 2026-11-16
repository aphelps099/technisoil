# TechniSoil Motion Studio

A buildless, browser-based product video editor at `/studio/`.

## Run

From the repository root:

```sh
python3 -m http.server 4173
```

Open http://localhost:4173/studio/.

The Brand House homepage links to the studio. No package installation or backend is required. Product artwork is stored locally; typography loads from Google Fonts with system fallbacks.

## Features

- Eleven product presets from the Brand House catalog, each with four editable scenes.
- Product, statement, benefits, image, video, and end-card scenes; reorder, duplicate, delete, undo, and redo.
- Full-height white product panels, large product artwork, centered statement/end-card typography.
- Six animation styles, five brand palettes, timing, playback, seeking, looping, and safe-area guides.
- Landscape (1920×1080), portrait (1080×1920), and square (1080×1080) output.
- Image/video uploads and one soundtrack or voiceover track with volume control.
- IndexedDB autosave and portable JSON project import/export, including uploaded media.
- PNG frames and real-time video recording using the same canvas renderer as the preview. MP4 is preferred where supported by MediaRecorder; otherwise WebM is used.

## Limits

Keep the tab visible during recording. Browser scheduling can affect recording smoothness. Clip audio is muted; uploaded soundtrack/voiceover audio is mixed into the video. Upload limits are 80 MB per scene asset and 40 MB for audio. Local storage is browser-specific; download projects for backup. Product claims originate from the existing catalog; review campaign copy before publishing ads.

## Verification

`node --check studio/studio.js`

Browser checks covered product generation, scene editing and duplication, undo, format switching, saved-project restoration, canvas preview, and a completed video export. The UI is responsive and supports keyboard-accessible controls.
