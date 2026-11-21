# FL-IDS Showcase

An interactive walkthrough of **Federated Learning-based Intrusion Detection System for SDN-enabled IoT Networks**
(Aaryan Prakash, Aaron B Ajay, Amal Roy, Amogh Krishna J S; Department of Computer Science & Engineering, BMS College of Engineering).

Live site: https://theaaryanprakash.github.io/FL-IDS-SDN/
Project code and run logs: https://github.com/TheAaryanPrakash/FL-IDS-SDN

## What is in it

- **Present**: 12 full-screen slides (arrow keys). Slide 3 is an animated network map of the whole system with four scenarios
  (a training round, cheating sites caught, an attack caught and blocked, a brand-new attack type), step-by-step controls and
  settings you can change. Clicking a part of the map zooms into an animated scene of that part.
- **Results**: one long page with every measured table and chart, for reading alone.
- Every number is copied from `PAPER_NOTES.md` section 8.15 of the FL-IDS-SDN repository and carries a tag saying how it was measured
  (for example "measured · full pool · 3 seeds" or "seed 42 only"). Animations are schematic, not measured timings.

All numbers live in one file, `src/data.js`.

## Build

```bash
npm install
npm run dev      # local preview
npm run build    # production build in dist/
```

The site is built and published to GitHub Pages by the workflow in `.github/workflows/pages.yml` on every push to `main`. The Vite `base` is `/FL-IDS-SDN/`, so the site is served under that path.

## Stack

React 18, Vite, GSAP (`gsap` and `@gsap/react`), hand-written SVG. Fonts: Space Grotesk, Inter and JetBrains Mono (bundled
through Fontsource, no external requests).

## Design and animation guidance used

Built with guidance from open skill collections that were downloaded and read before building (frontend-design, the GSAP React, timeline and performance skills, svg-animations, Emil Kowalski's animate skill and make-interfaces-feel-better):
frontend-design,
[greensock/gsap-skills](https://github.com/greensock/gsap-skills),
[supermemoryai/skills `svg-animations`](https://github.com/supermemoryai/skills),
[emilkowalski/skills](https://github.com/emilkowalski/skills),
[vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills),
[pbakaus/impeccable](https://github.com/pbakaus/impeccable) and
[jakubkrehel/make-interfaces-feel-better](https://github.com/jakubkrehel/make-interfaces-feel-better).

`vercel-labs/agent-skills` and `pbakaus/impeccable` were also downloaded but not applied in this build.
