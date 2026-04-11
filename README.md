<div align="center">

<br>

<img src="https://img.shields.io/badge/version-0.9.2-1a6cff?style=flat-square&labelColor=0a2550" alt="Version">
<img src="https://img.shields.io/badge/status-live-10b981?style=flat-square&labelColor=0a2550" alt="Status">
<img src="https://img.shields.io/badge/license-MIT-94a3b8?style=flat-square&labelColor=0a2550" alt="License">
<img src="https://img.shields.io/badge/built%20with-Claude%20AI-7c3aed?style=flat-square&labelColor=0a2550" alt="Built with Claude">

<br><br>

# ClearSkies

### Aviation decoded. Instantly.

Plain-English briefings for METARs, TAFs, NOTAMs, SIGMETs, and ATC clearances.  
Route planning, airport dashboards, ATPL theory, and 7 pre-flight calculators — all in one file.

<br>

**[theskycrate.com](https://theskycrate.com)** · Built by aviation enthusiasts, for pilots.

<br>

---

</div>

<br>

## What it does

ClearSkies takes the cryptic shorthand of aviation data and turns it into structured, readable briefings in seconds. It covers every message type a pilot encounters:

| Input | What you get |
|---|---|
| `METAR LRCL 111130Z VRB04KT 9999 SCT070 11/M05 Q1017` | Wind, visibility, ceiling, QNH, flight category, AI weather narrative |
| `TAF EDDM 101100Z 1012/1118 27012KT...` | Forecast timeline with AI summary |
| `A1234/24 NOTAMN Q) EGTT/...` | Plain-English closure and restriction summary |
| `WSRO31 RJJJ 101200 SIGMET...` | Hazard type, altitudes, movement, pilot action |
| `SPEEDBIRD 123 CLEARED TO AMSTERDAM VIA WOTAN1F...` | What you were told, what to do, exact readback |

<br>

## Features

### Decoder
- Auto-detects METAR, TAF, NOTAM, SIGMET, and ATC clearances from a single input
- Structured cockpit-panel output with instrument strips (wind, visibility, ceiling, QNH, temp, time)
- Flight category classification (VFR / MVFR / IFR / LIFR) with colour coding
- Priority flags — HIGH / MODERATE / ROUTINE
- PDF export with ClearSkies branding
- Live METAR fetch by ICAO code
- Recent inputs dropdown, favourites strip

### Route Briefing
- Enter two ICAO codes → live METARs fetched for both airports
- Interactive Leaflet map with great-circle route and distance in NM / km
- AI en-route briefing: departure conditions, destination conditions, en-route considerations, go/no-go assessment

### Airport Dashboard
- Look up any of 85,000+ airports worldwide
- Live METAR auto-fetched and parsed into instrument grid
- Runway analysis with headwind and crosswind components per end
- Active runway recommendation auto-derived from live wind
- 3-hour weather trend with trend arrows (visibility, ceiling, QNH)
- Sunrise & sunset times (UTC) via NOAA algorithm
- Direct links to ChartFox (approach plates) and SkyVector (VFR/IFR charts)
- PDF export of full airport briefing

### ATPL Theory Q&A
- Ask any aviation theory question across all 14 ATPL subjects
- Structured answers with explanation, memory tip, and related topics
- Subject grid with one-click question starters

### Tools (7 calculators)
- **Runway Analysis** — best runway for current wind with crosswind limits
- **T/O & Landing Performance** — V-speeds and field length for A320, C172, PA-28
- **Weight & Balance** — CG calculation with envelope chart for C172S and A320
- **Fuel Planner** — ICAO-standard block fuel (trip + alternate + reserve + contingency)
- **Crosswind Calculator** — headwind and crosswind components from runway heading
- **Density Altitude** — pressure altitude corrected for non-standard temperature
- **Unit Converter** — QNH (hPa/inHg), altitude (ft/m), speed (kt/km/h), temperature (°C/°F)

<br>

## Tech stack

| Layer | Technology |
|---|---|
| Frontend | Vanilla HTML, CSS, JavaScript — single file, no framework |
| AI | [Claude](https://anthropic.com) (`claude-sonnet-4-20250514`) via Anthropic API |
| Proxy | Vercel serverless function (API key never exposed to browser) |
| Weather data | [aviationweather.gov](https://aviationweather.gov) — free, no key required |
| Airport data | [OurAirports](https://ourairports.com) — 85k+ airports, open data |
| Maps | [Leaflet](https://leafletjs.com) + OpenStreetMap |
| Icons | [Lucide](https://lucide.dev) |
| Hosting | GitHub Pages + custom domain |

<br>

## Changelog

### v0.9.2 — April 2026 *(current)*
- Route Briefing interactive map with great-circle route and NM distance
- Unified Decoder — METAR, TAF, NOTAM, SIGMET, and ATC in one input
- Full airport dashboard — live METAR, runway analysis, 3h trend, sunrise/sunset, charts links
- Mobile bottom navigation
- Branded PDF export for decoder and airport briefings
- Sunrise/sunset via NOAA algorithm
- Lucide icons throughout — no emoji UI elements
- Page transition animations
- Favourites strip with localStorage persistence
- Auto runway recommendation from live METAR wind
- QNH correctly displays hPa or inHg without conversion

### v0.9 — April 2026
- OurAirports CSV integration (85k+ airports, 47k+ runways)
- Live METAR fetch via Vercel proxy (CORS-safe on all devices)
- Route Briefing with AI en-route analysis
- ATPL Theory Q&A with subject grid
- Weight & Balance calculator with CG envelope chart

### v0.1–0.8 — April 2026
- Core METAR/NOTAM/TAF/SIGMET decoder
- Cockpit panel UI, dark/light mode, animated radar background
- Flight category classifier, glossary tooltips, priority badges
- Full landing page, pricing page, about page
- Tools suite (performance, fuel, crosswind, density altitude)

<br>

## Roadmap

- [ ] Go / No-Go assistant — structured fly/no-fly from weather + personal minimums
- [ ] Stripe payments + user accounts with saved decode history
- [ ] ATPL exam practice mode with question bank and scoring
- [ ] Batch decoder — up to 20 messages at once
- [ ] Shareable briefing links
- [ ] PWA — installable on iPhone/Android, tools available offline
- [ ] Rate limiting on proxy to prevent abuse

<br>

## Disclaimer

ClearSkies is for planning reference and educational purposes only. AI-generated briefings are advisory and must not be used as a substitute for official pre-flight sources. Always consult official NOTAMs, METARs, TAFs, and ATC communications through authorised channels before flight.

<br>

---

<div align="center">

Built with ♥ for aviation · [theskycrate.com](https://theskycrate.com)

</div>
