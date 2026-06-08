# QuickTools — your automated tool-site asset

A fast, zero-maintenance website of free utilities people search Google for every day.
It's pure static HTML/CSS/JS — no server, no database, no upkeep. Once it's live it runs
itself. Income comes from ad slots and affiliate links that are already wired in; it scales
with how many visitors find the site through search.

## What's inside
```
quicktools/
├── index.html                 # homepage (links every tool)
├── assets/style.css           # shared design system
├── tools/
│   ├── tip-calculator.html
│   ├── loan-calculator.html
│   ├── percentage-calculator.html
│   ├── bmi-calculator.html
│   ├── password-generator.html
│   └── word-counter.html
├── sitemap.xml                # for Google
└── robots.txt
```
Each tool is its own page = its own entry point in Google search. More tools = more ways in.

## 1. Preview it locally
From this folder:
```
py -m http.server 8000
```
Then open **http://localhost:8000** in your browser. Everything works offline.

## 2. Put it online for free (GitHub Pages)
You already have Git + GitHub set up. Steps:
1. Create an empty repo on GitHub named **`quicktools`** (https://github.com/new, leave it empty).
2. I (or you) push this folder to it.
3. On GitHub: **Settings → Pages → Source: Deploy from branch → `main` / root → Save.**
4. In ~1 minute your site is live at `https://YOURNAME.github.io/quicktools/`.

That URL is your free, permanent, automated website. (Optional: buy a custom domain later —
ad networks approve custom domains far more easily than github.io subdomains.)

## 3. Turn on the money (after it's live)
The ad slots and SEO are already built in. To monetize:

- **Affiliate links (works immediately, no approval):** add relevant affiliate links inside
  the `.seo` content blocks — e.g. a password-manager referral on the password page, a
  high-yield-savings referral on the loan page. Sign up free at Amazon Associates,
  Impact, or ShareASale.
- **Display ads (needs traffic + approval):** once you have steady visitors, apply to
  **Google AdSense** or **Ezoic**. Paste their script tag where each page says
  `<!-- AdSense: paste your script tag here -->` and replace the `.ad-slot` placeholders.

> Honest note: ad/affiliate income scales with visitors. The asset is built; the growth lever
> is traffic. See "Grow traffic" below.

## 4. Grow traffic (the one ongoing lever — optional, automatable)
- **Submit your sitemap** to Google Search Console (free) so Google indexes every tool.
- **Add more tools.** Each new page targets a new search term. Copy any tool file, change the
  logic + the `<title>`/`<meta>`, and add a card to `index.html` + a line to `sitemap.xml`.
- Ideas with strong search demand: unit converter, age calculator, QR-code generator,
  discount/sale calculator, time-zone converter, GPA calculator, date calculator.

I can build any of these on request — the more tools, the more traffic, the more income.

## 5. Before going live: replace placeholders
- Swap `https://example.com/` in `sitemap.xml`, `robots.txt`, and each page's `<link rel="canonical">`
  with your real URL.
- That's it — the site is otherwise complete.
