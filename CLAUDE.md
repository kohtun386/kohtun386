# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

GitHub profile repo (`kohtun386/kohtun386`), forked from the `thmsgbrt/thmsgbrt` "self-updating README" starter. The auto-generation pipeline is **disabled** — `README.md` is now hand-authored profile content. The legacy generator code remains in the tree but is dormant.

## Commands

- `npm install` — install dependencies (`dotenv`, `mustache`, `node-fetch`, `puppeteer`).
- `node index.js` — runs the legacy README generator. **Do not run this casually**: it Mustache-renders `main.mustache` into `README.md`, overwriting the hand-written profile. Requires a `.env` with `OPEN_WEATHER_MAP_KEY`.
- No test suite (`npm test` is a stub that exits 1) and no lint script. Formatting is via Prettier config: `npx prettier --write <file>`.

## Architecture

**Current state — hand-authored profile.** Update `README.md` directly. Its content describes the user's other projects (Factory ERP, Shadow Thesis Factory, POS-system, Vibe Code Tours), which live in separate repos and are not part of this one.

**Legacy generation pipeline (dormant):**
- `.github/workflows/main.yaml.disabled` — was the CI: ran on push to `master` and every 3 hours, executed `node index.js`, then committed the regenerated README. Disabled by renaming the file.
- `index.js` — the orchestrator. Fetches Stockholm weather from OpenWeatherMap (needs `OPEN_WEATHER_MAP_KEY`), scrapes the latest Instagram posts, then renders `main.mustache` into `README.md`.
- `services/puppeteer.service.js` — a singleton `PuppeteerService` that launches Chrome and scrapes `picuki.com` for `.post-image` image srcs. Launches with a hardcoded third-party proxy (`--proxy-server=http=194.67.37.90:3128`).
- `main.mustache` — the upstream starter's template, still referencing the original author's content (Stockholm, @visitstockholm, Thomas Guibert's projects). It does not match the current profile.

`.env.example` documents the only env var the generator needs. `.prettierrc.yaml` and `.vscode/settings.json` define formatting (2-space indent, single quotes, 110 print width, format-on-save).

## Gotchas

- Restoring `main.yaml.disabled` or running `node index.js` replaces the hand-authored README.md with the legacy template output — the two are not equivalent, so only do this if the generation pipeline is being intentionally resurrected.
- The puppeteer scraper targets a third-party site through a hardcoded proxy; treat it as fragile legacy code.
