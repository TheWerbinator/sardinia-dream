# Sardinia Dream

Marketing and booking site for a luxury Sardinia stay-and-charter experience: island stays, private boat charters, and a custom booking form. Built as a fast static site with real photography from the trips.

## Stack

- Vite (dev server + bundler)
- Sass 1.88+ (7-1 architecture)
- Vanilla ES6+ JavaScript
- HTML5

No framework. The interactive pieces (lightboxes, counters, maps) are small vanilla JS modules, so the site ships as static files with no runtime dependency.

## Features

- Custom booking form
- Image galleries with lightboxes
- Interactive location maps
- Background video and animated counters
- Customer reviews

## Structure

```text
sass/            # 7-1 Sass architecture
  abstracts/     # variables, functions, mixins
  base/          # reset, typography, animations
  components/    # buttons, cards, forms, popups
  layout/        # header, footer, grid, navigation
  pages/         # page-specific styles
src/             # compiled CSS + JS
img/             # images
public/          # static assets
```

## Local development

```bash
git clone https://github.com/TheWerbinator/sardinia-dream.git
cd sardinia-dream
npm install
```

Run two processes:

```bash
npm run dev         # Vite dev server at http://localhost:5173
npm run watch:sass  # recompile Sass on change
```

Scripts:

- `dev` runs the Vite dev server
- `watch:sass` recompiles Sass on change
- `build` outputs a production build to `/dist`
- `preview` serves the production build locally

## Deploy

Static output. Run `npm run build` and deploy `/dist` to any static host (Vercel, Netlify, GitHub Pages).
