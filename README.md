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
