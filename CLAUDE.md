# Crucigramas — Español fácil

A Progressive Web App (PWA) with simple Spanish crossword puzzles for learning
Spanish. Plain vanilla HTML/CSS/JS with no build step — the entire app (layout,
puzzle data, game logic) lives in `index.html`.

## Language policy

Everything in this repo is in English (docs, code comments, commit messages,
repo description). The game itself — UI text, clues, word lists — is entirely
in Spanish.

## Files

- `index.html` — the complete app including styles, puzzle data, and game logic
- `sw.js` — service worker (network first with offline cache fallback)
- `manifest.webmanifest`, `icon-192.png`, `icon-512.png` — PWA manifest and icons

## Deployment

Hosted via GitHub Pages (branch `main`, root). Every push to `main` publishes
directly.

## Versioning scheme

Current version: **v2.5-web**

On **every release**, two places must be bumped in sync:

1. `index.html` — the `VERSION` constant (e.g. `const VERSION = "2.5-web";`)
2. `sw.js` — the cache name `CACHE` (e.g. `const CACHE = "crucigramas-v2.5";`)

Bumping `CACHE` is mandatory so that installed clients discard the old service
worker cache and load the new version.
