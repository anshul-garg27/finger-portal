# Finger Portal

Open portals to other worlds using just your fingers. Make a circle with your thumb and index finger — a portal opens showing a galaxy, underwater scene, fire, forest, or cyberpunk city inside.

![Demo](https://img.shields.io/badge/status-live-brightgreen) ![HTML](https://img.shields.io/badge/tech-HTML%20%2B%20Canvas%20%2B%20ES%20Modules-orange) ![MediaPipe](https://img.shields.io/badge/tracking-MediaPipe%20Tasks%20Vision-blue)

## How It Works

1. **Open** `index.html` in Chrome/Edge (needs webcam access)
2. **Make a circle** with your thumb and index finger
3. A **portal opens** showing another world inside your finger circle
4. **Move your hand** — portal follows smoothly
5. **Tilt your hand** — parallax shifts the world inside
6. **Peace sign** with other hand — switches to next world
7. **Space / Arrow keys** — switch worlds via keyboard
8. **Reach in** with your other hand — distortion effect

## Worlds

| World | Visual Effects |
|-------|---------------|
| Galaxy | Spiral arms (Density Wave Theory), nebula clouds, core glow, colored stars, shooting stars |
| Fire | Rising flame particles with additive blending, lava base glow, ember color transitions |
| Underwater | Animated caustic light patterns, rising bubbles with highlights, volumetric bottom fog |
| Forest | Volumetric god rays, falling leaves with rotation, floating dust motes, atmospheric depth |
| Cyberpunk | Neon grid, digital rain with trails, scanline effect, neon bloom pulse |

## Visual Effects

- **Chromatic aberration** — RGB channel shift at portal edge
- **Vortex rim particles** — swirling particles along the portal border
- **Light spillage** — portal color tints the surrounding camera feed (screen blend)
- **Shadow ring** — darkens area around portal to anchor it in reality
- **Additive glow** — all effects use `globalCompositeOperation: lighter` for cinematic bloom
- **Portal vignette** — dark edges create depth illusion inside the portal
- **Particle burst** — explosion effect when portal closes
- **Leak particles** — world-colored particles escape from portal edge

## Tracking

- **MediaPipe Tasks Vision** (modern `HandLandmarker` API, GPU-accelerated)
- **EMA landmark smoothing** — exponential moving average kills hand jitter
- **Smoothed portal position** — center and radius interpolated for fluid movement
- **Smoothed parallax tilt** — no jerky movement when tilting hand
- **Gesture debouncing** — prevents portal flickering on/off

## Tech Stack

- **@mediapipe/tasks-vision** — modern hand landmark detection (GPU delegate)
- **Canvas 2D API** — rendering, clipping, compositing, blend modes
- **ES Modules** — modern JavaScript imports from CDN
- **Procedural generation** — all worlds generated with particles and math, zero external assets
- **Single HTML file** — no build tools, no npm, no framework

## Requirements

- Modern browser (Chrome/Edge recommended)
- Webcam
- Decent lighting on your hands

## Performance Notes

- Targets 60fps on modern hardware
- GPU-delegated hand tracking offloads ML inference
- Additive blending is hardware-accelerated
- Offscreen canvas architecture ready for further optimization
- ~650 lines total, single file

## Future Enhancements

- [ ] Three.js 3D worlds with real depth and camera rotation
- [ ] Video/image backgrounds as world option
- [ ] Sound effects (whoosh on open, ambient per world)
- [ ] Two-hand portal (both hands form bigger portal)
- [ ] Screenshot/record button for reel content
- [ ] Mobile touch fallback
- [ ] WebGL shader post-processing (bloom, ripple distortion)
- [ ] Deploy to Vercel/Netlify

## License

MIT
