# Landing Page

A single-file, conversion-optimized sales landing page for a 3-volume digital product.
Pure HTML + inline CSS + vanilla JS — no build step, no framework, no dependencies.
Open `index.html` in a browser, or drop it on any static host (Cloudflare Pages,
Netlify, Vercel, GitHub Pages).

## Design system

**Typography — Pairing 01**
- **Fraunces** (variable display serif) — headings, prices, brand, card titles
- **DM Sans** — body copy, UI labels, buttons, badges

**Color roles** — each color does one job, so the eye learns the page instantly:
| Color | Meaning | Where |
|---|---|---|
| **Red** | Urgency / time pressure | Top promo bar, "This price expires in" countdown |
| **Gold** | Value / buy | All CTAs, "Best Value" banner, corner stamps, featured card |
| **Black** (navy `#15293b`) | The price | The big `$27 / $47 / $97` numbers |
| **Blue / steel** | Brand & structure | Page background, nav brand, book covers |

The two single cards (Vault, Blueprint) are **white**; the featured "Complete Vault"
card has a **cream-gold** wash with matching gold bonus + equation panels, so it reads
as the recommended pick against the cool-blue page.

All colors live in the CSS `:root` block at the top of `index.html` — edit there to re-skin.

## What's inside (the conversion machinery)

| Section | Purpose |
|---|---|
| Sticky **urgency bar** | Live-viewer counter + countdown (session-based) |
| Sticky **nav** | Always-visible bundle CTA + price |
| Compact **hero** | Short on purpose so pricing cards sit near the fold |
| 3-card **offer** | Two singles + a scaled-up featured bundle, anchor pricing, `I+II+III` equation, bonus stack |
| **Story** | Placed *after* the offer to soften price reaction |
| **Countdown** | Mid-page deadline, synced to the top bar's timer |
| **Testimonials** | Social proof (replace with real reviews) |
| **FAQ** | Native `<details>` accordion, kills objections |
| **Reminder modal** | Fires at 2 min, downsell to the cheapest product |
| **Purchase toasts** | Rotating "X just bought" social proof |
| **Mobile sticky CTA** | Always-visible buy bar on phones |

## Customize

1. **Copy & meta** — search `index.html` for `TODO` and the `YOUR BRAND` / `Your Product` placeholders.
2. **Checkout links** — every CTA `href="#"` needs your real checkout URL (Hotmart, Stripe, Gumroad, etc.).
3. **Theme** — edit the CSS variables in `:root`.
4. **Book covers** — replace the `.cover-placeholder` divs with `<img src="images/vol1.jpg">` once you have artwork.

## Honesty note

The live-viewer counter, countdowns, and purchase toasts are **simulated** by default.
If you show them to real visitors, either wire them to real data or be aware that
fabricated scarcity/social-proof can be deceptive (and is regulated in many jurisdictions).
The testimonials are placeholders — replace them with real, verifiable ones before launch.
