# Benc.AI — Foundational Financial Infrastructure for the AI Agent Era

A high-performance, pixel-perfect static web application showcasing **Benc.AI**, the autonomous economic layer and financial gateway engineered for artificial general intelligence (AGI) and machine-to-machine transactions.

---

## 📑 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [Design & Typography System](#-design--typography-system)
- [Interactive Canvas Engines](#-interactive-canvas-engines)
  - [1. 3D Fibonacci Particle Globe](#1-3d-fibonacci-particle-globe)
  - [2. Dotted Vector Map & Curved Data Arcs](#2-dotted-vector-map--curved-data-arcs)
- [Tech Stack](#-tech-stack)
- [Getting Started](#-getting-started)
- [File Structure](#-file-structure)
- [Configuration & Customization](#-configuration--customization)
- [Browser Compatibility](#-browser-compatibility)
- [License](#-license)

---

## 🌟 Overview

Benc.AI provides decentralized identification (DID RFC-402 standards), low-latency model inference routing, autonomous payment rails, and trustless multi-agent settlement. 

This website faithfully recreates the minimalist editorial aesthetic, warm beige background palettes, custom vector geometries, and interactive mathematical canvas animations seen on the official platform.

---

## ✨ Key Features

- **Real-Time Scrolling Ticker**: Smooth CSS marquee animation highlighting supported LLM engines (`DeepSeek-R1-Flash`, `GLM-4.5-Flash`, `Qwen2.5-Coder-32B`, `MiniCPM-o-2.6`). Pauses on hover.
- **Header & Navigation**: Sticky blur bar with navigation dropdowns, mobile hamburger drawer, language switcher, and rapid console access triggers.
- **Hero & Query Interface**: Interactive agent query input with predefined quick tags and responsive focus states.
- **Editorial Beige Showcase (`01 / Agent id`)**: Three-column structured feature matrix with custom inline SVG geometric glyphs representing agent economic identities, API gateways, and developer toolkits.
- **Interactive 3D Sphere Section**: Fibonacci-distributed particle globe rendered at 60 FPS on HTML5 Canvas with full drag-and-rotate physics and touch controls.
- **Global Network Topology Map**: Procedural continent dot matrix with real-time Bezier curved data links sending animated transaction pulses between global financial hubs.
- **Modal Integrations & Toast Feedback**: Zero-dependency modal system for Web3 wallet connection and API key provisioning, backed by dynamic animated toast notifications.
- **Zero Build Tooling Required**: Ships as a single self-contained file with no `npm install`, Webpack, or Vite compilation required.

---

## 🎨 Design & Typography System

The interface pairs classic editorial serif styling with ultra-clean modern sans-serif typography:

| Token | Family / Value | Usage |
|---|---|---|
| **Display Serif** | `Instrument Serif`, `Newsreader`, Georgia | Primary editorial titles, section heads, brand serif mark |
| **Sans Serif** | `Inter`, system-ui | Interface text, pills, navigation, buttons, numbers |
| **Beige Base** | `#f5f2eb` | Primary card container background |
| **Beige Dark** | `#eeeae0` / `#e6dfcf` | Feature card surfaces & icon plates |
| **Obsidian** | `#111111` / `#0a0a0a` | Action buttons, ticker background, text headers |
| **Dark Charcoal** | `#0f0f11` | Enterprise footer |

---

## 🧮 Interactive Canvas Engines

### 1. 3D Fibonacci Particle Globe
Implemented on `#globeCanvas` without heavyweight 3D dependencies (like Three.js).
- **Mathematical Distribution**: Utilizes the golden ratio angle $\phi = \pi \times (3 - \sqrt{5})$ to plot 850 equidistant points on a spherical surface.
- **Projection & Depth Shading**: Applies 3D rotation matrices around the X and Y axes, sorted via the painter's algorithm to calculate depth-based size and opacity ($Z$-indexing).
- **Inertia & Touch Physics**: Supports drag interaction with mouse move listeners and multi-touch mobile events.

### 2. Dotted Vector Map & Curved Data Arcs
Implemented on `#mapCanvas`.
- **Procedural Dot Grid**: 80 $\times$ 40 dot grid filtered against bounding continent coordinate algorithms to draw lightweight vector landmasses.
- **Quadratic Bezier Flight Arcs**: Calculates quadratic curves ($P_0, P_1, P_2$) connecting San Francisco, London, Frankfurt, Tokyo, Singapore, and Sydney to the central AGI hub, animating packets with continuous time parameters ($t \in [0, 1]$).

---

## 🛠 Tech Stack

- **Markup**: Semantic HTML5 (Single File Architecture)
- **Styling**: [Tailwind CSS v3 CDN](https://tailwindcss.com/) with extended color palettes and font families
- **Typography**: [Google Fonts](https://fonts.google.com/) (`Inter`, `Newsreader`, `Instrument Serif`)
- **Icons**: [Lucide Icons CDN](https://lucide.dev/)
- **Graphics**: Native HTML5 2D Canvas API (Zero WebGL/Three.js overhead)
- **Interactivity**: Vanilla JavaScript (ES6+)

---

## 🚀 Getting Started

No build step or dependencies need to be installed.

### Option 1: Direct Browser Launch
Simply double-click `index.html` or drag it into any modern web browser (Chrome, Safari, Firefox, Edge, Brave).

### Option 2: Run via Local Server (Recommended)
Running through a local web server ensures optimal font caching and smooth canvas rendering:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js npx
npx serve .

# Using PHP
php -S localhost:8000
```

Once running, navigate to:
```
http://localhost:8000/index.html
```

---

## 📁 File Structure

```text
.
├── index.html        # Complete standalone web application (HTML, CSS, and JS)
└── README.md         # Architecture, design guidelines, and usage documentation
```

---

## ⚙️ Configuration & Customization

### Modifying Globe Density & Rotation
Locate the particle configuration inside `index.html`:
```javascript
let globeRadius = 140;     // Radius multiplier of the 3D sphere
const numPoints = 850;      // Total particles on the sphere
let angleX = 0.2;           // Initial tilt angle
let angleY = 0;             // Horizontal rotation speed
```

### Modifying Map Nodes
You can add or update geographical coordinates in the `globalNodes` array:
```javascript
const globalNodes = [
  { x: 0.19, y: 0.36, label: "San Francisco" },
  { x: 0.49, y: 0.28, label: "London" },
  { x: 0.82, y: 0.38, label: "Tokyo" }
];
```

---

## 🌐 Browser Compatibility

| Browser | Status |
|---|---|
| Google Chrome 90+ | Fully Supported (60+ FPS Canvas) |
| Apple Safari 14+ | Fully Supported (Hardware accelerated) |
| Mozilla Firefox 88+ | Fully Supported |
| Microsoft Edge 90+ | Fully Supported |
| Mobile Safari & Chrome | Fully Supported (Touch drag & gesture support) |

---

## 📄 License

Distributed under the MIT License. Feel free to use, modify, and distribute this codebase for educational and commercial purposes.
