# 📍 Third-Party Tech Network Map

An interactive US map of all active third-party technicians and vendor companies, color-coded by Internal Rating with contact info, proximity search, travel cost estimation, coverage radius, gap analysis, vendor layer with workorder-based coverage areas, multi-site planning, and a full tech management workflow.

**Live site:** https://cjackson1-maker.github.io/Tech-map/

---

## 🗺 Features

### Map & Pins
- **99 active techs** plotted across the US
- **Color-coded pins** by Internal Rating
  - 🔵 Blue = 1 – Top Technician
  - 🟢 Green = 2 – Good
  - 🟠 Amber = 3 – Needs Support
  - 🔴 Red = 4 – Struggling
- **Click any pin** for full contact card — name, company, phone, email, territory, travel radius, notes
- **Work order history** shown in each popup — job count and states worked, pulled from Salesforce report
- **Excludes:** Do Not Use, No Longer Works, Moved to W-2, Connext (individual), Veteranson (individual)

### Vendor Layer
- **6 vendors mapped** with color-coded square pins matching their coverage circles
  - 🟢 Green = Site Services Now (46 states, 1,133 work orders)
  - 🔵 Blue = Connext (23 states, 177 work orders)
  - 🟠 Amber = Techlink Services LLC (23 states, 86 work orders)
  - 🔴 Red = Progressive Technologies Inc
  - 🟣 Purple = Veteranson Low Voltage (5 states, 33 work orders)
  - 🟡 Yellow = VGI Technology (Texas, 2 work orders)
- **Coverage radius circles** — dashed circles drawn over every state each vendor has worked in, sourced from Salesforce workorder report
- Vendor popup shows: coverage type, total work orders, states covered, and linked techs
- Click any linked tech name in vendor popup to fly to their pin on the map
- **🏢 Vendors button — 3-click cycle:**
  - Click 1 → Vendors ✓ — vendor pins + coverage circles alongside tech pins
  - Click 2 → Only ▌▌ — tech pins hide, vendors and coverage areas only
  - Click 3 → Off — resets to full tech map

### Filters & Search
- Search by name, company, city, or state
- Filter by territory (Central US, East Coast, West Coast)
- Rating filter buttons (All, Top Tech, Good, Support)
- Live badge counts update as filters are applied

### Coverage Tools
- **⊙ Radius** — toggle each individual tech's preferred travel range as a dashed circle
- **⚠ Gap Analysis** — side panel grading every US state: No Coverage (red), Low Coverage (amber), Covered (green). Updates live with active filters

### Find Nearest Techs
- Enter any city, address, or ZIP code
- Select Top 3, 5, or 10 results
- Map zooms to show search location + nearest techs with dashed lines
- Results panel shows drive time, one-way cost, and round-trip cost at $0.76/mile
- Round-trip cost flags 🔴 red when over $200
- Click any result card to fly to that tech on the map

### 🌐 Multi-Sites Planner
- Add multiple school or site locations by name, address, city, or ZIP
- Each site gets a unique numbered colored pin on the map
- Finds Top 5 nearest techs per site with drive time, miles, one-way and round-trip cost
- Click any tech row to fly to their pin on the map
- **Show on Map** — drops all site pins with dashed lines to nearest tech and zooms to fit
- **Export to CSV** — downloads full planner results (site, tech, drive time, cost) for sharing or scheduling
- Sits on the same bar as Find Nearest Techs for quick access

### Tech Management (Admin)
- **+ Add Tech** — submit new techs with vendor association and Salesforce link for review
- **✎ Suggest an Edit** — propose updates to any existing tech from their pin popup
- **📋 Review** (🔒 Admin only) — approve or reject pending submissions
- **⬇ Export to CSV** (🔒 Admin only) — download approved changes formatted for Salesforce import
- Review queue persists across browser sessions

### Other
- **? Help** — full in-app how-to guide with 6 tabbed sections
- **v1.9 badge** visible in header
- Favicon in browser tab

---

## 🔧 Tech Stack

- [Leaflet.js](https://leafletjs.com/) — interactive map rendering
- [CartoDB Dark](https://carto.com/basemaps/) — map tile layer
- [OpenStreetMap Nominatim](https://nominatim.org/) — geocoding for proximity search and multi-site planner
- Haversine formula — straight-line distance calculation
- localStorage — pending review queue persists across sessions
- Salesforce workorder report — source for tech job history and vendor state coverage
- All tech data embedded in HTML — no backend or database required
- Hosted via [GitHub Pages](https://pages.github.com/)

---

## 📋 Changelog

### v1.9 — August 2026
- Added **🌐 Multi-Sites Planner** — add multiple school/site locations and find nearest techs for each
- Each site gets a unique numbered colored pin with dashed line to nearest tech
- Top 5 nearest techs shown per site with drive time, one-way and round-trip cost
- Export planner results to CSV for scheduling and sharing
- Multi-Sites button placed on the Find Nearest bar for quick access
- Button renamed from Job Sites → Multi-Sites

### v1.8 — August 2026
- Vendor pin colors now match their coverage circle color
- Vendor popup header shows color swatch and matching colored text
- Single **🏢 Vendors** button cycles through: Off → Show with techs → Vendors only
- Removed separate "Only" button — merged into single 3-state cycle button
- Purple "Vendors Only Mode" banner appears at top of map in vendor-only mode

### v1.7 — August 2026
- Removed vetting status from vendor layer
- Added vendor-only toggle mode
- Vendor pins now show job count directly on the pin
- Vendor popup states sourced from actual Salesforce workorder report
- Added **work order history** to every individual tech popup

### v1.6 — August 2026
- Added **Vendor Layer** — 6 vendor companies mapped with square color-coded pins
- Coverage radius circles per vendor state based on workorder history
- Added Vendor Association field to Add New Tech form

### v1.5 — August 2026
- Added **Coverage Radius** toggle for individual techs
- Added **Gap Analysis** panel
- Added **+ Add New Tech** and **✎ Suggest an Edit** workflow
- Added **📋 Review Panel** (admin only) with approve/reject and CSV export
- Added **? Help** button with 6-tab in-app guide
- Admin password protection on Review Panel and Export

### v1.4 — August 2026
- Added favicon to browser tab
- Reverted to original CartoDB Dark tile background

### v1.3 — August 2026
- Added version badge and last updated date to header

### v1.2 — August 2026
- Added estimated drive time and travel cost (one-way + round-trip at $0.76/mile)
- Round-trip cost flags red when over $200
- Fixed emoji rendering on Find Nearest button

### v1.1 — August 2026
- Added **Find Nearest Techs** proximity search
- Results panel with ranked list and click-to-fly

### v1.0 — August 2026 — Initial Launch
- 99 active techs plotted across the US
- Color-coded pins by Internal Rating
- Filter by rating and territory, search by name/city/state
- Hosted on GitHub Pages

---

## 👤 Maintained by
cjackson1-maker
