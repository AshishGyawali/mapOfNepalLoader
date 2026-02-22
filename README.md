# 🇳🇵 Nepal Map Loader

A beautiful, lightweight loading screen featuring an animated SVG map of Nepal. The map fills from left to right as loading progresses, with a glowing outline and shimmer particle effects — all built with pure HTML, CSS, and JavaScript. **Zero dependencies.**

![Nepal Map Loader Preview](preview.gif)

---

## ✨ Features

- **SVG Nepal Map** — Real geographic outline of Nepal rendered as an SVG path
- **Left-to-Right Fill Animation** — Map fills progressively based on loading percentage, clipped precisely to the map boundary
- **Animated Glowing Outline** — Stroke draw animation with a neon glow effect
- **Shimmer Particles** — Floating particles add depth and visual polish
- **Smooth Fade Out** — Loader gracefully fades away once loading completes
- **Pure HTML/CSS/JS** — No frameworks, no libraries, no build tools
- **Lightweight** — Single file, under 5KB total
- **Easy to Integrate** — Drop it into any project with simple `show`/`hide` API functions

---

## 🚀 Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/AshishGyawali/nepal-map-loader.git
cd nepal-map-loader
```

### 2. Open in browser

Simply open `index.html` in any modern browser:

```bash
open index.html
```

That's it — no build step, no installation required.

---

## 📦 Integration

### Drop into your project

Copy the loader HTML, CSS, and JS into your project. Use the built-in API to control it:

```javascript
// Show the loader
showNepalLoader();

// Hide the loader (e.g., after data finishes loading)
hideNepalLoader();
```

### With dynamic loading progress

If you have real loading progress (e.g., from an API or asset loader), update the fill directly:

```javascript
const fillRect = document.getElementById('fillRect');
const MAP_VIEWBOX_WIDTH = 60;

function updateProgress(percent) {
    const fillWidth = (percent / 100) * MAP_VIEWBOX_WIDTH;
    fillRect.setAttribute('width', fillWidth);
}

// Example: set to 50%
updateProgress(50);
```

---

## 🎨 Customization

| What | Where | Default |
|---|---|---|
| **Fill color** | `fill` attribute on `#fillRect` | `rgba(233, 69, 96, 0.35)` |
| **Outline color** | `.map-outline` stroke in CSS | `#e94560` |
| **Glow color** | `.map-glow` stroke in CSS | `rgba(233, 69, 96, 0.15)` |
| **Background** | `.loader-overlay` background in CSS | `#1a1a2e` |
| **Loader size** | `.nepal-loader` width/height in CSS | `420px × 320px` |
| **Loading speed** | `setInterval` delay in JS | `50ms` |
| **Particle count** | `.shimmer-particles .p` divs in HTML | `6` |

## 🌐 Browser Support

| Browser | Supported |
|---|---|
| Chrome | ✅ |
| Firefox | ✅ |
| Safari | ✅ |
| Edge | ✅ |
| Opera | ✅ |

Works in all modern browsers that support SVG, CSS animations, and `clipPath`.

---

## 🙏 Acknowledgments

- Nepal map outline sourced from [Natural Earth](https://www.naturalearthdata.com/) / OpenStreetMap GeoJSON datasets
- Inspired by creative SVG loading animations

---

<p align="center">
  Made with ❤️ for Nepal 🇳🇵
</p>
