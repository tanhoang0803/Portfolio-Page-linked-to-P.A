# Portfolio Version — Project Summary

## Overview
Two web projects built for a **Data Analyst portfolio**, both deployed to GitHub Pages under the account `tanhoang0803`.

---

## Project 1: Portfolio Page

| | |
|---|---|
| **Type** | Static HTML (single file, no build step) |
| **File** | `Portfolio Version/index.html` |
| **Live URL** | https://tanhoang0803.github.io |
| **GitHub repo** | https://github.com/tanhoang0803/tanhoang0803.github.io |
| **Stack** | HTML, Tailwind CSS (CDN), Google Fonts (Inter) |

### Run locally
```bash
cd "Portfolio Version"
npx serve . --listen 3000
# → http://localhost:3000
```

### Deploy
Auto-deploys via GitHub Actions on push to `main`.
Workflow: `.github/workflows/deploy.yml` (static upload, no build).

### Sections
- Hero (name, title, CTA)
- Stats (projects, years, tools)
- Featured Projects (Sales Analytics + 2 placeholder cards)
- Skills (Analytics & Data, Frontend & Viz, Tools & Workflow)
- Contact (email + GitHub)
- Footer

---

## Project 2: Product Sales Analytics Dashboard

| | |
|---|---|
| **Type** | React SPA |
| **Folder** | `Portfolio Version/product-sales-analytics/` |
| **Live URL** | https://tanhoang0803.github.io/product-sales-analytics/ |
| **GitHub repo** | https://github.com/tanhoang0803/product-sales-analytics |
| **Stack** | React 18, Recharts, Tailwind CSS, Vite, Lucide React |

### Run locally
```bash
cd "Portfolio Version/product-sales-analytics"
npm run dev
# → http://localhost:5173
```

### Build
```bash
npm run build   # outputs to /dist
```

### Deploy
Auto-deploys via GitHub Actions on push to `main`.
Workflow: `.github/workflows/deploy.yml` (build → upload dist → deploy Pages).
Vite base path set to `/product-sales-analytics/`.

### Features
- Product data input form (collapsible, validated)
- Auto-calculates: Revenue, Variable Cost, Total Cost, Gross Profit, Profit Margin, Break-even Units
- KPI Dashboard: Total Revenue, Total Gross Profit, Avg Margin, Top Product
- Revenue Trend line chart (monthly, Recharts)
- Profit Comparison bar chart (per product, Recharts)
- Sortable + filterable data table (search + category dropdown)
- Delete rows, Export to CSV
- 18 sample records (5 products × 3 months)

### Key files
| File | Purpose |
|------|---------|
| `src/App.jsx` | Root component, shared state |
| `src/utils/calculations.js` | Pure financial calculation functions (JSDoc) |
| `src/utils/csvExport.js` | CSV generation + browser download |
| `src/data/sampleData.js` | 18 dummy records |
| `src/components/ProductForm.jsx` | Add product form |
| `src/components/KPIDashboard.jsx` | KPI summary cards |
| `src/components/ChartsSection.jsx` | Line + Bar charts |
| `src/components/DataTable.jsx` | Sortable/filterable table |
| `src/components/Header.jsx` | Sticky header + export button |
| `src/index.css` | Tailwind directives + component classes |

### Financial formulas (see calculations.js)
```
Revenue             = unitsSold × unitPrice
Variable Cost       = unitsSold × unitCost
Total Cost          = variableCost + fixedCosts
Gross Profit        = revenue − totalCost
Profit Margin (%)   = (grossProfit / revenue) × 100
Break-Even (units)  = fixedCosts / (unitPrice − unitCost)
```

### Config notes
- `postcss.config.js` and `tailwind.config.js` use `module.exports =` (not `export default`) — no `"type": "module"` in package.json
- `vite.config.js` sets `base: '/product-sales-analytics/'` for GitHub Pages

---

## GitHub Account
- **Username:** tanhoang0803
- **Profile:** https://github.com/tanhoang0803
- **Email:** Hquoctan0803@gmail.com

## Deployment workflow
Both repos use GitHub Actions (`actions/deploy-pages@v4`).
Pages source must be set to **"GitHub Actions"** in each repo's Settings → Pages.
