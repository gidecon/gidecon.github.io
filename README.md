# gideon-bornstein.com

Personal academic website hosted on GitHub Pages with custom domain.

## Structure

```
index.html        # Single-page website (all HTML, CSS, JS in one file)
papers/            # PDF files for all papers and CV
headshot.png       # Profile photo
favicon.ico        # Browser tab icon
CNAME              # Custom domain config (add when DNS is ready)
```

## How to update

All updates are made by editing files in this repo and pushing to `main`. GitHub Pages auto-deploys on push (takes ~1 minute).

### Update a paper PDF

Replace the file in `papers/` with the new version, keeping the same filename:

```
papers/BP_IneQuality.pdf
papers/Bornstein_Entry_Aging.pdf
papers/Monopsony_Monetary_Policy.pdf
papers/Social_Insurance_Household_Debt.pdf
papers/Trade_Credit.pdf
papers/NLP_BornsteinPeter.pdf
papers/BKR_Oil_Market.pdf
papers/CTSD.pdf
papers/BBD_European_Debt.pdf
papers/CV_Gideon_Bornstein.pdf
```

Then commit and push:
```bash
git add papers/FILENAME.pdf
git commit -m "Update PAPER_NAME"
git push
```

### Update paper summaries, titles, or metadata

Edit `index.html`. Each paper is a `<div class="paper">` block. Summaries are inside `<div class="paper-abstract">`.

### Add a new paper

1. Add the PDF to `papers/`
2. Add a new `<div class="paper">` block in `index.html` under the appropriate section (`#working-papers`, `#publications`, or `#wip`)
3. Follow the existing pattern for title, meta, status, and abstract

### Update CV

Replace `papers/CV_Gideon_Bornstein.pdf` with the new version.

### Update headshot

Replace `headshot.png` with the new image (keep the same filename).

## Custom domain

The site uses the custom domain `gideon-bornstein.com`. This requires:
- A `CNAME` file in the repo root containing `gideon-bornstein.com`
- DNS A records at Google Domains pointing to GitHub Pages IPs:
  - 185.199.108.153
  - 185.199.109.153
  - 185.199.110.153
  - 185.199.111.153
- DNS CNAME record: `www` -> `gidecon.github.io`

## Features

- Dark/light mode toggle (top-right moon/sun icon)
- Responsive mobile layout (auto-activates below 768px)
- Hover-to-reveal abstracts on desktop, tap-to-toggle on mobile
- Coauthor photo carousel
- Seminar logo carousel
