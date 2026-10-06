# Bible Verse Wallpaper Maker

A free, browser-based tool that turns a Bible verse into a phone or desktop wallpaper. Everything runs in the browser: no account, no watermark, nothing is uploaded.

## Features

- **Verse:** type or paste any verse, with a reference and translation, or press **Random verse**.
- **References:** curated King James Version (KJV) verses for the selected topic.
- **Topics:** Love, Peace, Strength, Hope, Comfort, Faith, Joy, Gratitude, Courage, Guidance. Random verse draws from a separate pool of 8 verses per topic.
- **Backgrounds:** Pure black, Heavenly light, Sunrise, Cream paper, Navy and gold, Minimal white, Bold sans, or your own photo (with a darken slider).
- **Sizes:** iPhone (1179x2556), iPhone Pro Max (1290x2796), Android (1080x2400), Desktop 4K (3840x2160).
- **Safe zones:** the verse stays clear of the lock-screen clock and bottom buttons. A preview-only clock guide shows these areas and is never saved in the PNG.
- **Export:** full-resolution PNG, plus the system share sheet where the browser supports it.

## Run locally

It is a single static file with no build step.

```bash
# Option 1: just open index.html in a browser
# Option 2: serve it locally
python3 -m http.server 8000   # then visit http://localhost:8000
```

Fonts (Newsreader, Hanken Grotesk) load from Google Fonts and fall back to system fonts when offline.

## Deploy

Any static host works. For GitHub Pages: Settings > Pages > Deploy from branch > `main` / root.

## Project layout

```
index.html   the whole app: HTML, CSS and JavaScript
README.md
```

## Notes

- Bible text is the King James Version, which is public domain. Other translations are mostly copyrighted, so only add them if you have permission.
- The wallpaper is drawn on an HTML canvas at the exact target resolution and exported with `canvas.toBlob`.
- Add a license of your choice before making the repository public.
