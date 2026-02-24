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
