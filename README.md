# Positioning Landing Page — Limited to Limitless™

Built from **LtL Positioning — Wireframe Plan** (landing outline 1b + build spec 1c).
Single self-contained page. Just open `index.html` in a browser to view.

```
lisa-positioning-landing/
├── index.html              ← the landing page
└── assets/
    ├── infinity-mark.jpg   ← glass infinity mark (hero, nav, final CTA)
    └── ltl-badge.png       ← "Limited to Limitless" seal (footer)
```

## Sections (matches the plan, A–J)
Sticky nav · Hero · Reality check · My IP reframe · My lane (Do/Don't) ·
Positioning band · About Lisa · How it works · Results · Final CTA · Footer.

Design tokens are taken verbatim from the spec: ground `#000012`, panel `#0C1526`,
teal `#1FA9A9` (structure), amber `#F2A03D→#E8641E` (hero), body `#F0F0F0`, labels `#A8A8A8`.
Fonts: **Archivo** (display) + **Inter** (body). One accent per zone. No light backgrounds.

## ⚠️ 1 placeholder left to fill before this goes live
1. **Photo of Lisa** — the "About Lisa" section has a grey placeholder box.
   Drop a headshot into `assets/` and point the `.photo` block at it.

## ✅ Hero title
Eyebrow "Limited to Limitless™" over the amber headline **"LISA MURPHY, MBA"**.
Browser tab title: *Lisa Murphy, MBA — Limited to Limitless™*.

## ✅ Booking wired up
All 3 CTAs (nav, hero, final) open your Google Calendar booking page in a new tab:
`https://calendar.app.google/v1Wxp8zg28MouuAQ6`

## Goal + offer name (confirmed)
The single action is **book a diagnostic call**. The call is named **"Diagnostic call"**
across all three CTAs (nav, hero support, final). The button verbs stay emotional
("Find the leak" / "Fix the bottleneck") while "diagnostic call" is the calm, clear name
underneath. Can be elevated to a branded **"The Diagnostic"** later once traffic is warmer.

## Copy note
All wording uses your real fragments from the plan (pull signal, IP reframe, lane,
positioning statement, results). Nothing invented — no fake testimonials, no new tagline.
The `33–150%` and margin/time results come straight from the plan; confirm they're the
numbers you want public.

## SEO / GEO / AEO (added)
Domain baked in everywhere: **https://keynotesbylisa.limitedtolimitless.com/**
(lowercase canonical; your `KeynotesByLisa` QR resolves to the same place — domains
are case-insensitive).

**In `index.html`:**
- Meta description, robots (`index,follow,max-image-preview:large`), author, theme-color
- Canonical URL + favicon / apple-touch-icon (the infinity mark)
- Open Graph tags (Facebook, LinkedIn, iMessage previews) + Twitter/X card
- JSON-LD structured data — Organization, Person (*Lisa Murphy, MBA*), WebSite, WebPage
  (this is what Google rich results and AI answer engines read)
- **FAQ section** (visible accordion, above the final CTA) + matching **FAQPage** schema —
  6 on-brand Q&As drawn from your positioning; answer text mirrors the visible copy verbatim
  (Google's requirement). Strong AEO signal for AI answer engines.

**Root files (must deploy at the site root, not inside a folder):**
- `robots.txt` — allows all crawlers + explicitly welcomes AI engines (GPTBot,
  PerplexityBot, ClaudeBot, Google-Extended, Applebot, CCBot…); points to the sitemap
- `sitemap.xml` — the homepage URL
- `llms.txt` — plain-language summary for LLMs (who Lisa is, her IP, the offer, the CTA)

### ⚠️ Two things that MUST match for SEO to work
1. **Deploy to exactly `keynotesbylisa.limitedtolimitless.com`** — the same address as
   your printed QR code. Every canonical/social/sitemap URL points there.
2. Keep `robots.txt`, `sitemap.xml`, `llms.txt` at the **root** so they resolve at
   `/robots.txt`, `/sitemap.xml`, `/llms.txt`.

### Nice-to-have later
- A dedicated **1200×630 share image** (right now social previews reuse the square
  infinity mark — it works, but a purpose-built banner looks sharper).

## To publish
GitHub → Vercel → Cloudflare (your standard stack). Upload this folder to a repo,
connect it to Vercel, and point the `keynotesbylisa` subdomain at it via Cloudflare.
Happy to walk you through it click-by-click when you're ready.
