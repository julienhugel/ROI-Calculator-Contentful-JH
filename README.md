# Contentful ROI Calculator

A Customer Success ROI calculator for Contentful — Calculator, Benchmarks and Scenario Analysis, with a **Quick Start** panel that produces a first estimate from just an industry + a few public facts.

Built with **Vite + React + TypeScript**. Deploys to **Vercel** with zero config.

## Local development

```bash
npm install
npm run dev      # http://localhost:5173
npm run build    # type-check + production build into dist/
npm run preview  # serve the production build locally
```

## Quick Start (intuitive first estimate)

The dark panel at the top of the Calculator lets a CSM:

1. Pick an **industry** (10 presets) and a **previous CMS**.
2. Enter **company name**, **annual revenue**, and **# brands on Contentful / total brands**.
3. Click **Apply presets & estimate** — salaries, % digital, content volumes, locales and agency spend are pre-filled from the industry preset.

Every pre-filled value can be refined in the sections below. Industry presets live in `src/lib/data.ts` (`INDUSTRY_PRESETS`).

## Deploy to Vercel

### Option A — Vercel CLI (fastest)

```bash
npm i -g vercel        # once
vercel login           # authenticate with your Vercel account
vercel                 # preview deploy
vercel --prod          # production deploy
```

### Option B — GitHub → Vercel dashboard

```bash
git init && git add -A && git commit -m "Contentful ROI calculator"
git remote add origin https://github.com/<you>/contentful-roi-calculator.git
git push -u origin main
```

Then in the Vercel dashboard: **Add New → Project → Import** the repo. Vercel auto-detects Vite; settings already provided in `vercel.json`:

- Framework: `vite`
- Build command: `npm run build`
- Output directory: `dist`

No environment variables required.
