# Sardinia Dream — Luxury Travel & Villa Portfolio

[![Vite](https://img.shields.io/badge/Vite-6.x-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vite.dev/)
[![Sass](https://img.shields.io/badge/Sass-1.88+-CC6699?style=for-the-badge&logo=sass&logoColor=white)](https://sass-lang.com/)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

A high-performance, visually immersive landing platform showcasing luxury holiday villas, custom booking forms, backgrounds, and real images gatherd from private boating experiences across Sardinia. 

This platform prioritizes raw speed, eliminating modern framework overhead by pairing a lightning-fast **Vite** bundler with a scalable, production-grade **7-1 Sass layout engine** and vanilla ES6+ JavaScript components.

---

## 🚀 Architectural Overview

The project relies on clean engineering fundamentals to deliver instantaneous page transitions, highly structured style rules, and frictionless asset compilation:

* **Vite Dev Server & Bundling Engine:** Leverages native ES modules (ESM) over HTTP to provide near-instantaneous Hot Module Replacement (HMR) during local development, compiling down into hyper-optimized, minified asset sheets for production.
* **7-1 Sass Software Architecture:** The layout layer avoids the chaotic pitfalls of single-sheet styles by compartmentalizing design tokens into distinct, encapsulated Sass components (`_button.scss`, `_card.scss`, `_popup.scss`) unified through a central compilation entry point.
* **Encapsulated Vanilla JavaScript UI:** Interactive components (such as modular lightboxes, feature boxes, state counters, and custom map interfaces) are managed natively via standalone JS modules to maintain zero runtime library bloat.

---

## 🛠️ Stack Deep Dive

### CSS Engineering & Sass Architecture
The stylesheets follow the industry-standard **7-1 Pattern**, managing visual assets across dedicated semantic subdirectories:
* **Abstracts:** Defines foundational structural tokens (`_variables.scss`), functional tools (`_functions.scss`), and reusable mixin configurations (`_mixins.scss`) for responsive design handling.
* **Base:** Sets the global document defaults, raw typography styling matrices, custom keyframe `@keyframes` templates (`_animations.scss`), and non-intrusive layout helpers.
* **Components:** Encapsulates self-contained design UI blocks—ranging from functional backgrounds (`_bg-video.scss`), navigation primitives (`_button.scss`), media elements (`_story.scss`), and user-interactive prompt layers (`_popup.scss`).
* **Layout & Pages:** Manages layout skeletons (`_grid.scss`, `_navigation.scss`) alongside viewport-specific presentation layers (`_home.scss`).

### Asset Pipelines & Module Compiles
* **Parallel SASS Compiles:** The workflow detaches manual style generation by using active filesystem listeners (`sass --watch`), mapping the nested Sass architecture down directly into a single, clean browser-readable layout sheet (`src/style.css`).
* **Optimized Static Asset Delivery:** High-fidelity background streams, local photography vectors, and SVG maps are cached, hashed, and processed by Vite to prevent visible layout shift or excessive initial block transfers.

---

## 📂 Project Structure

```text
├── sass/                    # 7-1 Architecture Source Files
│   ├── abstracts/           # Mixins, global design variables, and utilities
│   │   ├── _functions.scss
│   │   ├── _mixins.scss
│   │   └── _variables.scss
│   ├── base/                # Reset rules, core typography, and animations
│   │   ├── _animations.scss
│   │   ├── _base.scss
│   │   ├── _typography.scss
│   │   └── _utilities.scss
│   ├── components/          # Reusable UI component blocks
│   │   ├── _bg-video.scss   # Hero background video styling
│   │   ├── _book.scss       # Booking section UI
│   │   ├── _button.scss     # Global button designs & hover states
│   │   ├── _card.scss       # Villa & experience display cards
│   │   ├── _composition.scss# Image layout clusters
│   │   ├── _feature-box.scss# Highlights & selling points layout
│   │   ├── _form.scss       # Input fields & custom validation states
│   │   ├── _map.scss        # Interactive location layouts
│   │   ├── _popup.scss      # Detail lightboxes and modal elements
│   │   └── _story.scss      # Customer review layouts & video masks
│   ├── layout/              # Structural scaffolding
│   │   ├── _footer.scss
│   │   ├── _grid.scss       # Float or flex-based layout grids
│   │   ├── _header.scss
│   │   └── _navigation.scss # Fullscreen overlay or dropdown menus
│   ├── pages/               # Page-specific style sheets
│   │   └── _home.scss       # Home landing page configuration
│   └── main.scss            # Master stylesheet entry point (imports all partials)
├── src/                     # Application Source Code
│   ├── counter.js           # Numeric state counter module
│   ├── javascript.svg       # Language branding indicator asset
│   ├── main.js              # Central JavaScript entry point
│   ├── style.css            # Compiled vanilla CSS stylesheet
│   └── style.css.map        # Source map for cross-referencing Sass in browser DevTools
├── img/                     # Compressed image directory
├── public/                  # Static raw public assets (favicon, raw streaming media)
├── index.html               # Main application document structure
├── package.json             # Manifest of project scripts and development tools
└── vite.config.js           # Optional Vite engine bundle overrides
```

## ⚙️ Local Development Setup

Follow these steps to configure your local workspace, initialize the parallel compiler, and start working on the source files:

### 1. Clone & Install Dependencies
Ensure you have Node.js 18+ installed on your computer before proceeding.

```bash
git clone [https://github.com/TheWerbinator/sardinia-dream.git](https://github.com/TheWerbinator/sardinia-dream.git)
cd sardinia-dream
npm install
```

### 2. Launch the Ecosystem
To work on the site with live browser syncing and active Sass tracking, you will need to open two terminal windows or run them concurrently:

**Terminal 1: Spin up the Vite Dev Server**
This handles your HTML, JavaScript modules, and launches the hot-reloading browser preview.
```bash
npm run dev
```
Local Preview URL: http://localhost:5173 (or the port displayed in your terminal).

**Terminal 2: Initialize the Sass Compiler**
This actively watches your sass/ directory files and continuously generates the compiled browser-ready stylesheet.
```bash
npm run watch:sass
```
Now, any changes made to your `.scss` or `.js` source code files will instantly update your browser view without manual page refreshes.

## 🛠️ Script Reference

The tasks configured inside `package.json` manage your entire development and deployment workflow:

| Script | Command | Functional Purpose |
| :--- | :--- | :--- |
| `dev` | `vite` | Boots the development ecosystem with near-instantaneous HMR. |
| `watch:sass` | `sass --watch sass/main.scss src/style.css` | Tracks workspace Sass changes and compiles them down into standard CSS. |
| `build` | `vite build` | Compiles, hashes, and minifies production code into a deployable `/dist` directory. |
| `preview` | `vite preview` | Provisions a local production server environment to test build builds locally. |

## 🚀 Building and Deploying

When your adjustments are ready for production, execute the build pipeline:

```bash
npm run build
```
