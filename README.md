# WingtraLIDAR PointCLOUD Viewer

A lightweight, browser-based LiDAR point cloud viewer for `.las` files — no server, no install, pure WebGL.

## Features

- **Drag & drop** `.las` file upload — directly on the canvas or in the sidebar (LAS 1.0–1.4, point formats 0–8)
- **Large file support** — chunked streaming parser handles files of any size (tested up to 8 GB+), never loading the full file into memory
- **Color modes:** Elevation (Jet colormap with adjustable min/max range) · RGB (if present in file)
- **Profile View** — angular cut plane (0–179°) with Near/Far sliders, second perpendicular cut, manual % input
- **Viewer Quality** — subsampling ratio, point size (0.1–6), brightness
- **Perspective & Views** — Auto-rotate, Reset, Top, Back, Side L/R
- **Export** — JPG/PNG at 6 preset resolutions up to 6000×6000, export frame preview overlay
- Auto-subsamples large files (>4M points) for smooth performance

## Tech Stack

| Dependency | Source |
|---|---|
| [Three.js r128](https://threejs.org) | cdnjs CDN |
| [Rajdhani + JetBrains Mono](https://fonts.google.com) | Google Fonts |

No build step. No npm. No framework. Single `index.html`.

## Deploy to Vercel

### Option 1 — Vercel CLI
```bash
npm i -g vercel
vercel
```

### Option 2 — GitHub Integration
1. Push this repo to GitHub
2. Go to [vercel.com](https://vercel.com) → **Add New Project**
3. Import your GitHub repo
4. Framework preset: **Other** (Static)
5. Click **Deploy** — done

## Run locally

Just open `index.html` in any modern browser. No server needed.

```bash
# Or with a simple dev server:
npx serve .
```

## Usage

1. Open the deployed URL
2. Drag a `.las` file onto the upload zone or directly onto the viewer canvas
3. Use the sidebar to adjust color, range, profile cuts and camera settings
