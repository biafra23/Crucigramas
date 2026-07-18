# Crucigramas — Español fácil

Eine Progressive Web App (PWA) mit einfachen spanischen Kreuzworträtseln zum
Spanischlernen. Reines Vanilla-HTML/CSS/JS ohne Build-Schritt — die gesamte App
(Layout, Rätseldaten, Spiellogik) steckt in `index.html`.

## Dateien

- `index.html` — komplette App inkl. Styles, Rätseldaten und Spiellogik
- `sw.js` — Service Worker (Network-first mit Offline-Cache-Fallback)
- `manifest.webmanifest`, `icon-192.png`, `icon-512.png` — PWA-Manifest und Icons

## Deployment

Gehostet über GitHub Pages (Branch `main`, Root). Jeder Push auf `main`
veröffentlicht direkt.

## Versionsschema

Aktuelle Version: **v2.3-web**

Bei **jedem Release** müssen zwei Stellen synchron hochgezählt werden:

1. `index.html` — die Konstante `VERSION` (z. B. `const VERSION = "2.3-web";`)
2. `sw.js` — der Cache-Name `CACHE` (z. B. `const CACHE = "crucigramas-v2.3";`)

Das Hochzählen von `CACHE` ist zwingend, damit installierte Clients den alten
Service-Worker-Cache verwerfen und die neue Version laden.
