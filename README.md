# Fluid Tilt – 2D Particle Fluid

Real-time 2D fluid in the browser (no dependencies) that fills exactly 40% of the screen, leaving 60% air, and sloshes with your phone's gyro. It uses a double-density-relaxation particle solver (Clavet et al.) with a spatial grid, drawn as a blue metaball surface.

**Live demo:** https://bhargavd1501.github.io/Fluid-tilt/

- Tilt the phone to move the water (device orientation sensor, accelerometer fallback, drag-to-tilt if no sensor)
- Fixed 40:60 water-to-air ratio at any screen size, aspect ratio or DPI
- Particles stay inside the outer screen edges, with adjustable bounce and friction
- ⚙ panel: fluid density, stiffness, viscosity, cohesion, gravity
- Speed-based colour shading, fixed 120 Hz physics step for frame-rate independence
- Installable as a Progressive Web App (works offline after the first visit)

## Files
`index.html` (the app) · `manifest.json` · `sw.js` · `icon-192.png` · `icon-512.png`

## Install
Open the GitHub Pages link in Chrome → ⋮ menu → **Install app** (or **Add to Home screen**). Tap **Start** and allow motion access. Sensors only work over HTTPS, not from a local file.

## Tuning
Constants are at the top of the script in `index.html`: `TARGET_PARTICLE_COUNT`, `CFG.density`, `CFG.stiffness`, `CFG.viscosity`, `CFG.cohesion`, `CFG.restitution`. If the water moves the wrong way, tap **Flip tilt**.

## Note
Educational and visual toy, not a validated CFD solver. The fluid compresses slightly under gravity.
