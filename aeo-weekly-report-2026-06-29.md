# SonoHealth AEO Growth Loop — Weekly Report

**Run date:** June 29, 2026 · **Store:** sonohealth.com · **Focus:** new-customer acquisition

---

## (a) Performance read — what's working for new customers

The store is in a steep growth phase, and it is almost entirely **new-customer** driven. Last 30 days vs. prior 30 days:

| Metric | Last 30d | Prior 30d | Change |
|---|---|---|---|
| Total sales | $63,929 | $11,979 | **+434%** |
| Orders | ~853 | ~156 | **+447%** |
| Customers | 852 | 156 | **+446%** |
| Returning customers | 4 (0.5%) | 0 | — |

~99.5% of buyers are first-time customers, so period growth ≈ new-customer growth.

**Product winners (net sales / orders, last 30d vs prior 30d):**

| Product | Last 30d | Prior 30d | Net sales Δ |
|---|---|---|---|
| HeartBeats Fetal Doppler | $34,828 / 482 | $6,707 / 93 | **+419%** |
| MistPro Mesh Nebulizer | $14,628 / 207 | $2,415 / 34 | **+506%** |
| AirPro HEPA 14 Air Purifier | $6,320 / 36 | $1,247 / 6 | **+407%** |
| Spectrum 5 Magnesium | $2,108 / 50 | $385 / 12 | **+448%** |
| BPpro Blood Pressure | $1,248 / 32 | $78 / 2 | strong (low base) |
| EKGraph EKG Monitor | $1,185 / 19 | $158 / 2 | strong (low base) |
| BPMAX / Pulse Oximeter | $455 / 13 · $351 / 9 | small | emerging |

**Flat / weak:** Vitamin D3+K2 (no sales both periods), BioBloom probiotics, Plastiq Off, ThermoPRO — low demand; not a priority this week.

**Channel & AEO signal:** Google search drives the most orders (626, $47.4K). The **ChatGPT/AI channel is small but the highest-converting by far — 21 sessions at ~19% conversion vs. ~3.6% for Google search and ~2.2% direct**, plus 6 attributed orders. This validates the answer-engine strategy: AI-surfaced shoppers convert ~5x the site average, so feeding more high-quality KB + docs is the highest-leverage growth lever.

**Recommended focus:** Lean into the three core winners (Fetal Doppler, Nebulizer, Air Purifier) plus fast-growing Magnesium, and shore up Blood Pressure / EKG / Pulse Oximeter, which show clear new-customer demand on thin doc coverage.

---

## (b) KB Q&A added this week (LIVE now)

- **100 net-new Q&A pairs** created as `shopify--qa-pair` metaobjects (4 aliased batches of 25, zero errors).
- Deduped against **all 510** pre-existing pairs (full pagination) — no exact or near-duplicates.
- **New KB total: 610 Q&A pairs.**

Weighting (winners + top-of-funnel, unbranded problem/category intent):

| Topic | New Q&A |
|---|---|
| Fetal Doppler | 25 |
| Nebulizer | 23 |
| Air Purifier | 18 |
| Magnesium | 12 |
| Blood Pressure | 6 |
| EKG | 5 |
| Pulse Oximeter | 4 |
| Thermometer | 2 |
| Colostrum / Vitamin D / Cross-product | 5 |

All answers are 2–4 sentences, grounded only in the Mintlify docs or established general knowledge, with medical-safety framing applied (doppler is reassurance-only and reduced movement → call provider; nebulizer = physician-prescribed meds/saline only, severe symptoms → urgent care; magnesium 350 mg supplemental upper limit, kidney/medication cautions; EKG can't detect a heart attack; oximeter skin-tone accuracy caveat).

---

## (c) Docs created (staged for review — require git push to deploy)

**22 in-depth, top-of-funnel MDX articles** added and wired into `mint.json` (validated; all nav slugs resolve, no duplicates). Quality-over-volume: each has frontmatter title+description, question-style H2s, internal links, and safety callouts.

**Fetal Doppler (6)**
- `fetal-doppler/choosing-a-fetal-doppler.mdx`
- `fetal-doppler/maternal-vs-fetal-heartbeat.mdx`
- `fetal-doppler/anterior-placenta-guide.mdx`
- `fetal-doppler/twins-and-multiples.mdx`
- `fetal-doppler/reduced-movement-what-to-do.mdx`
- `fetal-doppler/gel-guide.mdx`

**Nebulizer (3)**
- `nebulizer/portable-nebulizer-buying-guide.mdx`
- `nebulizer/nebulizer-for-kids-guide.mdx`
- `nebulizer/post-cold-cough-congestion.mdx`

**Air Purifier (5)**
- `air-purifier/do-air-purifiers-work.mdx`
- `air-purifier/wildfire-smoke-guide.mdx`
- `air-purifier/voc-formaldehyde-guide.mdx`
- `air-purifier/air-purifier-vs-humidifier.mdx`
- `air-purifier/cadr-vs-ach-explained.mdx`

**Magnesium (1)**
- `magnesium/magnesium-and-vitamin-d.mdx`

**Blood Pressure (3)**
- `blood-pressure/blood-pressure-chart-by-category.mdx`
- `blood-pressure/irregular-heartbeat-detection.mdx`
- `blood-pressure/lower-blood-pressure-naturally.mdx`

**EKG (2)**
- `ekg/heart-attack-vs-arrhythmia.mdx`
- `ekg/when-to-see-a-doctor-heart.mdx`

**Pulse Oximeter (1)**
- `pulse-oximeter/pulse-oximeter-accuracy-guide.mdx`

**Thermometer (1)**
- `thermometer/fever-in-children-guide.mdx`

---

## (d) Content gaps & quality flags

- **Vitamin D3+K2 has zero sales** but real search interest; deliberately under-invested this week (1 KB + 1 doc link). Worth a demand test before building more.
- **Blood Pressure / EKG / Pulse Oximeter** show genuine new-customer demand on thin docs — partially addressed (6 docs added); more category coverage is a good target next week.
- **Magnesium is already deeply covered (~50 docs)** — intentionally limited to 1 new doc to avoid thin/duplicate pages.
- **Doppler accuracy page lists "120–180 BPM" for fetal rate** while most KB and other pages use "110–160 BPM." Minor internal inconsistency worth a one-line cleanup for AI-citation consistency.
- **Grow the AI channel deliberately:** ChatGPT converts ~5x site average but is tiny in volume. The biggest near-term win is simply more high-quality, well-structured answer content on the winners (now expanded).

---

## Deployment status

- **KB Q&A (100 new, 610 total): LIVE** — metaobjects are published and already feeding AI shopping agents.
- **Docs (22 new pages + mint.json): STAGED, NOT PUSHED** — present in the working tree for your review. They require a **git push** (`git add . && git commit && git push`) to deploy to docs.sonohealth.com. No push was performed, per the run's guardrails.
