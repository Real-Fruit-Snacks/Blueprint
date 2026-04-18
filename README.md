# Blueprint

An incremental factory game. Build, automate, prestige, publish.

**Play:** https://real-fruit-snacks.github.io/blueprint/

---

## About

Blueprint is a browser-based incremental game built in pure HTML, CSS, and JavaScript — no frameworks, no dependencies, no build step. The entire schematic aesthetic is rendered with SVG and CSS primitives.

Mine Ore, smelt it into Ingots, craft Parts, assemble Circuits, forge Cores, and refine Prototypes. Invest Schematics into a radial research tree. Publish your work for permanent Patents that persist across every reset.

## Features

- **6-tier production chain** — 28 machines spanning Extraction through Refinement
- **Radial research tree** — 45+ nodes across 6 branches with progressive reveal
- **Two-layer prestige loop** — per-run Schematics for the tree, meta-layer Patents for permanent bonuses
- **Patent Library** — 15+ unlocks and leveled upgrades that survive every reset
- **30+ achievements** — each granting a small stacking passive bonus
- **Per-resource manual crafting** — each tier has its own click-to-convert operation with real input costs
- **Per-resource auto-mine toggles** — unlockable via research and the Omnitap patent
- **Offline progression** — capped at 8 hours, extendable via patents
- **Procedural audio** — synthesized with the Web Audio API, no external files
- **Local save** — with base64 export/import for backup or transfer

## Controls

| Action | Shortcut |
| --- | --- |
| Buy 1 | Click a machine |
| Buy ×10 | Shift+Click *(requires Bulk Buy)* |
| Buy ×100 | Shift+Alt+Click *(requires Bulk Buy)* |
| Buy ×1000 | Ctrl+Shift+Click *(requires Max Buy)* |
| Toggle auto-buy | Right-click a machine *(requires Auto-Buy)* |
| Pan research tree | Click and drag |
| Zoom research tree | Scroll wheel · or the +/− buttons |

All shortcuts unlock through gameplay — nothing is locked behind external config.

## Running Locally

Open `index.html` in any modern desktop browser. No install, no build step, no server required.

## Tech

- Vanilla HTML / CSS / JavaScript
- Web Audio API for procedural sound
- LocalStorage for persistence
- Single-file deploy — static to any web host (GitHub Pages, Netlify, itch.io, etc.)

## License

MIT — see [LICENSE](LICENSE).
