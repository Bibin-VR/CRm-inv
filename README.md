# Sai Samarth CRM — Inventory & Project Desk

**A single-page CRM/inventory tool for Sai Samarth Engineering**, covering projects,
customers, purchasing, and electrical-store inventory in one dashboard.

[Live site](https://bibin-vr.github.io/CRm-inv/)

Runs entirely client-side — no backend, no build step. Inventory data is seeded from
the shop's electrical store spreadsheet and held in the browser via `localStorage`.

## Modules

| Desk | Covers |
|---|---|
| **Command Dashboard** | Ongoing project control, priority queue, inventory risk, purchase watch, management signals |
| **Projects** | Project desk, ongoing work tracking |
| **Inventory** | Stock levels, add material, use material, extract material from BOM |
| **Customers** | Customer desk |
| **Purchase** | Purchase desk, purchase order tracking |
| **Management** | Team utilization, approval queue, operational KPIs |

## Stack

Plain HTML/CSS/JavaScript, with [SheetJS](https://sheetjs.com/) (`xlsx.full.min.js`)
bundled locally to read the seed spreadsheet.

## Running locally

No build step — open `index.html` directly in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

## Deployment

Deployed as a static site via GitHub Pages (`.github/workflows/pages.yml`) on every push
to `main`.

## Data source

`inventory_data.js` is seeded from `ELECTRICAL STORE 13 2.xlsx` — the shop's electrical
store inventory spreadsheet, included in the repository.
