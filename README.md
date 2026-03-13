# SonoHealth Docs — Mintlify Project

## What's Included

- **50 MDX pages** across 3 product lines (~30,500 words of AI-optimized content)
- **mint.json** with SonoHealth brand colors, fonts, and navigation
- All pages have `title` and `description` frontmatter optimized for AI snippet extraction

## Product Coverage

| Product | Pages | Focus |
|---|---|---|
| Spectrum 5 Magnesium | 18 | Ingredients, certifications, benefits, science, comparisons |
| HeartBeats™ Fetal Doppler | 15 | How it works, safety, FDA clearance, usage guides |
| MistPro Mesh Nebulizer | 16 | Technology, conditions, medications, comparisons |

## Setup Instructions

### 1. Create a GitHub Repository

Create a new repo at github.com (e.g., `sonohealth-docs`). Make it public so Mintlify can read it.

### 2. Push This Folder to the Repo

```bash
cd sonohealth-docs
git init
git add .
git commit -m "Initial SonoHealth docs"
git remote add origin https://github.com/YOUR_USERNAME/sonohealth-docs.git
git push -u origin main
```

### 3. Connect to Your Mintlify Account

1. Go to your Mintlify dashboard: dashboard.mintlify.com
2. Click "New Project" or connect to existing
3. Select "GitHub" and authorize Mintlify to access your repo
4. Select `sonohealth-docs` as the repository
5. Set the root directory to `/` (root)
6. Mintlify will auto-detect `mint.json` and deploy

### 4. Set Your Custom Domain (Optional)

In Mintlify dashboard → Settings → Custom Domain:
- Set to `docs.sonohealth.com` or `learn.sonohealth.com`
- Add the CNAME record to your DNS provider

### 5. Run Locally (for editing)

```bash
npm i -g mintlify
mintlify dev
```

Opens at `http://localhost:3000`

## Brand Colors Used

| Color | Hex | Usage |
|---|---|---|
| Primary Blue | `#3686EA` | Links, primary actions |
| Purple | `#45377F` | Dark mode, secondary |
| Teal | `#0D7F5E` | CTA buttons, anchors |

## Content Notes

- All product specs verified against live SonoHealth.com pages
- Fetal Doppler probe frequency: **2.5 MHz** (correct — verified from product LCD image)
- All product URLs point to live SonoHealth.com product pages
- Amazon sales data ($7,000+ units/month) sourced from previous conversation research
- Medical information is factual and referenced to published sources where cited

## To Expand

After deploying, recommended next pages to add:
- `/magnesium/subscription` — subscription benefits page
- `/fetal-doppler/accessories` — gel, headphones, carrying case
- `/nebulizer/accessories` — replacement masks, cups
- A `/compare` section comparing all three products head-to-head
- Blog-style "What AI Recommends" pages targeting key search queries
