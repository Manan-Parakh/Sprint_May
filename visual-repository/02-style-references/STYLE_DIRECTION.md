# Style Direction — Trulo Biological Visualization
**Style: LOCKED — Kurzgesagt-adapted for Trulo brand**
**Sprint:** May 26–28, 2026

---

## Style Decision: Made

The visual style for all Trulo biological content is **Kurzgesagt-adapted**.

This is not a direction to evaluate. It is the production standard going forward. Every asset generated, every prompt written, every frame reviewed uses this as the benchmark.

---

## What Kurzgesagt Style Actually Means

Kurzgesagt is not "flat cartoon." It occupies a specific visual zone that takes discipline to execute correctly.

### The 6 defining characteristics:

**1. Dark backgrounds, bright elements**
Every biology video Kurzgesagt makes uses a deep, rich background — dark navy, deep charcoal, or deep warm brown. Organs, molecules, and characters sit on this dark field and *pop* with warm, saturated color. Nothing is washed out. Nothing is clinical white.

**2. Bold, flat fills with 2–3 tonal steps**
No photorealistic gradients. No subsurface scattering. Each organ or element gets a base fill, one highlight, one shadow — max. The result reads as illustrated, not rendered. It's warm and confident, not cold and digital.

**3. Rounded, organic forms everywhere**
Zero sharp corners. Organs are slightly softer than real anatomy — not blobs, but the hard edges of a real liver or pancreas are eased into smooth curves. Cells and molecules have personality. They feel like they belong in the same universe as Kurzgesagt's birds.

**4. Soft colored glow on active elements**
The signature "alive" quality. A pancreas releasing insulin has a warm amber glow around it. A glucose particle in the bloodstream has a soft golden halo. A fatigued cell is dim, no glow. This glow is the primary way Kurzgesagt communicates biological activity without animation.

**5. Warm, saturated color palette — not pastels, not clinical**
Kurzgesagt uses rich, fully saturated warm colors. Oranges that are actually orange. Reds that feel warm, not alarming. Yellows that glow. For Trulo, this maps directly onto the brand palette — saffron, terracotta, golden yellow — applied at full saturation on the dark background.

**6. Clean, integrated typography**
Labels and callouts use bold, clean sans-serif (Poppins or similar). They're part of the design, not afterthoughts. Color-coded to match their element. Short. Never a full sentence on an illustration.

---

## The Kurzgesagt ↔ Trulo Palette Translation

Kurzgesagt's biology videos typically use a deep blue-purple or deep warm-dark background. For Trulo, this shifts to a **warm dark** — deep brown-black that feels like an amber-lit interior rather than cold space.

| Kurzgesagt standard | Trulo adaptation | Hex |
|---|---|---|
| Deep dark background | Deep warm brown-black | `#0D0805` |
| Warm accent (orange) | Saffron | `#D4891A` |
| Bright highlight | Golden yellow | `#FFD580` |
| Organ depth (dark shade) | Terracotta | `#8B2500` |
| Neutral surface / label bg | Linen (for static only) | `#F5E6C8` |
| Outline color | Warm brown | `#2C1A0E` |
| Cool contrast accent | Deep teal-sage (for insulin, veins) | `#2D6B5E` |

**Static posts and carousels** swap the dark background for linen (`#F5E6C8`) — Kurzgesagt's visual rules (bold fills, glow, rounded forms) still apply, just on a warm light ground instead of dark.

---

## Organ-by-Organ Color Assignments

Kurzgesagt assigns each biological element a consistent, memorable color. Trulo's system:

| Element | Base fill | Highlight | Shadow/depth | Glow color |
|---|---|---|---|---|
| Pancreas | `#C4704A` warm salmon | `#F0C4A0` cream | `#8B3A1A` | `#D4891A` saffron |
| Liver | `#8B3A1A` mahogany | `#C4704A` terracotta | `#5C1A0A` deep | `#D4891A` saffron |
| Stomach | `#D4896A` peach-terracotta | `#F0C4A0` cream | `#8B3A1A` | `#FFD580` golden |
| Small intestine | `#E8C4A0` warm cream | `#F5E6C8` linen | `#C4704A` | `#FFD580` golden |
| Large intestine | `#A0785A` muted brown | `#C4956A` | `#5C3A1A` | none |
| Blood vessel | `#C0392B` crimson | `#E8735A` salmon | `#8B1A0A` | `#FF6B4A` warm red |
| Heart | `#B03020` deep rose-red | `#D4603A` | `#8B1A0A` | `#FF6B4A` |
| Brain | `#C8A090` warm pink-grey | `#E8C8B8` | `#8B5040` | `#FFD580` golden |
| Glucose molecule | `#FFD580` golden | `#FFF0C0` bright | `#D4891A` | `#FFD580` bright |
| Insulin molecule | `#7BC8A4` warm sage | `#B4E8CC` | `#2D6B5E` | `#7BC8A4` sage |
| Allulose crystal | `#F0F0FF` white-cool | `#FFFFFF` | `#D0D0E8` | `#FFD580` sparkle |
| Sunfiber gel | `#C8A878` warm amber | `#E8C8A0` | `#8B6840` | `#D4891A` |
| Beta cell | `#D4895A` warm orange | `#F0C4A0` | `#8B4A1A` | `#FFD580` |
| Fat cell | `#E8C840` warm yellow | `#F8E880` | `#B8980A` | dim / none |
| Body silhouette | `#F5E6C8` linen @ 40% | `#FFFFFF` @ 20% | transparent | `#D4891A` edge glow |

