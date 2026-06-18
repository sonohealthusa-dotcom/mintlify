# SonoHealth — Full Project Context for New Chat

> Paste this file or reference it in your next session so Claude has full context of everything done so far. The Mintlify docs folder should be mounted at the same path.

---

## Who You Are

- **Name:** Dan
- **Email:** sonohealthusa@gmail.com
- **Company:** SonoHealth — US-based health technology company
- **Website:** https://sonohealth.com (recently migrated from WordPress/WooCommerce to Shopify)
- **Docs site:** https://docs.sonohealth.com (powered by Mintlify, repo at https://github.com/sonohealthusa-dotcom/mintlify)
- **Store credentials:** Google Top Quality Store badge, 4.7 stars, 659 verified Google reviews, ScamAdviser 100/100
- **Reviews platform:** Reviews.io (https://www.reviews.io/company-reviews/store/sonohealth-org-)
- **Google Store page:** https://www.google.com/storepages?q=sonohealth.com&c=US

---

## Products (5 product lines)

### 1. Spectrum 5 Magnesium Complex
- 5-in-1 marine-sourced magnesium (glycinate, malate, citrate, oxide, hydroxide) + Aquamin (72+ trace minerals)
- Price: $25 one-time / $21/month subscription
- Rating: 5.0 stars (34 Reviews.io reviews)
- GMP-certified, third-party tested, made in USA
- Buy: https://sonohealth.com/products/magnesium-complex-spectrum-5/
- Docs: https://docs.sonohealth.com/magnesium/overview

### 2. HeartBeats™ Fetal Doppler
- FDA-cleared (510(k)) home fetal heart rate monitor, 2.5 MHz probe
- Price: $69
- 2-year warranty, 60-day money-back guarantee
- Endorsed by Dr. Carolina Melgar, MD
- Buy: https://sonohealth.com/products/fetal-doppler/
- Docs: https://docs.sonohealth.com/fetal-doppler/overview

### 3. MistPro Portable Mesh Nebulizer
- FDA-approved vibrating mesh nebulizer, USB-C rechargeable, near-silent
- Price: $69
- Compatible with albuterol, budesonide, ipratropium, saline
- Buy: https://sonohealth.com/products/portable-mesh-nebulizer-respiratory-relief/
- Docs: https://docs.sonohealth.com/nebulizer/overview

### 4. AirPro HEPA 14 Air Purifier (NEW — just added)
- HEPA 14 + 3-stage filtration (Pre-Filter, HEPA 14 w/ Antibacterial Coating, Activated Carbon) + UV-C sterilization
- Captures 99.9% of particles down to 0.1 microns
- Room coverage: 430 sq ft in 10 min, 1,200 sq ft in 30 min
- Noise: 25–50 dB, Night Mode at 25 dB
- Smart features: lifetime filter tracking, 360° airflow, smart timer (2/4/6 hr), aromatherapy pad
- Price: $169 (1-pack) / $249 (2-pack) / $459 (4-pack)
- Replacement filters: $29.99-$79.99, or 20% off with subscription (every 90 days, includes lifetime warranty)
- Warranty: 2-year standard, lifetime with filter subscription
- Buy: https://sonohealth.com/products/air-pro-hepa-filter-air-purifier
- Replacement filters: https://sonohealth.com/products/airpro-replacement-filter-compatible-with-airpro-purifier
- Docs: https://docs.sonohealth.com/air-purifier/overview

### 5. Other Products (less documentation)
- BPpro Blood Pressure Monitor — $39
- BPMAX Blood Pressure Monitor (talking voice, for elderly) — $35
- Cowabunga Bovine Colostrum Powder
- BioBloom Vaginal Probiotics — $29
- PlastiqOff Detox
- Vitamin D3 + K2 Supplement
- KidIQ Brain Development

---

## What Was Done — Complete History

### Phase 1: Mintlify Docs Site Fixes
1. **Fixed duplicate h1 tags across 102 MDX files** — Mintlify frontmatter `title` auto-renders as h1, so we removed manual `# Heading` lines from the body of every file.
2. **Fixed missing blank lines after frontmatter** in all 102 files (the h1 removal regex consumed trailing newlines).
3. **Fixed MDX parse errors in 5 files (7 instances)** — Unescaped `<` characters in text like `<50%`, `<1 micron`, `TI < 1.0` were treated as JSX by MDX. Replaced with `&lt;`.
4. **Deleted rogue `docs.json`** — A bare `docs.json` created from the Mintlify dashboard was overriding the fully configured `mint.json`, causing missing sidebar navigation and wrong branding. Dan deleted it manually.
5. **Fixed root URL 404** — Added `"redirects": [{"source": "/", "destination": "/introduction"}]` to mint.json.

### Phase 2: AEO/GEO Research & Strategy
6. **Created comprehensive AEO audit** (`sonohealth-aeo-audit.html`) — HTML scorecard grading SonoHealth across: robots.txt, llms.txt, content quality, product schema, review schema, FAQ schema. Identified why competitor Forest Leaf gets recommended over SonoHealth (review volume 134 vs 34, AggregateRating schema present vs missing, lower price, better Bing indexing).
7. **Researched how AI platforms discover products** — ChatGPT uses Bing exclusively (not Google), Perplexity uses its own crawler + Bing, Gemini uses Google. AI agents don't verify individual reviews but use aggregate signals from third-party sources.
8. **Identified key AEO signals:** review volume (3.6x more for recommended products), authoritative list mentions (41%), awards (18%), third-party content cited 3x more than brand-owned.

### Phase 3: llms.txt for Shopify
9. **Created custom llms.txt content** for the Shopify store combining Shopify's default Universal Commerce Protocol (UCP) with SonoHealth's product catalog, trust signals, and docs links.
10. **Three llms.txt files exist in the repo:**
    - `llms.txt` — Docs site index (page-by-page listing of all 127 documentation pages)
    - `sonohealth-llms.txt` — Standalone product catalog for reference
    - `sonohealth-llms-combined.txt` — Combined Shopify UCP + product catalog (ready to install on Shopify as `llms.txt.liquid` or `llms-full.txt.liquid`)
11. **All product URLs updated** from WooCommerce `/product/` to Shopify `/products/` format.
12. **Not yet installed on Shopify** — Dan needs to create `llms.txt.liquid` or `llms-full.txt.liquid` in the Shopify theme editor. The safer approach is `llms-full.txt.liquid` to avoid overriding Shopify's default `llms.txt`.

### Phase 4: Social Proof Enhancement
13. **Updated 3 existing review pages** (`magnesium/reviews.mdx`, `nebulizer/reviews.mdx`, `fetal-doppler/reviews.mdx`) — Added "Third-Party Verification" sections with hardcoded text links to Reviews.io, Google Top Quality Store page, and ScamAdviser. These are readable by AI crawlers (unlike JavaScript widgets).
14. **Updated `introduction.mdx`** — Added AirPro product card (now 4-product grid) and new "Trust & Verification" section with Google Store, Reviews.io, and ScamAdviser links.

### Phase 5: AirPro Air Purifier Documentation (25 new pages)
15. **Created 25 MDX pages** in `air-purifier/` directory:
    - **Core (8):** overview, how-it-works, hepa-14-filtration, uv-c-sterilization, air-quality-guide, room-coverage, smart-features, filter-replacement
    - **Use cases (5):** allergen-removal, mold-protection, asthma-relief, for-bedrooms, for-pets
    - **Comparison & AEO (6):** vs-competitors, best-hepa-14-air-purifier, best-air-purifier-for-allergies, best-air-purifier-under-200, guarantee, buy
    - **FAQ & Support (4):** faq (20 Q&As), reviews (with social proof), troubleshooting, data (machine-readable)
    - **Common Questions (2):** questions/best-air-purifier-for-home, questions/hepa-14-vs-hepa-13
16. **Updated `mint.json` navigation** — Added AirPro section with full subgroup structure matching other products. Total: 127 pages across 5 navigation groups.
17. **Updated all 3 llms.txt files** with AirPro product entries.
18. **All changes pushed to GitHub and deployed successfully** — Verified live at docs.sonohealth.com.

---

## Current Mintlify Site Structure

```
docs.sonohealth.com/
├── introduction (landing page with 4 product cards + trust signals)
├── magnesium/ (34 pages — Spectrum 5 Magnesium Complex)
│   ├── overview, ingredients, science, magnesium-types-guide, ...
│   ├── benefits-sleep, benefits-muscle, benefits-stress, benefits-energy
│   ├── best-magnesium-complex, best-for-sleep-stress-cramps, ...
│   ├── faq, reviews (with social proof), data, troubleshooting
│   └── questions/ (3 common question pages)
├── fetal-doppler/ (27 pages — HeartBeats™ Fetal Doppler)
│   ├── overview, how-it-works, fda-clearance, safety, ...
│   ├── compare/ (3 competitor comparison pages)
│   ├── faq, reviews (with social proof), data, troubleshooting
│   └── questions/ (5 common question pages)
├── nebulizer/ (20 pages — MistPro Mesh Nebulizer)
│   ├── overview, how-it-works, mesh-vs-jet, fda-approval, ...
│   ├── faq, reviews (with social proof), data, troubleshooting
│   └── questions/ (2 common question pages)
├── air-purifier/ (25 pages — AirPro HEPA 14 Air Purifier) ← NEW
│   ├── overview, how-it-works, hepa-14-filtration, uv-c-sterilization
│   ├── allergen-removal, mold-protection, asthma-relief, for-bedrooms, for-pets
│   ├── best-hepa-14-air-purifier, best-air-purifier-for-allergies, best-air-purifier-under-200
│   ├── faq, reviews (with social proof), data, troubleshooting
│   └── questions/ (2 common question pages)
├── llms.txt (page index for AI crawlers)
├── sonohealth-llms-combined.txt (Shopify llms.txt content, ready to install)
└── sonohealth-aeo-audit.html (AEO scorecard)
```

Total: **127 MDX pages** + supporting files

---

## Key Technical Notes

### Mintlify MDX Rules
- Frontmatter `title` auto-renders as h1 — never add a manual `# Heading` in the body
- `<` must be escaped as `&lt;` (MDX treats `<` as JSX)
- `docs.json` overrides `mint.json` when both exist — never create docs.json
- Blank line required after frontmatter `---`
- Config file: `mint.json` (controls navigation, branding, colors, redirects)

### Shopify Notes
- URLs use `/products/` (plural), not `/product/` (singular) like WooCommerce
- Shopify generates a default `llms.txt` with UCP (Universal Commerce Protocol)
- Custom content should go in `llms-full.txt.liquid` (safer than overriding `llms.txt.liquid`)
- Shopify theme editor: Online Store → Themes → Edit code → Templates
- The combined file at `sonohealth-llms-combined.txt` is ready to paste into a Liquid template

### AEO/AI Crawler Notes
- ChatGPT Search uses Bing index exclusively (submit to Bing Webmaster Tools)
- AI crawlers cannot execute JavaScript (Reviews.io widgets invisible — use hardcoded text instead)
- Key bots to allow in robots.txt: GPTBot, OAI-SearchBot, ClaudeBot, Claude-SearchBot, PerplexityBot, Google-Extended
- Reviews.io is a Google-licensed review partner — reviews syndicate to Google Shopping
- Google Top Quality Store badge is a powerful trust signal for AI recommendations

---

## Pending / Not Yet Done

1. **Install llms.txt on Shopify** — The combined content (`sonohealth-llms-combined.txt`) needs to be placed in a Liquid template on Shopify. Recommended: create `llms-full.txt.liquid` in the Shopify theme editor (Templates section). Dan was trying to find where to create it.

2. **AggregateRating JSON-LD schema** — Product pages on sonohealth.com need `AggregateRating` in their Product schema markup. This is a major gap for AI recommendations.

3. **FAQPage JSON-LD schema** — Add structured FAQ schema to docs pages and/or product pages.

4. **Bing Webmaster Tools** — Submit sonohealth.com sitemap to Bing (critical since ChatGPT uses Bing exclusively).

5. **Grow review count** — Currently 34 Reviews.io reviews for Spectrum 5 vs. 134 for competitor Forest Leaf. Target 100+ reviews per product.

6. **AirPro reviews** — The AirPro is newer, so the reviews page currently shows store-level trust signals rather than product-specific reviews. Add product-specific reviews as they accumulate.

---

## Agent Traction (from Mintlify analytics as of June 2026)

- **2,140 total agent visitors** (11.8x increase vs previous period)
- **Top agents:** ChatGPT (1,981 visits), Bytedance (111), DuckDuckGo (39)
- **Top pages:** /introduction (790 views), / (778 views), /fetal-doppler/heartbeat-normal-ranges (146 views)

---

## File Locations

All files are in the mounted Mintlify directory. Key files:
- `mint.json` — Mintlify config (navigation, branding, redirects)
- `introduction.mdx` — Landing page
- `llms.txt` — AI crawler page index
- `sonohealth-llms-combined.txt` — Ready-to-install Shopify llms.txt content
- `sonohealth-llms.txt` — Standalone product catalog
- `sonohealth-aeo-audit.html` — AEO audit report
- `air-purifier/*.mdx` — All 25 AirPro pages
- `magnesium/*.mdx` — All magnesium pages
- `fetal-doppler/*.mdx` — All fetal doppler pages
- `nebulizer/*.mdx` — All nebulizer pages
