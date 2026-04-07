# Finger Portal 🌀

Open portals to other worlds using just your fingers. Make a circle with your thumb and index finger — a portal opens showing a galaxy, underwater scene, fire, forest, or cyberpunk city inside.

![Demo](https://img.shields.io/badge/status-live-brightgreen) ![HTML](https://img.shields.io/badge/tech-HTML%20%2B%20Canvas-orange) ![MediaPipe](https://img.shields.io/badge/tracking-MediaPipe%20Hands-blue)

## How It Works

1. **Open** `index.html` in Chrome/Edge (needs webcam access)
2. **Make a circle** with your thumb and index finger
3. A **portal opens** showing another world inside your finger circle
4. **Move your hand** — portal follows
5. **Peace sign** (✌️) — switches to next world
6. **Reach in** with your other hand — distortion effect

## Worlds

| World | Visual |
|-------|--------|
| Galaxy | Rotating stars, nebula clouds, shooting stars |
| Fire | Rising flame particles, lava glow, ember effects |
| Underwater | Rising bubbles, caustic light, deep blue-green |
| Forest | Falling leaves, light rays, deep green canopy |
| Cyberpunk | Neon grid, digital rain, purple-pink particles |

## Features

- Real-time hand tracking with MediaPipe (21 landmarks per hand)
- Portal scales with your finger distance
- Parallax effect — tilt hand to shift the world inside
- Edge glow that pulses and matches the current world color
- Particles leak out from the portal edge
- Smooth open/close animations with particle burst on close
- Reach-in distortion when second hand enters portal
- Zero dependencies — single HTML file, no build tools

## Tech Stack

- **MediaPipe Hands** — hand landmark detection
- **Canvas 2D API** — rendering, clipping, compositing
- **Procedural generation** — all worlds are generated with particles and math, no external assets

## Requirements

- Modern browser (Chrome/Edge recommended)
- Webcam
- Decent lighting on your hands

## Future Enhancements

- [ ] Three.js 3D worlds with real depth
- [ ] Video/image backgrounds as world option
- [ ] Sound effects (whoosh on open, ambient per world)
- [ ] Two-hand portal (both hands form bigger portal)
- [ ] Screenshot/record button for reel content
- [ ] Mobile touch fallback
- [ ] Deploy to Vercel/Netlify

## License

MIT
