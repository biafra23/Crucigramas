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

Current version: **v2.8-web**

On **every release**, two places must be bumped in sync:

1. `index.html` — the `VERSION` constant (e.g. `const VERSION = "2.6-web";`)
2. `sw.js` — the cache name `CACHE` (e.g. `const CACHE = "crucigramas-v2.6";`)

Bumping `CACHE` is mandatory so that installed clients discard the old service
worker cache and load the new version.

## Development workflow

Every change follows this flow before it lands on `main`:

1. Develop on a feature branch, never directly on `main`.
2. Verify the change end-to-end in a headless browser against the real page
   (not just by reading the code).
3. Run an internal "no memory" code review: reviewers with no knowledge of
   the authoring session (fresh subagents) review the branch diff from
   independent angles (correctness, removed behavior, cross-references,
   reuse, simplification, efficiency, altitude, conventions), findings are
   adversarially verified, and confirmed findings are fixed and re-verified
   before opening the PR.
4. Open a pull request and subscribe to its activity.
5. Wait for reviews and address each review comment individually: reply
   in that comment's own thread (not with one summary comment) and push
   fixes to the same branch. The PR is done only when it is merged or
   closed.
