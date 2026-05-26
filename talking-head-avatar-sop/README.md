# Talking Head Avatar — Production Hub
**Trulo Foods · Internal · May 2026**

This folder is the production workspace for all Trulo talking head avatar videos. It contains the workflow documentation, per-video idea folders, and references the shared visual asset library.

---

## Files in this folder

| File | What it is |
|------|-----------|
| `how-to-produce-a-talking-head-video.md` | **Start here.** Step-by-step guide: script → ElevenLabs audio → HeyGen avatar → publish. Covers every tool setting, QA checklist, and file naming convention. |
| `sop.html` | Full production SOP as a styled HTML document (same content as above, web-viewable). |
| `index.html` | Research report: platform comparison (HeyGen vs Synthesia vs D-ID), voice tool comparison (ElevenLabs vs Murf), creator reference library, content type taxonomy. |
| `talking-head-avatar-sop.md` | Combined SOP + research in single markdown. |

---

## Idea folders

Each video gets its own `idea_N_[topic]/` folder created by the `/video-idea` skill (see below).

| Folder | Topic | Status |
|--------|-------|--------|
| `idea_1_impact_of_glucose/` | Blood glucose spikes — causes, effects, habits | In progress |

### What each idea folder contains

```
idea_N_[topic]/
├── rudimentary_script     ← Original human-written script (verbatim, unmodified)
├── text_to_speech         ← TTS-optimized narration with pause markers
├── README.md              ← Full animation production plan (see below)
└── [exported audio/video files when produced]
```

---

## The `/video-idea` Skill

### What it does

`/video-idea` takes a raw, human-written script and produces a complete animation production package in one step. You give it a rough script — it creates everything you need to start generating animations.

**To use it:**

```
/video-idea [paste your rudimentary script here]
```

Or paste the script after typing the command.

### What it creates

**1. A new idea folder** (`idea_N_[topic]/`) with:
- `rudimentary_script` — your original script saved verbatim
- `text_to_speech` — the same script cleaned up for ElevenLabs: spoken delivery pacing, SSML pause markers, FSSAI compliance check, pronunciation guides
- `README.md` — the full animation production plan (see sections below)

**2. The idea folder `README.md` contains six sections:**

| Section | What's in it |
|---------|-------------|
| **A — Overview** | Topic, estimated duration, scene count, assets needed vs. ready |
| **B — Scene-by-scene animation plan** | Every scene mapped: spoken line → animation description → which existing image to use (exact filename) → whether a new image is needed |
| **C — New elements to generate** | For every gap in existing assets: full Midjourney/DALL-E prompt in Kurzgesagt style, folder to save in, approval criteria |
| **D — Animation prompts** | For every scene: tool recommendation (Runway/Kling/Luma), duration, **initial frame prompt**, **final frame prompt**, full motion prompt, compositing note |
| **E — Assembly order** | How clips sequence together, when the talking head is visible vs. fullscreen animation, text overlay notes |
| **F — Assets checklist** | Two ready-to-tick lists: existing assets to pull and new assets to generate |

### Why this order matters

The skill reads the visual inventory (`visual-repository/VISUAL_INVENTORY.md`) before making any suggestions. It only recommends generating new images for scenes that have no good existing match. This means you:
- Don't re-generate images that already exist
- Know exactly which existing filename to pull for each scene
- Get specific initial + final frame prompts written against the actual images you have

### Example output for a 60-second video

```
Idea folder created: idea_2_benefits_of_allulose/
Scenes planned: 8
Using existing assets: 6 scenes (75%)
Needs new generation: 2 scenes
  - Allulose crystal particle → Midjourney, save to molecules/
  - Walking figure post-meal → Midjourney, save to body-level/
Estimated generation time: ~30 min (2 Midjourney images + 8 Runway clips)
```

---

## Visual Repository

The shared asset library lives at:
`D:\Intern\Trulo\claude-cowork\visual-repository\`

Key files:

| File | What it is |
|------|-----------|
| `VISUAL_INVENTORY.md` | **The image index.** All 28 existing images listed with exact filenames, what they show, and a quick scene lookup table. The `/video-idea` skill reads this automatically. |
| `README.md` | Master guide to the repository — style overview, workflow, folder map, brand palette. |
| `02-style-references/STYLE_DIRECTION.md` | Full Kurzgesagt style spec. Every asset must pass this. |
| `05-generation-prompts/GENERATION_PROMPTS.md` | All generation prompts for still images (Midjourney/DALL-E) and video (Runway/Kling/Luma). The global style tail to append to every prompt is here. |
| `03-element-catalogue/ELEMENT_CATALOGUE.md` | Catalogue of all 60+ elements planned (organs, molecules, cellular, body-level, food, process diagrams, icons). |

### What's already generated (28 images)

Quick summary — see `VISUAL_INVENTORY.md` for exact filenames:

- **Organs (10):** Pancreas healthy, pancreas fatigued, liver, stomach cross-section, small intestine villi, blood vessel cross-section, heart, brain (x2 variants), kidney
- **Molecules (8):** Glucose single, glucose spike top-down, glucose flood side-view, insulin molecule, dietary fiber gel, beta cell releasing insulin, insulin-resistant cell, GLUT4 open/closed
- **Body-level (4):** Healthy body silhouette, crash/dim silhouette, bloodstream POV top-down, pancreas releasing insulin scene
- **Process diagrams (6):** Blood sugar spike curve, GI scale, 3-stage insulin resistance, lock-and-key mechanism, allulose vs sugar comparison, sunfiber gut before/after

### What still needs to be generated

Allulose crystal, fructose molecule, fat cell, large intestine, muscle cell, gut epithelial cell close-up, high-GI food illustration, low-GI food illustration, walking figure, active body silhouette, healthy blood vessel, glucagon molecule. See `VISUAL_INVENTORY.md` → "What's Missing" section.

---

## Production workflow (quick reference)

```
1. Write rough script
       ↓
2. /video-idea [paste script]
   → Creates idea folder, TTS file, full animation plan
       ↓
3. Generate missing images
   → Use prompts from idea README Section C
   → Save to visual-repository/03-element-catalogue/[folder]/
       ↓
4. Generate animation clips
   → Use prompts from idea README Section D
   → Runway Gen-3 / Kling / Luma Dream Machine
       ↓
5. Generate voiceover in ElevenLabs
   → Use text_to_speech file as input
   → Model: Eleven Multilingual v3
   → Export: MP3, 192 kbps
       ↓
6. Build talking head video in HeyGen
   → Upload ElevenLabs MP3 (disable HeyGen voice)
   → Lip-sync avatar to your audio
   → Add animation clips as background / cutaways in CapCut
       ↓
7. QA and publish
   → See how-to-produce-a-talking-head-video.md → QA Checklist
```

---

*Trulo Foods Internal · May 2026*
