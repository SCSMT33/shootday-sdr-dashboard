---
name: verify
description: Build/launch/drive recipe for verifying changes to the single-file SDR dashboard (index.html) end-to-end with Playwright.
---

# Verifying the SDR dashboard

Static single-file app — no build step. Serve the repo root and drive it with
the pre-installed Playwright + Chromium.

## Launch

```bash
(python3 -m http.server 8931 >/dev/null 2>&1 &)
```

## Drive

Global playwright is installed; resolve it with NODE_PATH:

```bash
NODE_PATH=/opt/node22/lib/node_modules node <script>.js
```

Script skeleton that gets a populated dashboard:

```js
const { chromium } = require('playwright');
const browser = await chromium.launch();
const page = await browser.newPage({ viewport: { width: 1500, height: 1100 } });
await page.goto('http://localhost:8931/index.html');
await page.setInputFiles('#fileInput', '<bookings CSV>');        // Airtable/bookings export
await page.waitForSelector('#summaryCards .card');               // dashboard is hidden until a CSV loads
await page.setInputFiles('#callsFileInput', '<aircall CSV>');    // optional, needed for speed-to-lead/call metrics
```

## Gotchas

- Chart.js loads from a CDN; in the sandboxed environment it fails
  (`Chart is not defined` pageerrors, canvases blank). Pre-existing —
  tables/cards/sections still render, so ignore it unless verifying charts.
- The dashboard persists uploads and settings in localStorage
  (`sdr_data`, `sdr_goals`, `sdr_mandate`, `sdr_funnel`, ...); reloads keep
  state within a browser context. Clear keys to test cold-start paths.
- Collapsible sections (Mandate, Sales Funnel, Commission, AE Baseline) are
  rendered even while collapsed — click their `.mandate-header`/title row to
  expand before screenshotting.
- Cross-check trick: the Sales Funnel (B2B mode) and the Mandate Scoreboard's
  Month-over-Month table compute leads/qualified/closed via independent code
  paths but identical definitions — their monthly numbers must match exactly.
