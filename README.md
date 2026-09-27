# Digital Agency

A minimalist, award-style **digital agency landing page** built with Next.js. Bold typography ("WE CREATE BEST DIGITAL PRODUCTS."), an animated gradient blob, and a spinning "DISCUSS THE PROJECT" CTA — a classic creative-studio hero layout.

Originally prototyped with [v0.app](https://v0.app).

## What it does

- Single-page agency landing with a light `#f8f8f8` canvas and black-on-white editorial aesthetic.
- Header: brand dots, EN language toggle, `CONTACT US` link, hamburger menu.
- Hero: oversized lightweight headline, animated pastel gradient blob (pink → orange → yellow, blurred, pulsing) behind the content, and a "DISCUSS THE PROJECT" outline button wrapped in a slow-spinning ring.
- Tagline section: "We create websites, applications, 3D design, motion design and animation."
- Purely presentational — no forms, no backend.

## Features

- Custom `animate-spin-slow` keyframe animation (spinning CTA ring)
- Animated gradient blob with `blur-3xl` + `animate-pulse`
- Light theme editorial layout; responsive spacing
- shadcn-style Button component

## Tech stack

- **Framework:** Next.js 15 (App Router) + React 19 + TypeScript
- **Styling:** Tailwind CSS, custom keyframes in `tailwind.config.js`
- **UI components:** Radix-backed `components/ui/*` (button)
- **Theming:** `next-themes` provider included
- Fully client-side — no API routes, no database

## Quick start

```bash
npm install        # or: pnpm install
npm run dev        # open http://localhost:3000
```

Production build:

```bash
npm run build
npm start
```

## Project structure

```
app/
  layout.tsx        Root layout, theme provider
  page.tsx          Agency landing page (header, hero, tagline)
  globals.css       Global styles
components/
  theme-provider.tsx
  ui/button.tsx     Button primitive
lib/
  utils.ts          Classname helpers
styles/globals.css  Legacy global stylesheet
public/             Placeholder images/logo
```

## Environment variables

None required. The site is fully client-side.

## Deployment

- **Static export ready:** no API routes or server actions, so it can be built as a static site. Set `output: "export"` in `next.config.mjs` and run `npm run build` to produce an `out/` directory.
- **GitHub Pages:** this repo ships with a `gh-pages` branch hosting the static export at `https://girishlade111.github.io/digital-agency/`.
- **Vercel:** also deployable as a standard Next.js app.
- Note: the header's `CONTACT US` link points to `/contact`, which is not implemented in this repo — wire it up to a real page or form before using the site in production.

---

Built by Girish Lade — [ladestack.in](https://ladestack.in)
