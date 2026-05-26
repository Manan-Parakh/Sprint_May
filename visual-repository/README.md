# Trulo Visual Repository — Master Guide

**Style: Kurzgesagt-adapted for Trulo brand. Locked.**
**Single source of truth. Start here every time.**

---

## What This Is

A production-ready library for building Trulo's biological/metabolic health visual assets — everything needed to educate people about diabetes, glucose spikes, insulin, and how Trulo's ingredients (allulose, Sunfiber) work inside the body.

The style is decided. The element list is defined. The prompts are written. Your job now is to generate, review, save, and compose.

---

## The Style — One Paragraph

Every asset in this library looks like a Kurzgesagt biology video, adapted to Trulo's warm palette. Deep warm dark background. Bold flat color fills (max 3 tonal steps). Rounded organic forms — organs are recognizable but not clinical. Soft colored outer glow on active elements (the primary way to show something is alive and working). Clean sans-serif labels in Poppins, color-matched. No cold grey. No photorealistic 3D. No cartoon blobs.

The Trulo twist: swap Kurzgesagt's blue/teal palette for saffron `#D4891A`, terracotta `#8B2500`, and linen `#F5E6C8`. Everything else follows Kurzgesagt rules.

**5 words: Warm. Glowing. Organic. Credible. Flat.**

Full style spec: `02-style-references/STYLE_DIRECTION.md`

---

## Watch List — Do This Before Generating Anything

15 minutes. These calibrate your eye before you touch a prompt.

| # | Who | What | Link |
|---|---|---|---|
| 1 | **Kurzgesagt** | How The Immune System Works | https://www.youtube.com/watch?v=lXfEK8G8CUI |
| 2 | **Kurzgesagt Dribbble** | Style frames in detail | https://dribbble.com/tags/kurzgesagt |
| 3 | **WEHI.TV** | Insulin Receptor & Type 2 Diabetes | https://www.wehi.edu.au/wehi-tv/insulin-receptor-and-type-2-diabetes/ |
| 4 | **Alila Medical** | Diabetes NARRATED (full) | https://www.alilamedicalmedia.com/media/b13f42e3-24ec-4b99-85b8-1decf0535101-updated-diabetes-narrated-animation-full-version |
| 5 | **YouTube** | 3D Glucose Transport into Cells | https://www.youtube.com/watch?v=mAaXdx4sfvY |

Watch #1 and #2 for style. Watch #3, #4, #5 for content accuracy — what actually happens biologically that you'll then illustrate in Kurzgesagt style.

---

## The Workflow — Step by Step

### Phase 1 — Generate Still Assets (~2 weeks)

Open `05-generation-prompts/GENERATION_PROMPTS.md`. Copy a prompt. Paste into Midjourney with `--style raw`. Review against the checklist below. Save approved assets to the correct subfolder.

**Week 1 — The 10 core elements**

| # | Element | Folder | Prompt |
|---|---|---|---|
| 1 | Pancreas (healthy, glowing) | `organs/` | §1.1 |
| 2 | Pancreas (fatigued, dim) | `organs/` | §1.1b |
| 3 | Glucose particle | `molecules/` | §2.1 |
| 4 | Glucose — spike state (many) | `molecules/` | §2.2 |
| 5 | Blood vessel cross-section | `organs/` | §1.5 |
| 6 | Insulin molecule | `molecules/` | §2.3 |
| 7 | Stomach interior | `organs/` | §1.3 |
| 8 | Small intestine + villi | `organs/` | §1.4 |
| 9 | Full body silhouette (healthy) | `body-level/` | §3.1 |
| 10 | Liver | `organs/` | §1.2 |

**Week 2 — Trulo-specific and process elements**

| # | Element | Folder | Prompt |
|---|---|---|---|
| 11 | Allulose crystal | `molecules/` | §2.4 |
| 12 | Sunfiber gel in gut | `molecules/` | §2.5 |
| 13 | Beta cell releasing insulin | `conditions/` | §2.6 |
| 14 | Insulin-resistant cell | `conditions/` | §2.7 |
| 15 | Blood sugar spike graph | `process-diagrams/` | §4.1 |
| 16 | GI scale visual | `process-diagrams/` | §4.2 |
| 17 | Insulin resistance — 3 stages | `process-diagrams/` | §4.3 |
| 18 | Lock-and-key mechanism | `process-diagrams/` | §4.4 |
| 19 | Allulose vs sugar pathway | `process-diagrams/` | §4.5 |
| 20 | Indian food icons (thali, roti, dal) | `icons/` | See ELEMENT_CATALOGUE.md §7 |

