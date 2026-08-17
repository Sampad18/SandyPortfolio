# Sannidhi Nayak — Portfolio Site

A static, dark-themed portfolio site (plain HTML/CSS/JS, no build step) styled after deepikarao.co.in — numbered project list, serif/sans type pairing, metrics-driven case studies.

## Structure

```
site/
├── index.html          Home — hero, selected work (4 projects), gallery, timeline, contact
├── about.html           About + contact
├── work/
│   ├── medium.html       Flagship case study — Medium, Antenatal Wellness Toolkit (MRes thesis)
│   ├── ventrimon.html     VentriMon — Non-Invasive ICP Monitoring
│   ├── canopy.html        Canopy — Insurance App
│   └── dualpulse.html     DualPulse — Mobile Gaming Device
├── css/style.css
├── js/main.js            mobile nav toggle + scroll-reveal animation
└── assets/
    ├── portfolio/         images extracted from Portfolio_Sannidhi Nayak_2026.pdf
    └── medium/             images extracted from the Medium/Antenatal Wellness Toolkit PDF
```

## Preview locally

From this `site/` folder:

```
python3 -m http.server 8000
```

Then open http://localhost:8000 in a browser.

## Deploy to Vercel

**Option A — CLI (fastest):**

```
cd site
npx vercel          # first run: log in, confirm project settings (framework: "Other")
npx vercel --prod    # promote to your production URL
```

**Option B — GitHub + Vercel dashboard:**

1. Push this `site/` folder (or the whole repo, setting `site` as the Vercel "Root Directory") to a GitHub repo.
2. In vercel.com → **Add New Project** → import the repo.
3. Framework preset: **Other**. No build command needed — it's static.
4. Deploy.

Either way, no environment variables or build step are required — it's plain static files.

## Content source

Copy and images are sourced directly from:
- `Portfolio_Sannidhi Nayak_2026.pdf`
- `Medium - Antenatal Wellness Toolkit - Sannidhi Nayak - MRes Healthcare and Design 2026.pdf`

To swap in different imagery later, replace files in `assets/portfolio/` or `assets/medium/` and update the `<img src>` paths referencing them.
