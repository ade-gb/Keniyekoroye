# Responsive Interactive Web Showcase

## Overview

This repository contains a small, static single page website designed as an interactive visual showcase. The project combines modern front-end motion techniques (scroll-linked animations, smooth scrolling), WebGL/3D support, and media-rich gallery assets to create an engaging portfolio or demo page.

The site is delivered as a static artifact centered around `index.html` and supported by a custom stylesheet and several vendor JavaScript libraries.

## Key Features

- Interactive animations driven by GSAP and ScrollTrigger for polished, scroll-linked motion.
- Smooth scrolling via `lenis.js` (or similar) for fluid page navigation.
- Optional 3D scenes using Three.js (`three.min.js`) for WebGL-based visuals.
- Media-rich gallery with optimized images (AVIF) in the `images/` folder.
- Modular script organization in `js/` so vendor libraries and application scripts stay separated.
- Custom typography and layout controlled by `css/Keniyekoroye.css` and assets in `fonts/`.
- Socket.IO present (`socket.io.min.js`) if realtime features are added later.

## Tech Stack & Libraries

- HTML5 — `index.html` is the single-page entry.  
- CSS — Custom styles live in `css/Keniyekoroye.css`.  
- JavaScript — Vendor libraries are included in `js/`:
  - `gsap.min.js` (GSAP animation engine)
  - `ScrollTrigger.min.js` (scroll-based animation triggers)
  - `lenis.js` (smooth scrolling)
  - `three.min.js` (WebGL / 3D rendering)
  - `socket.io.min.js` (optional realtime)
  - `jquery-3.5.1.min...` (legacy helpers if referenced)

## Project Structure (important files)

- `index.html` — Main page and script/style includes.
- `css/Keniyekoroye.css` — Core styling for layout, responsive rules, and typography.
- `js/` — Vendor and site scripts. Keep vendor libs first, then custom scripts.
- `images/` — Media assets; large images may be AVIF/WebP optimized for performance.
- `fonts/` — Local font files used by the design.

Sample tree:

```
index.html
css/
  Keniyekoroye.css
fonts/
images/
js/
```

## Installation & Local Usage

No build step is required — this is a static site. Two simple ways to run locally:

1) Quick (may work for simple demos):

   - Open `index.html` in a browser.

2) Recommended (serves files over HTTP — necessary for some APIs and modules):

```bash
# Python 3
python3 -m http.server 8000
# then open http://localhost:8000 in your browser

# or using the `serve` npm package
npm install -g serve
serve .
```

Use a static server when testing Three.js, module imports, or features that require proper HTTP headers.

## Customization Tips

- Replace images in `images/` and adjust markup in `index.html` where the gallery or hero images are referenced.  
- Edit `css/Keniyekoroye.css` to change colors, spacing, breakpoints, and typography.  
- Add or remove vendor scripts in `index.html` depending on which features you need (e.g., remove `socket.io.min.js` if realtime is not used).  
- For Three.js customizations, find the initialization code in the `js/` scripts and update scene, camera, and renderer parameters.

## Development Notes

- Keep vendor libraries in `js/` and reference them before your custom scripts so dependencies load in the correct order.  
- During development, use unminified versions of libraries and enable source maps for easier debugging.  
- When deploying, bundle/minify and optimize assets for performance, and convert large raster images to AVIF/WebP where supported.

## Accessibility & Performance

- Add `alt` attributes for all meaningful images.  
- Use semantic heading structure (H1 → H2 → H3) for screen reader navigation.  
- Test the site on mobile viewports and slow devices to ensure animations remain smooth; consider reducing animation complexity on low-powered devices.  
- Lazy-load offscreen images and defer non-critical scripts to improve first paint metrics.

## Contributing

- Fork the repository and open a pull request with a clear description of the change.  
- Include screenshots or a short GIF for visual changes.  
- Run the site locally via a static server to validate changes before opening a PR.

## Suggested License

Consider using the MIT License for permissive reuse, or choose another OSI-approved license depending on your goals. Add a `LICENSE` file at the repo root if you want to publish with an explicit license.

## Credits & Third-Party Libraries

- GSAP (gsap.min.js)
- ScrollTrigger (ScrollTrigger.min.js)
- Lenis (lenis.js)
- Three.js (three.min.js)
- Socket.IO (socket.io.min.js)
- jQuery (included but optional)

List any font sources or image attributions here if they come from third-party providers.

## Usage Scenarios / Examples

- Personal or freelance portfolio with animated hero and project gallery.  
- Landing page with parallax/scroll-triggered sections.  
- Interactive demo showcasing WebGL/3D experiments.

## Next Steps / Recommendations

- If you plan to publish this on GitHub Pages or a CDN, test performance and enable aggressive image optimization.  
- Add a `LICENSE`, update `README.md` with your contact or author info, and create an issue template if you expect contributions.

---

If you want, I can commit this `README.md` to the repository, create a `LICENSE` file (MIT), or generate a short `CONTRIBUTING.md`. Tell me which you'd like next.
