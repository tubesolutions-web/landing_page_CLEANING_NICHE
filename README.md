# Hidden Cleaning Hacks — Landing Page

A single-file, conversion-optimized sales landing page for a single ebook.
Pure HTML + inline CSS + vanilla JS — no build step, no framework, no dependencies.
Open `index.html` in a browser, or drop it on any static host (currently deployed to
GitHub Pages via `.github/workflows/static.yml`, on push to `main`).

## Design system

**Typography**
- **Playfair Display** — headings, prices, title, cover
- **Hanken Grotesk** — body copy, UI labels, buttons
- **Space Mono** — labels, stats, fine print, the cost-comparison "bill"

**Color roles**
| Color | Meaning | Where |
|---|---|---|
| **Cream** (`#f3ead7`) | Page background | Light sections |
| **Dark** (`#16130f`) | Contrast bands | Alternating dark sections, footer, sticky bars |
| **Green** (`#3c6d4a` / `#5fae7a`) | Brand accent / value | Eyebrows, prices, cover art, dividers |
| **Red** (`#b23a28`) | Action | All CTA buttons, urgency bar |

All colors live in the CSS `:root` block at the top of `index.html` — edit there to re-skin.

## What's inside (the conversion machinery)

| Section | Purpose |
|---|---|
| Sticky **top bar** | Launch price + evergreen countdown |
| Sticky **buy bar** | Appears once you scroll past the hero |
| **Hero** | Headline, CTA, SVG-drawn book cover (no image asset needed) |
| **Stat ribbon** | Formula count, room count, index, price |
| **The Math** | Cost-of-doing-it-the-usual-way vs. with the book, receipt-style |
| **Who Profits** | Why the cheap fix is never the one you hear about |
| **What's Inside** | The 9 rooms/problem areas + how the A–Z index works |
| **The Deal** | 5 trust vows — what this book won't do |
| **Reviews** | Social proof (replace with real reviews before launch) |
| **Offer** | Single price card, guarantee, payment badges |
| **FAQ** | Native `<details>` accordion |
| **Close + Footer** | Final CTA, brand, legal fine print |

## Customize

1. **Checkout link** — set `EBOOK_LINK` near the bottom of `index.html` to your real
   checkout URL (Hotmart, Stripe, Gumroad, etc.). Until it's set, every CTA points to `#`
   and won't take visitors anywhere.
2. **Cover art** — the hero cover is inline SVG (dark green gradient, title, stats). A
   standalone copy lives at `images/cover.svg` if you want it as a separate asset. Edit
   the text/colors directly in the SVG markup (appears in both places) to change it.
3. **Price / title** — search `index.html` for `$36` and `Hidden Cleaning Hacks` to
   rename or reprice; both appear in several places (hero, buy bars, offer card, FAQ).
4. **Analytics** — GA4 is wired in (`G-V1FE4DV5WL`), including CTA click tracking by
   placement (hero / sticky buy bar / offer card / close).
5. **Domain** — `CNAME` points this repo at `hiddenhomesecrets.com` via GitHub Pages.

## Honesty note

The top-bar countdown resets to a fresh ~24h window for every visitor, every day — it's
a simulated deadline, not a real one. The reviews are placeholders. Replace both with
real data before relying on them; fabricated scarcity/social proof can be deceptive and
is regulated in many jurisdictions.
