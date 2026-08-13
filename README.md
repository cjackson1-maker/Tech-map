# 📍 Third-Party Tech Network Map

An interactive US map of all active third-party technicians, color-coded by Internal Rating with contact info, proximity search, and travel cost estimation.

**Live site:** https://cjackson1-maker.github.io/Tech-map/

---

## 🗺 Features

- **99 active techs** plotted across the US
- **Color-coded pins** by Internal Rating
  - 🔵 Blue = 1 – Top Technician
  - 🟢 Green = 2 – Good
  - 🟠 Amber = 3 – Needs Support
  - 🔴 Red = 4 – Struggling
- **Click any pin** for full contact card (name, company, phone, email, territory, notes)
- **Filter** by rating tier and territory (Central US, East Coast, West Coast)
- **Search** by name, company, city, or state
- **Find Nearest Techs** — enter any city, address, or ZIP to find the closest techs
- **Drive time estimate** based on distance + road factor
- **Travel cost** — one way and round trip at $0.76/mile
- Round trip cost flags 🔴 red when over $200
- **Excludes:** Do Not Use, No Longer Works, Moved to W-2, Connext, Veteranson

---

## 🔧 Tech Stack

- [Leaflet.js](https://leafletjs.com/) — interactive map
- [CartoDB Dark](https://carto.com/basemaps/) — map tile layer
- [OpenStreetMap Nominatim](https://nominatim.org/) — geocoding for proximity search
- Haversine formula — straight-line distance calculation
- All tech data embedded in HTML — no backend or database required
- Hosted via [GitHub Pages](https://pages.github.com/)

---

## 📋 Changelog

### v1.4 — August 2026
- Added favicon (blue map pin icon) to browser tab
- Reverted to original CartoDB Dark tile background

### v1.3 — August 2026
- Added v1.0 version badge to map header
- Added last updated date to header subtitle

### v1.2 — August 2026
- Added estimated drive time per tech (miles ÷ 55mph + 15% road factor)
- Added one way travel cost at $0.76/mile
- Added round trip travel cost at $0.76/mile x 2
- Round trip cost turns red with warning when over $200
- Fixed emoji rendering on Find Nearest button

### v1.1 — August 2026
- Added Find Nearest Techs proximity search by city, address, or ZIP
- Select Top 3, 5, or 10 results
- Dashed lines drawn from search point to nearest techs
- Results panel with ranked list, click to fly to tech on map

### v1.0 — August 2026 — Initial Launch
- 99 active techs plotted across the US
- Color-coded pins by Internal Rating
- Click pins for full contact card
- Filter by rating and territory, search by name/city/state
- Excludes inactive and Do Not Use techs
- Hosted on GitHub Pages

---

## 👤 Maintained by
cjackson1-maker
