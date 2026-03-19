# TileWorks · Tileset Tool

A free, browser-based tileset tool — no server, no tracking, no data leaves your browser.

**[tileworks.net](https://tileworks.net)**

Made with ❤️ and Privacy by [elexity](https://github.com/maskedByte/TileWorks).

---

## Features

### 🗂️ Create Tileset
Combine multiple individual tile images into a single tileset PNG.

- Upload PNG/JPG images via drag & drop or file picker into the library
- Configure tile size (width × height) and number of columns
- **Auto-fill** — automatically distribute all library images across the grid
- Manually drag images from the library onto specific grid cells
- **Swap tiles** via drag & drop between grid positions
- Images with a different size than the configured tile size trigger a scale confirmation dialog before placing
- Zoom (scroll) and pan (Alt+drag or middle-click) the canvas
- Toggle between Nearest and Linear display rendering (editor display only — does not affect the exported PNG)
- Download the finished tileset as a single `tileset.png`

### ✂️ Split by Grid
Extract individual tiles from an existing tileset using a regular grid.

- Load a tileset image from the library
- Configure tile width, height, X/Y offset and X/Y spacing
- Live grid overlay shows exactly which tiles will be extracted
- Toggle display rendering (editor only)
- Download all extracted tiles as a ZIP archive (`tile_RR_CC.png` naming)

### 🔲 Split Freely
Extract tiles from a tileset without a fixed grid — draw your own selection rectangles.

- Load a tileset image from the library
- Draw, move and resize selection rectangles freely on the canvas
- Each selection can be renamed in the side panel
- Pixel-perfect, anti-alias-free selection borders at any zoom level
- Toggle display rendering (editor only)
- Export all selections as a ZIP archive (filenames from selection labels)

---

## Privacy

All image processing happens entirely inside your browser using the Canvas API.  
No files are uploaded to any server. No analytics, no cookies, no external requests.

Images are persisted in `sessionStorage` for the duration of the browser session so you can refresh without losing your work. They are gone as soon as the session ends or the browser cache is cleared.

---

## Tech Stack

| | |
|---|---|
| Framework | [React 19](https://react.dev/) + [TypeScript](https://www.typescriptlang.org/) |
| Bundler | [Vite 8](https://vite.dev/) |
| ZIP export | [JSZip](https://stuk.github.io/jszip/) |
| Rendering | HTML5 Canvas API |
| Styling | CSS Modules |

