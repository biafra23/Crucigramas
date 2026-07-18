# Crucigramas — Español fácil

Simple Spanish crossword puzzles for language learners, built as a Progressive
Web App (PWA) — works offline and can be installed to the home screen.

**▶ Play: https://biafra23.github.io/Crucigramas/**

## Tech

Plain vanilla HTML/CSS/JS with no build step. The entire app lives in
`index.html`; `sw.js` is a service worker providing offline support
(network first with cache fallback).

## Development

See [CLAUDE.md](CLAUDE.md) for the project structure and the versioning scheme.
Every push to `main` is published automatically via GitHub Pages.
