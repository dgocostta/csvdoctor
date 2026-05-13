# CSVDoctor

> The CSV file you'd never push to production. Free, browser-only CSV quality check.

Drop a CSV, get a full diagnostic on missing values, duplicates, type mismatches, date-format chaos, casing inconsistencies, and invalid emails. Download a cleaned version and a markdown report. Everything runs in the browser — no file ever leaves the user's machine.

**Live:** _(add your URL here after deploy)_

## Why this exists

I spent two years at Ipsos building data validation frameworks across 15+ datasets and reduced downstream errors by 25%. CSVDoctor is that work, productised: a one-click version of the kind of quality check that every analyst, ops person, and data engineer ends up writing from scratch.

## Stack

- Static HTML / CSS / vanilla JS — no framework, no backend
- [PapaParse](https://www.papaparse.com/) for CSV parsing (loaded from CDN)
- Hosted on Vercel
- Zero data collection

## Run locally

```bash
# Just open it
open index.html

# Or serve it
python3 -m http.server 8000
# → http://localhost:8000
```

## Deploy to Vercel

1. Push this repo to GitHub
2. Import the repo at [vercel.com/new](https://vercel.com/new)
3. Framework preset: **Other** (it's a static site)
4. Build command: _(leave empty)_
5. Output directory: _(leave empty — uses repo root)_
6. Deploy

That's it. Vercel will redeploy on every push to `main`.

## Roadmap

- [x] v0 — browser-only quality check + cleaned CSV download
- [ ] v1 — Excel multi-sheet support, JSON, larger files
- [ ] v1 — saved profiles, user accounts (Supabase)
- [ ] v1 — Stripe Pro tier (€19/mo)
- [ ] v2 — scheduled monitoring on Drive/S3 folders, Slack alerts
- [ ] v2 — dbt test export, Airflow operator

## Built by

[Rohit Yadav](https://rohityadav.ie) — Data Engineer, Dublin.
[GitHub](https://github.com/nameisrohit) · [LinkedIn](https://www.linkedin.com/in/rohit-s-yadav/)

## License

MIT
