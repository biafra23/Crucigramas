# Crucigramas — Español fácil

Einfache spanische Kreuzworträtsel zum Spanischlernen, als Progressive Web App
(PWA) — offline nutzbar und auf dem Homescreen installierbar.

**▶ Spielen: https://biafra23.github.io/Crucigramas/**

## Technik

Reines Vanilla-HTML/CSS/JS ohne Build-Schritt. Die gesamte App steckt in
`index.html`; `sw.js` sorgt als Service Worker für Offline-Betrieb
(Network-first mit Cache-Fallback).

## Entwicklung

Details zu Projektstruktur und Versionsschema stehen in [CLAUDE.md](CLAUDE.md).
Jeder Push auf `main` wird automatisch über GitHub Pages veröffentlicht.
