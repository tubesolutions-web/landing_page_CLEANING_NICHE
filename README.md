# Landing Page

A single-file, conversion-optimized sales landing page — same architecture as the
reference (`hidden-homestead-vault`). Pure HTML + inline CSS + vanilla JS. No build step,
no framework. Open `index.html` in a browser, or drop it on any static host
(Cloudflare Pages, Netlify, Vercel, GitHub Pages).

## What's inside (the conversion machinery)

| Section | Purpose |
|---|---|
| Sticky **urgency bar** | Live-viewer counter + countdown (session-based) |
| Sticky **nav** | Always-visible bundle CTA + price |
| Compact **hero** | Short on purpose so pricing cards sit near the fold |
| 3-card **offer** | Two singles + a scaled-up featured bundle, anchor pricing, `I+II+III` equation, bonus stack |
| **Story** | Placed *after* the offer to soften price reaction |
| **Countdown** | Mid-page deadline reinforcement |
| **Testimonials** | Social proof (replace with real reviews) |
| **FAQ** | Native `<details>` accordion, kills objections |
| **Reminder modal** | Fires at 2 min, downsell to the cheapest product |
| **Purchase toasts** | Rotating "X just bought" social proof |
| **Mobile sticky CTA** | Always-visible buy bar on phones |

## Customize

1. **Copy & meta** — search the file for `TODO` and the `YOUR BRAND` / `Your Product` placeholders.
2. **Checkout links** — every CTA `href="#"` needs your real checkout URL (Hotmart, Stripe, Gumroad, etc.).
3. **Theme** — edit the CSS variables in `:root` at the top of `<style>` to re-skin the whole page.
4. **Book covers** — replace the `.cover-placeholder` divs with `<img src="images/vol1.jpg">` once you have artwork.
5. **Fonts** — Cinzel (headings), Crimson Pro (body), Inter (UI), loaded from Google Fonts.

## Honesty note

The live-viewer counter, countdowns, and purchase toasts are **demo / simulated** by default.
If you display them to real visitors, either wire them to real data or be aware that fabricated
scarcity/social-proof can be deceptive (and is regulated in many jurisdictions). The testimonials
are placeholders — replace them with real, verifiable ones before launch.
