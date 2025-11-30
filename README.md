# Mehrdad Salehi · Personal Website

Fully dynamic site powered by **Vite + React + TypeScript + Tailwind + shadcn/ui**. It mirrors the design in `imitationsite/` with reusable sections (Hero, About, Research, Projects, Experience, Teaching, Achievements, Skills, Contact) populated from the CV/SOP highlights.

## Tech stack

- Vite 5 + React 18 + TypeScript
- TailwindCSS with a custom design token layer
- shadcn/ui + Radix primitives for accessible components
- React Router (for future multi-page growth)

## Project structure

```
site/
├── public/           # Static files served as-is (.nojekyll, robots, CV assets)
├── src/
│   ├── components/   # Section + UI components
│   ├── pages/        # route-level components
│   ├── hooks/lib/    # shared utilities
│   └── main.tsx      # React entry
├── index.html        # Vite entry file (mounts React app)
├── package.json      # npm / bun scripts & deps
└── README.md         # You are here
```

## Getting started

```bash
cd site
npm install          # or pnpm install / bun install
npm run dev          # launches Vite dev server on http://localhost:5173
```

## Production build & preview

```bash
npm run build        # outputs static assets to dist/
npm run preview      # serves the production build locally
```

## Deploying to GitHub Pages

1. Push this folder to any GitHub repo (e.g., `<username>.github.io`).
2. Build the site: `npm run build`.
3. Publish the `dist/` directory via GitHub Pages (Actions workflow provided in `.github/workflows/deploy.yml`).
	- The supplied workflow builds on every push to `main` and deploys automatically.

## Customization checklist

- Drop the latest CV PDF and headshots into `public/` or `src/assets/` and update links (e.g., `/MehrdadCV.pdf`).
- Replace the Formspree endpoint in `Contact.tsx` if you use another contact service.
- Edit section copy inside the React components—each section is data-driven so it’s easy to swap content or add new cards.
- Tailor colors/spacing in `src/index.css` (design tokens) or extend Tailwind config as needed.

## Next ideas

- Wire in a blog or publications feed using MDX.
- Add analytics (Plausible, GoatCounter) by dropping the script into `index.html`.
- Internationalize the content with `react-i18next` if you need another language.
