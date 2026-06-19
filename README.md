<div align="center">

  # Blueprint

  **An engineering-sheet incremental. Build a factory one machine at a time, prestige for Schematics, publish for Patents, exhibit for Legacy Marks.**

  [![License: MIT](https://img.shields.io/badge/License-MIT-cba6f7.svg)](https://opensource.org/licenses/MIT)
  [![Version](https://img.shields.io/badge/version-1.0.0-89b4fa)](https://github.com/Real-Fruit-Snacks/Blueprint/releases)
  
  [Play Blueprint](https://real-fruit-snacks.github.io/Blueprint) • [Report Issue](https://github.com/Real-Fruit-Snacks/Blueprint/issues)

</div>

---

## Overview

Blueprint is a **browser incremental drawn as an engineering schematic.** Mine ore, smelt ingots, press parts, assemble circuits, forge cores, and refine prototypes across six tiers. When a run matures, **prestige** to bank Schematics and unlock the radial research tree. Push deeper to unlock the meta layer — **publish** for Patents that persist across every reset, then **exhibit** for Legacy Marks that survive even publish.

No framework, no build step, no external assets. Every machine icon, research node, UI glyph, and sound is generated at runtime from SVG primitives and the Web Audio API. Pure vanilla HTML/CSS/JS, zero dependencies, installable as a PWA with offline play.

---

## Key Features

- **6 Tiers of Production:** Progress from Ore to Ingot, Part, Circuit, Core, and Prototype.
- **28 Machines:** Featuring three rarity rungs per tier (Base / MK-IV / MK-V).
- **Radial Research Tree:** Over 60+ nodes on a radial tree spanning six discipline branches.
- **Deep Prestige Mechanics:**
  - *Schematics*: Per-run prestige currency.
  - *Patents*: Meta currency that survives every publish.
  - *Legacy Marks*: Endgame currency that survives every reset.
- **Mastery:** Complete 21 patents, 14 challenges, 15 blueprints, and 8 exhibitions.
- **Achievements:** 79 earnables with progress bars and stacking bonuses.
- **Accessibility:** 100%-150% font scaling, reduced motion options, and a colorblind palette with strong hue/brightness separation.
- **Pure Tech Stack:** Vanilla HTML/CSS/JS, PWA capabilities, Web Audio, LocalStorage, and MIT licensed.

---

## Getting Started / Installation

Run the game locally — no installation, build step, or complex server required!

```bash
git clone https://github.com/Real-Fruit-Snacks/blueprint.git
cd blueprint

# Option 1: Open directly in any modern browser
open index.html

# Option 2: Run via local python server
python -m http.server 8000
# -> Navigate to http://localhost:8000
```

*Note: The service worker only registers over `http://` or `https://`, so opening directly via `file://` will work, but it won't cache for offline PWA use.*

---

## Usage

### Desktop Controls

- `Click`: Buy one machine
- `Shift + Click`: Buy ×10 (requires Bulk Buy research)
- `Shift+Alt + Click`: Buy ×100 (requires Bulk Buy research)
- `Ctrl+Shift + Click`: Buy ×1000 (requires Max Buy research)
- `Right-click`: Toggle auto-buy (requires Auto-Buy research)
- `Click + drag`: Pan research tree
- `Scroll wheel`: Zoom research tree

### Touch Controls

- `Tap`: Buy one machine
- `Long-press`: Open machine details
- `Tap A chip`: Toggle auto-buy
- `BUY MODE bar`: Bulk buy without modifier keys
- `Drag / pinch`: Pan / zoom research tree
- `Tap-to-arm + tap`: Confirm research node

---

## Architecture / File Structure

```
[Browser]
 index.html  ->  game.js  ->  sim-worker.js  (production loop)
                          ->  Web Audio API   (procedural sound)
                          ->  LocalStorage    (saves, base64 export)
                          ->  sw.js           (offline shell cache)
```

- **Render:** SVG + CSS for every visual — drafting grid, tier pips, flow connectors.
- **Sim:** `sim-worker.js` runs the production loop off the main thread.
- **Audio:** Web Audio API — synthesized on demand with absolutely no pre-recorded samples.
- **Saves:** LocalStorage — base64-encodable for easy export and cross-device transfer.
- **Offline:** Service worker (`sw.js`) utilizing a cache-first approach with background refresh.
- **Deploy:** Single-file static — every asset in the repository root ships as-is.

**Key patterns:** Every machine icon, research node, UI glyph, and sound is generated at runtime from SVG primitives — no external assets. Three prestige layers compose: Schematics reset on prestige, Patents survive publish, Legacy Marks survive every reset. The PWA shell installs from the GitHub Pages build (the itch embed can't register a service worker).

Tested on current Chrome, Firefox, Edge, Safari (desktop + mobile). Responsive down to ~360 px and handles iOS Safari viewport-chrome changes.

---

## Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on how to help improve the project. Be sure to also review our [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).

---

## License

This project is licensed under the [MIT License](LICENSE). See [CHANGELOG.md](CHANGELOG.md) for the full version history.