---

## The Glow System

The single most important quality Kurzgesagt brings to biological illustration is **selective glow** — elements that are active, healthy, or important glow. Elements that are passive, damaged, or secondary don't.

**Rules:**
- Active / healthy / releasing: bright warm outer glow, 20–40px radius, 40–60% opacity
- Resting / supporting: soft inner highlight only, no outer glow
- Fatigued / damaged / resistant: glow absent or reduced to 10% opacity, color shifted gray-warm
- Background glow context: faint ambient warm glow behind hero elements (not hard light)

**The glow color always matches the element's highlight color** — never white, never grey.

---

## Typography in Kurzgesagt Style

- **Font:** Poppins SemiBold or Bold for labels; Poppins Regular for supporting text
- **Size:** Large enough to read at Instagram mobile size
- **Color:** Match to the element being labeled — glucose label in `#FFD580`, insulin in `#7BC8A4`
- **No outlines on text** — the dark background provides enough contrast
- **Max 3 labels per asset** — Kurzgesagt never crowds their frames with text
- **Style:** All caps for headers, title case for labels

---

## The "Not Gore, Not Cartoon" Line in Kurzgesagt Context

The common mistake when imitating Kurzgesagt for biology is going too flat (Headspace-blob territory) or adding too much 3D render (losing the illustration quality). The test:

**Too flat (avoid):** Organs look like icons. No depth reading. Could be a logo.
**Too rendered (avoid):** Subsurface scatter visible. Looks like a 3D medical render. Cold.
**Kurzgesagt sweet spot:** You can tell it's illustrated, you can tell what organ it is, it has warmth and light, but it never looks like a photograph or a surgery.

**Specific red lines for Trulo:**
1. No raw tissue texture — surface is smooth or has subtle stylized texture only
2. No blue or grey-toned organs — everything stays in the warm palette
3. No clinical white backgrounds for video content — always the deep warm dark
4. No thin outlines on linen — outlines only on dark background; linen gets soft shadow instead
5. Molecules must look like molecules, not logos — slight structural hint required

---

## Kurzgesagt Frame Anatomy

Every well-constructed Kurzgesagt frame has this structure:

```
┌─────────────────────────────────┐
│  [dark background gradient]     │
│                                 │
│     [ambient background glow]   │
│         ╔═══════════╗           │
│         ║  ORGAN    ║◀── glow  │
│         ║  (hero)   ║           │
│         ╚═══════════╝           │
│   ↑                  ↑          │
│ [molecule           [molecule   │
│  particles]          particles] │
│                                 │
│  [label]        [label]         │
└─────────────────────────────────┘
```

- Hero element centered or rule-of-thirds positioned
- Supporting elements (molecules, particles) surround it at smaller scale
- Labels close to their element, color-matched
- Ambient glow behind the hero creates depth without shadow
- Composition reads cleanly at 9:16 vertical for Reels

---

## Video vs Static — Same Style, Different Background

| Context | Background | What changes | What stays the same |
|---|---|---|---|
| Video / Reels | `#0D0805` deep warm dark | Background, glow intensity (brighter) | All fills, forms, palette |
| Static Instagram post | `#F5E6C8` linen | Background, glow off or subtle | All fills, forms, palette |
| Carousel slide | `#F5E6C8` linen or `#D4891A` saffron field | Background | All fills, forms, palette |
| Story panel | `#0D0805` dark or saffron gradient | Background | All fills, forms, palette |

The asset library is built once (transparent PNG) and placed on whichever background the content needs. The style is the same — the environment changes.

---

## Kurzgesagt Reference Frames to Study

Before generating any asset, spend 10 minutes screenshotting frames from these specific Kurzgesagt videos. Look at: how organs sit against the dark background, how particles move, how glow works, how labels integrate.

| Video | What to screenshot |
|---|---|
| How The Immune System Works: https://www.youtube.com/watch?v=lXfEK8G8CUI | Cell forms, glow on active cells, dark background |
| The Human Body — Your Incredible Body: Search Kurzgesagt | Organ visualization, body silhouette style |
| Cells (protein language video): https://thekidshouldseethis.com/post/cells-complex-language-kurzgesagt-video | Molecule particle systems, inside-cell feel |
| Kurzgesagt Dribbble: https://dribbble.com/tags/kurzgesagt | Still design frames, color system in detail |
| Kurzgesagt Pinterest: https://www.pinterest.com/ideas/kurzgesagt-art-style/934861879895/ | Full color palette and form reference |

---

*Style locked: May 25, 2026. All generation, review, and iteration uses this document as the benchmark.*
