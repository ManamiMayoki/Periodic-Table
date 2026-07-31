# Periodic Table: A Dual-Architecture Periodic Table

> An interactive exploration of the chemical elements, built twice — once as a lightweight 2D grid, once as an immersive 3D spatial environment — to compare two very different approaches to data visualization on the web.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=black)
![Three.js](https://img.shields.io/badge/Three.js-black?logo=three.js&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind_CSS-38B2AC?logo=tailwind-css&logoColor=white)

---

## 📖 Table of Contents

- [The Dual-Architecture Concept](#-the-dual-architecture-concept)
- [Tech Stack & Architecture](#️-tech-stack--architecture)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Design Philosophy & UX](#-design-philosophy--ux)
- [Recommended GitHub Topics](#️-recommended-github-topics)
- [Why a Monorepo](#-why-a-monorepo)

---

## The Dual-Architecture Concept

This project was built to explore the boundaries of data visualization on the web, comparing traditional DOM manipulation with hardware-accelerated 3D spatial rendering — using the same underlying dataset in both cases.

### 1. The Classic Stack (`/classic-2d`)

A production-ready, ultra-lightweight rendering of the periodic table using semantic HTML, responsive CSS Grid layouts, and vanilla JavaScript.

- **Focus:** Core Web Vitals, accessibility (a11y), instantaneous load times, and clean semantic structure.
- **Styling:** Modern, minimalist visual language with smooth CSS transitions and premium micro-interactions.

### 2. The Immersive Stack (`/spatial-3d`)

A hardware-accelerated, interactive 3D environment that transforms data parsing into a spatial experience. Built on React, Three.js, and React Three Fiber.

- **Focus:** Advanced graphics programming, dynamic camera orchestration, spatial UI/UX design, and smooth frame-rate optimization.
- **Styling:** High-end, premium dark aesthetic utilizing glowing materials, particle fields, and immersive orbital navigation.

---

## Tech Stack & Architecture

### Classic 2D Implementation

| Layer | Technology |
|---|---|
| Structure | Semantic HTML5 |
| Styling | Vanilla CSS3 (Custom Properties, Flexbox, CSS Grid) |
| Logic | Modern Vanilla JavaScript (ES6 Modules, Fetch API for dynamic data parsing) |

### Spatial 3D Implementation

| Layer | Technology |
|---|---|
| Framework | React 19 (Vite) |
| 3D Engine | Three.js |
| React Wrapper | React Three Fiber (`@react-three/fiber`) |
| Component Ecosystem | React Three Drei (`@react-three/drei`) |
| Animation | Framer Motion / GSAP (for seamless UI transitions) |
| Styling | Tailwind CSS |

---

## Features

- **Dynamic Data Filtering** — Filter elements instantaneously by group, period, block (s, p, d, f), and state of matter across both architectures.
- **Comprehensive Data Modals** — Detailed inspection panels showing atomic mass, electron configuration, electronegativity, melting points, and historical discovery context.
- **Advanced 3D Layouts (Spatial View):**
  - **Table Layout** — the classic grid translated into a 3D plane.
  - **Sphere Layout** — elements mapped onto a pristine spherical matrix.
  - **Helix Layout** — a continuous spiral tracking elements by ascending atomic number.
  - **Grid Layout** — a spatial block grouping elements by electron subshells.
- **Responsive Mechanics** — Fluid breakpoints ensuring seamless interaction across mobile, tablet, and high-resolution desktop displays.

---

## Project Structure

```text
├── classic-2d/               # Vanilla HTML/CSS/JS Project
│   ├── index.html            # Main entry point
│   ├── src/
│   │   ├── js/                # Element data parsing and DOM logic
│   │   └── css/                # Minimalist layout and animations
│   └── data/                  # Periodic table dataset (JSON format)
│
├── spatial-3d/                # React + Three.js Project
│   ├── src/
│   │   ├── components/         # Reusable 3D objects & layout controls
│   │   ├── hooks/               # Custom React hooks for data parsing
│   │   ├── styles/               # Tailwind and global layout setups
│   │   ├── App.jsx                # Canvas configuration and scene controller
│   │   └── main.jsx                # React app mounting layer
│   ├── package.json               # Dependency management
│   └── vite.config.js             # Build configuration
```

---

## Getting Started

### Prerequisites

Make sure you have [Node.js](https://nodejs.org/) installed on your machine (LTS version recommended).

### Running the Classic 2D Stack

No installation required. Navigate into the folder and serve the HTML file using any local web server (e.g., the Live Server extension in VS Code):

```bash
cd classic-2d
# Open index.html in your preferred browser,
# or run it through a local dev server for module support
```

### Running the Spatial 3D Stack

Navigate to the React application, install dependencies, and start the Vite development server:

```bash
cd spatial-3d
npm install
npm run dev
```

The app will be available at `http://localhost:5173` by default.

**Building for production:**

```bash
npm run build
npm run preview
```

---

## Design Philosophy & UX

The user interface follows a modern, dark-themed, premium architectural aesthetic.

- **Typography:** Clean, highly legible sans-serif pairings optimized for data density.
- **Color Systems:** Muted, elegant color palettes marking elemental categories, moving away from overly saturated traditional chemistry charts to achieve a refined digital interface.
- **Performance:** 3D instances use highly efficient instanced meshes where possible to keep draw calls low and sustain a consistent 60 FPS on modern hardware.

---

## Recommended GitHub Topics

Add these tags to your repository so it's easier to discover:

`react` · `threejs` · `react-three-fiber` · `vanilla-js` · `css-grid` · `data-visualization` · `webgl` · `frontend`

---

## Why a Monorepo

Keeping both codebases under a single repository makes this an effective portfolio piece — anyone reviewing it can click through both folders and directly compare vanilla JavaScript fundamentals against advanced React / Three.js capabilities, all in one place.

---

<p align="center">Built to explore where DOM-based UI ends and spatial computing begins.</p>