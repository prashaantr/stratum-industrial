# STRATUM — Industrial intelligence

An original heavy-industry website combining Palantir-inspired photographic panels, Mercury-inspired calm composition and rounded controls, a purple palette, and Cognite-inspired industrial subject matter.

**Live site:** https://stratum-industrial-pr.fey-auk-0538.chatgpt.site

## Run

```sh
python3 -m http.server 4173 --directory dist
```

Open http://localhost:4173. No build, install, framework, API keys, or backend required.

## Features

- Responsive cinematic stock-photo hero and floating navigation
- Keyboard-accessible topic carousel with previous/next controls
- Three industry tabs with changing images and content
- Native disclosure panels
- Interactive asset maintenance demo with per-asset session review state
- Self-hosted fonts and imagery, reduced-motion support, skip link and visible focus

## Design reuse

Read `DESIGN.md`, `PRODUCT.md`, and `docs/AGENT-PROMPT.md`. The latter is a complete prompt to turn the actual implementation into a reusable design skill. Source of truth is `dist/styles.css`, `dist/index.html`, and `dist/app.js`.

## Files

- `dist/` — complete deployable website, tracked as source
- `docs/AGENT-PROMPT.md` — handoff prompt for extracting a design skill
- `docs/ASSETS.md` — stock photo provenance and licensing
- `DESIGN.md` — implemented design rules
- `PRODUCT.md` — scope, assumptions, and user direction
- `.openai/hosting.json` — Sites deployment identity

## Honest boundaries

STRATUM is a fictional brand and design demonstration, not an operating industrial software company. Data and workflows are illustrative. No form submits or industrial systems are connected. Review state resets when the page reloads. No customer logos, invented testimonials, or performance claims are included.

No affiliation with Palantir, Mercury, or Cognite. Those sites are visual references only. Original source code is MIT licensed; photography and fonts retain their respective licenses.