**Approval checklist before saving any asset:**
- [ ] Looks like Kurzgesagt biology — not clinical 3D, not cartoon
- [ ] Dark warm background (for video) or linen (for static)
- [ ] Bold warm fills — zero cold grey, zero hospital blue
- [ ] Rounded organic forms — no sharp anatomical corners
- [ ] Active elements have soft colored outer glow; passive ones don't
- [ ] Warm brown outlines (#2C1A0E) only — never black
- [ ] Organ is recognizable to a non-scientist
- [ ] Max 3 tonal steps per element

---

### Phase 2 — Compose Educational Assets (~1 week)

Take the built assets and compose them into finished educational pieces.

**Compositions to build first:**

| Composition | Elements needed | Tool |
|---|---|---|
| "What happens when you eat sugar" — full pathway | Body silhouette + stomach + intestine + blood vessel + pancreas + glucose particles | Figma or Canva Pro |
| "How insulin works" — lock and key | Cell + insulin molecule + receptor + GLUT4 | Figma |
| "Allulose vs sugar" — side by side | Spike curve + flat curve + metabolic path organs | Figma or Canva Pro |
| "GI of Indian foods" — carousel | GI scale + food icons (roti, dal, rice, mithai) | Canva Pro |
| "What repeated spikes do" — 3-stage | 3x pancreas (healthy → fatigued → damaged) | Figma |

Style rules for compositions: `02-style-references/STYLE_DIRECTION.md` → "Video vs Static" section.

---

### Phase 3 — Animate for Video

Take approved still assets as anchor frames and animate for Reels/Shorts.

| Content | Source script | Tool |
|---|---|---|
| 30-sec glucose spike video (9 scenes) | `my_files/impact-of-glucose/shotwise-prompts` | Runway Gen-3 + Kling |
| Allulose product hero video | `my_files/trulo-allulose-video-prompts.txt` | Runway Gen-3 / Pika 2.1 |
| Organ glow loops (Instagram loops) | Built still assets + Runway | Runway Gen-3 |
| Molecule motion loops | Built molecule assets | Luma Dream Machine |

**For every video prompt:** take the existing script prompt + add the Kurzgesagt video tail from `05-generation-prompts/GENERATION_PROMPTS.md` (top of Category 5).

---

## Folder Map

```
claude-cowork/visual-repository/
│
├── README.md                          ← YOU ARE HERE
│
├── 01-reference-creators/
│   └── CREATOR_PROFILES.md           ← 17 creators
│                                        ★ Kurzgesagt — primary style reference
│                                        WEHI — biological accuracy reference
│                                        Alila Medical — narrative flow reference
│                                        + 14 others for specific elements
│
├── 02-style-references/
│   └── STYLE_DIRECTION.md            ← Full Kurzgesagt style spec (READ THIS)
│                                        6 defining characteristics
│                                        Palette translation table
│                                        Organ-by-organ color assignments
│                                        Glow system rules
│                                        Video vs static background rules
│
├── 03-element-catalogue/
│   └── ELEMENT_CATALOGUE.md          ← 70+ visual elements catalogued
│                                        Molecules: glucose, insulin, allulose, Sunfiber
│                                        Cellular: beta cells, GLUT4, adipocytes
│                                        Organs: pancreas, liver, stomach, intestines
│                                        Mechanisms: spike curves, lock-key, pathways
│                                        Icons: GI scale, Indian foods, UI elements
│   ├── organs/                        ← Save generated organ PNGs here
│   ├── molecules/                     ← Save generated molecule PNGs here
│   ├── body-level/                    ← Body silhouettes, system diagrams
│   ├── food-visuals/                  ← Food illustrations
│   ├── process-diagrams/              ← GI charts, spike curves, mechanism diagrams
│   ├── conditions/                    ← Healthy vs disease state pairs
│   └── icons/                         ← GI scale, Indian food icons, UI elements
│
├── 04-inspiration-links/
│   └── INSPIRATION_LINKS.md          ← 90+ curated links
│                                        §1: Ordered watch list (start here)
│                                        §2: Studio portfolios
│                                        §2b: Style frame browsing
│                                        §2c: FREE downloadable assets
│                                        §3–7: Social, stock, brand, trend references
│
└── 05-generation-prompts/
    └── GENERATION_PROMPTS.md         ← All prompts, Kurzgesagt style throughout
                                         Global style tail (add to every prompt)
                                         Organs: §1.1–1.8 (9 organs)
                                         Molecules: §2.1–2.8 (8 molecules)
                                         Body scenes: §3.1–3.4
                                         Process diagrams: §4.1–4.6
                                         Video: §5 (Kurzgesagt tail for shotwise-prompts)
                                         Tool guide: Midjourney + Runway + Kling + Luma
```

**Existing scripts (not in this folder, but critical):**
```
my_files/impact-of-glucose/
├── master_script.md       ← 30-sec glucose spike video: narration + scene descriptions
├── shotwise-prompts       ← Shot-by-shot prompts for all 9 scenes (add Kurzgesagt tail)
├── consistency_prompts    ← Global "NOT" rules (still valid — matches Kurzgesagt)
└── rudimentary_script     ← Original narrative + 3 YouTube style references

my_files/trulo-allulose-video-prompts.txt  ← Product hero video prompts
```

---

## Brand Palette (Quick Reference)

| Name | Hex | Use |
|---|---|---|
| Saffron | `#D4891A` | Primary accent, glow, arrows, highlights |
| Terracotta | `#8B2500` | Depth, organ shadows, outlines |
| Linen | `#F5E6C8` | Static/carousel background, inner highlights |
| Golden Yellow | `#FFD580` | Glucose glow, energy, particle color |
| Warm Brown | `#2C1A0E` | All outlines, labels, text |
| Deep Warm Dark | `#0D0805` | Video/Reels background |
| Sage Green | `#7BC8A4` | Insulin molecules, healthy signals |

---

## What's Still Open

| Decision | Status |
|---|---|
| Style direction | ✅ **Locked — Kurzgesagt** |
| First video to animate | Pick: Glucose spike OR Allulose hero |
| Composition tool | Figma OR Canva Pro |
| Asset file format | PNG transparent (recommended) + source PSD/AI optional |
| Video generation tool priority | Runway Gen-3 (primary) + Kling (backup) |

---

*Style locked May 25, 2026. Merged from design/anatomy-repo/ + web research.*
*All generation, review, and iteration uses STYLE_DIRECTION.md as the benchmark.*
