# Universal File Converter

A single-file, browser-based file converter. No uploads, no server, no backend —
everything runs client-side using the Canvas, Web Audio, and MediaRecorder APIs.

## Features

- **Video** → WebM, MP4, animated GIF, or extracted audio (MP3/WAV) — with resolution
  downscaling and audio preserved on export
- **Audio** → MP3 (stereo), WAV, or OGG/Opus (where the browser supports it)
- **Images** → PNG, JPEG, WebP, BMP, ICO — with adjustable quality
- **Documents** → TXT, Markdown, HTML, JSON, CSV, PDF
- Drag-and-drop or click-to-browse, batch queue, per-file or "convert all" formats

## Usage

Just open `file-converter.html` in a modern desktop browser (Chrome, Edge, or
Firefox recommended). No install, no build step.

## Notes / limitations

- GIF export is capped at the first 10 seconds of a video (browser memory limits).
- MP4 output falls back to WebM in browsers that don't support `MediaRecorder`
  encoding to MP4 (most non-Chromium browsers).
- OGG export requires a browser that supports Opus recording (Firefox does;
  Chromium-based browsers generally don't) — you'll get a clear error instead of
  a mislabeled file if it's unsupported.
- Large video files can be slow to process since encoding happens in real time
  in the browser.

## Privacy

Files never leave your machine — all conversion happens locally in the browser tab.
The only external network calls are to load two small libraries from a CDN
(lamejs for MP3 encoding, gif.js for animated GIFs), fetched on first use.

## License

MIT — see [LICENSE](./LICENSE).
