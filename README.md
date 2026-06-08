# 🪐 Planet Search Discovery

> Explore and visualize confirmed exoplanet data from NASA's Exoplanet Archive — filter by stellar parameters, orbital mechanics, and detection methods across 5,000+ confirmed worlds.

![NASA API](https://img.shields.io/badge/data-NASA%20Exoplanet%20Archive-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Version](https://img.shields.io/badge/version-1.0.0-amber)

---

## ✨ Features

- 🔭 **Live NASA data** — queries the Exoplanet Archive TAP service in real time
- 🔍 **Advanced filtering** — by mass, radius, orbital period, equilibrium temp, and detection method
- 📊 **Interactive charts** — HR diagrams, period-radius plots, discovery timelines
- 🌍 **Habitability score** — Earth Similarity Index (ESI) estimation per planet

---

## 🚀 Quick Start

```bash
# clone & install
git clone https://github.com/your-user/planet-search
cd planet-search
npm install

# start dev server
npm run dev
```

---

## ⚙️ Environment Variables

Create a `.env.local` file in the root:

```env
NEXT_PUBLIC_NASA_API_KEY=your_key_here
NEXT_PUBLIC_TAP_URL=https://exoplanetarchive.ipac.caltech.edu/TAP
```

Get a free NASA API key at [api.nasa.gov](https://api.nasa.gov).

---

## 🗄️ Data Source

All planetary data is sourced from the **[NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/)** cumulative KOI table via the IPAC TAP service. Includes Kepler, K2, TESS, and ground-based confirmed detections.

Example TAP query:

```sql
SELECT pl_name, pl_orbper, pl_rade, st_teff
FROM ps
WHERE default_flag = 1
ORDER BY disc_year DESC
```

### Key stats
| Metric | Value |
|--------|-------|
| Confirmed planets | 5,599+ |
| Host star systems | 4,182+ |
| Multi-planet systems | 857+ |

---

## 🛠️ Tech Stack

- [Next.js](https://nextjs.org) — framework
- [TypeScript](https://www.typescriptlang.org) — type safety
- [Supabase](https://supabase.com) — database & auth
- [React Query](https://tanstack.com/query) — data fetching
- [Recharts](https://recharts.org) — charts
- [Tailwind CSS](https://tailwindcss.com) — styling

---

## 📁 Project Structure

```
planet-search/
├── app/
│   ├── page.tsx          # home / search UI
│   ├── planet/[id]/      # planet detail page
│   └── api/              # route handlers
├── components/
│   ├── FilterPanel.tsx
│   ├── PlanetCard.tsx
│   └── charts/
├── lib/
│   ├── nasa.ts           # TAP API client
│   └── supabase.ts
└── types/
    └── exoplanet.ts
```

---

## 📜 License

MIT © Built with ☕ in Barcelona
