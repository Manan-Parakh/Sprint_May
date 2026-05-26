# Talking Head Avatar — SOP & Research
**Trulo Foods · Internal Document · May 2026**

---

## Contents

1. [Top Picks (TL;DR)](#top-picks)
2. [The Production Stack](#production-stack)
3. [Creator Reference Library](#creator-reference-library)
4. [Content Type Taxonomy](#content-type-taxonomy)
5. [Platform Comparison — HeyGen vs Synthesia vs D-ID](#platform-comparison)
6. [Voice Tool Comparison — ElevenLabs vs Murf](#voice-tool-comparison)
7. [Similar & Adjacent Tools](#similar-tools)
8. [One-Time Setup](#one-time-setup)
9. [Pre-Production](#pre-production)
10. [Phase 2 — Voice Generation (ElevenLabs)](#voice-generation)
11. [Phase 3 — Avatar Production (HeyGen)](#avatar-production)
12. [Phase 4 — Post-Production & Publishing](#post-production)
13. [QA Checklist](#qa-checklist)
14. [Cost Tracker](#cost-tracker)
15. [Quick Reference Card](#quick-reference)

---

## Top Picks

| Role | Pick | Why |
|------|------|-----|
| **Avatar Platform** | **HeyGen** | Best lip-sync for Indian English, 175+ languages, social-native output, Avatar IV/V model passes the "is this real?" test. Creator plan at $24/mo. |
| **Voice Tool** | **ElevenLabs** | 89.6% speech naturalness score, 11 Indian regional languages via Multilingual V3, voice cloning from $11/mo. Far superior realism vs. Murf. |

> **Critical note — Accent Drift:** HeyGen's built-in voice clone drifts toward an American inflection. Fix: generate voiceover in ElevenLabs first, upload that audio to HeyGen, let HeyGen lip-sync to it. This combo locks the Indian English accent.

---

## Production Stack

```
Script (Google Docs / Notion)
    ↓
ElevenLabs Creator ($11/mo) — voice generation
    ↓
HeyGen Creator ($24/mo) — avatar + lip-sync + export
    ↓
CapCut / InShot (free) — optional light trim
    ↓
Publish
```

**Total entry cost: ~$35/mo** for ~8–10 × 60-second videos per month.

### Why keep them separate?
HeyGen can generate its own voice, but cloned voices drift toward American English. By generating audio in ElevenLabs first and uploading it to HeyGen, the avatar lip-syncs to your audio — the Indian English accent stays locked. **Never use HeyGen's built-in voice clone for Indian English.**

---

## Creator Reference Library

### 🇮🇳 India — News

**India Today — AI Anchor "Sana"**
- India's most prominent AI news anchor. Delivers prime-time 9pm news, bilingual (Hindi + English), traditional Indian attire, micro-expressions.
- Won INMA 2024 Global Media Award. Next-gen avatar "Sutra" (real-time interaction) launched 2026.
- Unique traits: Cultural attire, bilingual Hinglish, broadcast-quality, daily cadence, real-time interaction
- Links:
  - [YouTube Short](https://www.youtube.com/shorts/qdDdu-o_mxs)
  - [Full Playlist (AajTak)](https://www.youtube.com/playlist?list=PLPPKwCCueQ_BrKtsQVa5m6qBPJJ267M-O)
  - [Instagram Reel](https://www.instagram.com/aianchorsana/reel/C6byXklptgb/)

**Odisha TV — AI Anchor "Lisa"**
- India's first regional-language AI news anchor. Bilingual: Odia + English.
- A published research paper found higher YouTube retention for Lisa vs. human anchors on the same channel.
- Unique traits: Regional language pioneer, daily news format, academic engagement study
- Links:
  - [Launch Video](https://www.youtube.com/watch?v=k5NcpmQOu1g)
  - [AI Lisa Playlist](https://www.youtube.com/playlist?list=PLFYlC_Oei63AbISEhhTScnmEKHiFwcOHY)

### 🇮🇳 India — Education / Finance

**Indian Faceless Ed-Tech / Finfluencer Channels**
- 75%+ of new Indian educational/infotainment YouTube channels launched 2025–26 use AI-led avatar formats.
- Finance ("Finfluencer") channels dominate — AI presenter delivers SEBI-compliant market education.
- Unique traits: SEBI-compliant format, AI as recurring brand character, Hinglish delivery, high RPM niche
- [Context: TrueFan Blog](https://www.truefan.ai/blogs/faceless-youtube-channel-ai-india-2026)

**Dhiva Logu — "AITuber" Creator**
- Early Indian creator publicly building an AITuber brand on YouTube. Tamil + English. Full faceless workflow.
- [LinkedIn](https://www.linkedin.com/in/dhivalogu/)

### 🌍 International — Brand & Corporate

**Synthesia — Brand Marketing Library**
- 14 curated talking-head video examples: product demos, onboarding, compliance training, social ads.
- 240+ avatars, 160+ languages. Used by enterprise teams for L&D and multilingual content.
- Unique traits: 1-click 160-language dub, enterprise-grade, branded overlays
- [14 Examples](https://www.synthesia.io/post/best-talking-head-video-examples) · [250+ Templates](https://www.synthesia.io/video-templates) · [Marketing Examples](https://www.synthesia.io/post/marketing-video-examples)

**HeyGen — Creator Avatar Showcase**
- Public avatar gallery showing real creator outputs: social ads, product explainers, UGC-style testimonials.
- Avatar IV model (Aug 2025): full-body motion + micro-expressions — current benchmark for AI avatar realism.
- Unique traits: Full-body motion, micro-expressions, social-media native, UGC-style output
- [Avatar Gallery](https://community.heygen.com/public/collections/avatar-videos) · [Format Guide](https://www.heygen.com/blog/talking-head-video)

### 🥗 Food / CPG

**AI Food Avatar Content (Media.io)**
- Animated talking food/ingredient characters and AI avatar food presenters for Reels/Shorts.
- Directly relevant to Trulo — demonstrates ingredient spotlight content without on-camera talent.
- Unique traits: Food/ingredient characters, Reels/Shorts native
- [See Tool](https://www.media.io/video-effects/ai-food-talk.html)

**CPG Brand AI Avatar Ads (Creatify)**
- Drop a product URL → AI writes scripts → generates talking-head avatar ads in 2 minutes.
- CPG/FMCG brands using this have reported 45% better CPA and 73% better ROAS.
- Unique traits: URL-to-ad pipeline, A/B variant generation, performance-ad optimised
- [Format Overview](https://creatify.ai/blog/ai-avatar-generator-create-talking-video-ads-in-2-minutes)

---

## Content Type Taxonomy

### 6 Talking Head Content Formats

| Type | Description | Key traits |
|------|-------------|------------|
| **📺 AI News Anchor** | Avatar as daily news presenter. Sana, Lisa. Requires broadcast-grade realism. | Daily cadence · cultural styling · teleprompter pacing |
| **🎓 Educational Explainer** | Avatar teaches a topic. Dominant in Indian finance/ed-tech. B-roll + avatar split-screen. | Script-heavy · on-screen graphics · series format · 5–15 min |
| **📦 Product Explainer/Demo** | Avatar presents product features or benefits. Most common in FMCG and D2C. | Short-form · benefit-led · brand-voiced · multilingual dub |
| **📱 Social Ad / UGC-style** | Avatar mimics creator energy — casual, direct-to-camera. For paid Instagram/TikTok/Shorts ads. | 9:16 vertical · hook-first · multiple A/B variants |
| **🏢 Corporate Training** | Avatar delivers onboarding, compliance, or SOP content. Synthesia dominates. | Multilingual critical · custom brand avatar · L&D platform integration |
| **🎤 Brand Spokesperson** | Named, recurring AI character representing the brand across all content. | Custom avatar ($1K+ setup) · cross-platform · brand personality |

### Common traits across ALL types
- Direct-to-camera framing (no side angles)
- Script read at controlled pace (~130–150 wpm)
- Neutral or slightly warm background / studio look
- Subtitles / captions always present
- No heavy gestures — hands mostly below frame or static
- Consistent avatar across episodes (brand identity)

### What makes each type unique
- **News:** Indian cultural styling, rapid delivery, teleprompter cadence
- **EdTech:** Split-screen with slides/charts, deliberate slower pacing
- **Social ads:** Casual wardrobe, hook in first 2 sec, CTA at end
- **Brand ambassador:** Custom avatar name, branded frame, personality quirks
- **Corporate:** Headset mics, formal attire, white/office backgrounds

---

## Platform Comparison

### HeyGen vs Synthesia vs D-ID

| Criterion | HeyGen ⭐ Recommended | Synthesia | D-ID |
|-----------|----------------------|-----------|------|
| **Indian-accent voice** | ★★★★☆ Strong — 175+ languages, Hindi dubbing "clean, well-synced," multiple Indian accent toggles. Watch: accent drift on voice clones. | ★★★☆☆ Good — 160+ languages, 1,000+ AI voices. Indian English supported but no specific quality test data. | ★★★☆☆ Adequate — 120+ languages. Functional Indian English, narrower accent library. |
| **Lip-sync accuracy** | ★★★★½ Excellent — Avatar IV/V: full-body motion + micro-expressions. Smooth Hindi/Indian English. | ★★★★★ Best-in-class multilingual — leads on French, Arabic, Japanese in independent tests. Close second for English. | ★★★☆☆ Adequate — works for most languages. Head movement can feel mechanical. |
| **Cost per minute** | ~$2.40/min (Creator $24/mo = 10 min). Extra credits: ~$1/added min. | ~$1.80/min (Starter $18/mo = 10 min annual). Custom avatar add-on: $1,000/yr. | $0.60–$4.60/min. BUT commercial rights only on Advanced plan ($299/mo). |
| **Turnaround** | ⚡ Near real-time (minutes) | ⚡ Near real-time (minutes) | ⚡ Near real-time — but reliability issues reported. |
| **Free tier** | 3 videos/mo, up to 3 min, 720p, watermarked | 3 videos/mo, up to 5 min, watermarked | 14-day trial only. No ongoing free tier. |
| **Custom avatar** | From Creator plan — 2-min photo/video upload | $1,000/yr add-on (Studio Express-1) | Available on Pro+ — portrait-only output. |
| **Reliability** | ✅ Strong — widely used by major brands | ✅ Strong — enterprise-focused | ❌ Weak — Trustpilot 1.5/5, billing complaints, failed generations |
| **Best for** | Social ads, Reels/Shorts, brand spokesperson, multilingual product content | Corporate L&D, enterprise training, multilingual publishing at scale | Not recommended for professional marketing |

> **D-ID verdict:** Avoid for professional marketing use. Commercial rights gated behind the $299/mo Advanced plan, and Trustpilot reviews flag recurring billing and generation failures.

---

## Voice Tool Comparison

### ElevenLabs vs Murf

| Criterion | ElevenLabs ⭐ Recommended | Murf |
|-----------|--------------------------|------|
| **Indian English quality** | ★★★★★ — 89.6% speech naturalness score. Most lifelike AI voice available. | ★★★★☆ — Good, slightly synthetic. "Polished synthetic" quality, below ElevenLabs realism. |
| **Indian languages** | 11 Indian regional languages via Multilingual V3: Hindi, Tamil, Malayalam, Kannada, Telugu, Gujarati + more | Indian English + Hindi, Tamil, Bengali among 35+ languages. Non-English voices ~80–85% as natural as English. |
| **Voice cloning** | Instant clone: Starter ($5/mo). **Pro clone: Creator ($11/mo).** High-fidelity from short samples. | Enterprise only — starts at **$75/mo for 5 users.** Not accessible on individual plans. |
| **Free tier** | 10,000 credits/mo ≈ 10 min high-quality TTS | 10 min generation, no download, no commercial use. Too restrictive for evaluation. |
| **Pricing** | Free → Starter $5 → Creator $11/mo → Pro $99/mo | Free → Creator Lite $19/mo → Creator Plus $33/mo → Business Lite $26/mo |
| **Best used for** | Generate voiceover → upload to HeyGen for lip-sync. Avoids HeyGen accent drift. | Teams wanting built-in video/presentation sync. Good for structured L&D. |
| **Weakness** | No built-in video editor — pure audio tool, needs pairing with avatar platform. | Voice cloning gated behind expensive enterprise tier. Realism gap on Indian English. |

---

## Similar & Adjacent Tools

### Avatar Platforms

| Tool | What it is | Best for |
|------|-----------|---------|
| **Hedra AI** | "Dark horse of 2026" — photorealistic talking head from a single image | Testing as HeyGen alternative for max realism |
| **Creatify** | Product URL → AI scripts → avatar ad in 2 min | Performance ads, rapid A/B testing |
| **InVideo AI** | Full video editor + AI avatar generator. Lower price than HeyGen. | Indian creators, experimentation before committing |
| **TrueFan Studio / Voomo** | India-built, culturally resonant avatars (Gunika, Annie, Aryan). Hinglish phoneme accuracy. | India-first content, Hinglish delivery |
| **Captions.ai** | Talking-head + auto-captions + B-roll, all-in-one mobile/web app | Fast social video with zero context-switching |
| **Jogg AI** | Avatar consistency across episodic content | Recurring AI host identity for video series |

### Voice Tools

| Tool | What it is | Best for |
|------|-----------|---------|
| **Cartesia** | Ultra-low-latency TTS, API-first | Real-time interactive avatar experiences |
| **VEED.io Voice** | Avatar + AI voiceover + captions in one tool | All-in-one social creators, lower quality ceiling |

---

## One-Time Setup

*Do this once before your first production. Takes ~2–3 hours total.*

### A. ElevenLabs Setup (~60 min)

**Step 1 — Create account & subscribe to Creator plan ($11/mo)**
Go to [elevenlabs.io](https://elevenlabs.io) → Sign up → Creator plan.
Unlocks: Professional Voice Cloning, 100,000 credits/mo, 192 kbps quality.

**Step 2 — Record voice sample for cloning**
```
Mic:     Any condenser mic or iPhone in a quiet room
Format:  MP3 or WAV, 44.1 kHz, no background noise
Length:  2–5 minutes of continuous natural speech
Content: Read a product description or brand story aloud — varied sentences
Avoid:   Music, echo, plosives (use a pop filter or move back from mic)
```
> ⚠️ Do NOT use music, background sound, or over-processed audio. ElevenLabs will clone those artifacts too.

**Step 3 — Create the Professional Voice Clone**
Voices → Add a new voice → Professional Voice Clone → Upload recording.
Name it: *"Trulo — [Name] (Indian EN)"*. Training takes 15–30 min.

Recommended voice settings after cloning:
```
Stability:          55–65   (lower = more expressive, higher = more consistent)
Similarity boost:   75–80   (how closely it mirrors the clone)
Style exaggeration: 20–30   (subtle warmth without over-acting)
Speaker boost:      ON      (boosts similarity for short texts)
```

**Step 4 — Test with a 30-second sample script**
Generate a product sentence. Pass criteria: natural Indian English cadence, correct stress, no American vowel shifts.

---

### B. HeyGen Setup (~60 min)

**Step 5 — Create account & subscribe to Creator plan ($24/mo)**
Go to [heygen.com](https://heygen.com) → Creator plan.
Tip: Use the 3-video free tier first to test before subscribing.

**Step 6 — Choose your avatar approach**

| Option | How | Cost | Best for |
|--------|-----|------|---------|
| **Stock avatar** | Browse 1,100+ avatars → filter: Female / South Asian / Professional | Included in Creator | Starting out, testing formats |
| **Custom avatar** *(recommended)* | Record 2–5 min consent video → upload to HeyGen Avatar Studio | Included in Creator | Brand consistency, spokesperson identity |

> ⚠️ Custom avatar consent statement: *"I, [name], consent to HeyGen creating an AI avatar in my likeness for use by Trulo Foods."*

**Step 7 — Create a Brand Template**
```
Aspect ratio:   9:16 (Reels/Shorts) + save a 16:9 version (YouTube)
Background:     Warm cream / off-white gradient OR brand BG image
Avatar position: Centre frame, slightly right of middle
Captions:       ON by default — white text, black outline, bottom-third
Resolution:     1080p
Brand watermark: Trulo logo top-right (upload once)
```

---

## Pre-Production

*20–30 min per video*

### Step 1 — Define the video brief

Answer before writing a word:
- **Video type:** Product explainer / Social ad / Brand story / Recipe tip / Ingredient spotlight
- **Platform:** Instagram Reels · YouTube Shorts · YouTube long-form · Website embed
- **Target length:** 30 sec · 60 sec · 90 sec · 3 min
- **One goal:** What is the single thing the viewer should know/do after watching?
- **CTA:** Link in bio / Buy now / DM us / Comment below / Visit trulofoods.com

### Step 2 — Write the script

~130 words = 60 seconds at natural Indian English pace.

| Section | Timing | Content |
|---------|--------|---------|
| **HOOK** | 0–3 sec | 1 punchy sentence. States the problem or bold claim. *e.g. "Most energy bars are just candy in disguise."* |
| **SETUP** | 3–10 sec | Who you are / what this video is about. One sentence max. |
| **VALUE BODY** | 10–45 sec | 2–3 points max. Each = 1–2 sentences. Simple, conversational. No jargon. |
| **PROOF** | 45–55 sec | One specific, credible detail — an ingredient, a stat, a real outcome. |
| **CTA** | 55–60 sec | One clear action. Tie back to the hook. *e.g. "Try Trulo — link in bio."* |

> 💡 Read aloud and time it. If it feels rushed, cut — don't speed up. Add pronunciation guides for product names: *[troo-loh]*.

### Step 3 — Script sign-off

One person reviews: factual accuracy, brand tone, claim compliance, CTA clarity.
**Do NOT generate voice until the script is locked — re-generating wastes credits.**

> ⚠️ FSSAI compliance: No disease-prevention or cure claims (e.g., "cures diabetes"). Stick to: "high protein," "natural ingredients," "no added sugar."

---

## Voice Generation

*(ElevenLabs · ~10–20 min per video)*

**Step 1 — Open Studio and select voice clone**
[elevenlabs.io/studio](https://elevenlabs.io/studio) → New Project → Select *Trulo — [Name] (Indian EN)* → Set model to **Multilingual V3**.

**Step 2 — Paste approved script and add SSML pauses**
```
Short pause (comma):    <break time="0.3s"/>
Sentence pause:         <break time="0.6s"/>
Section transition:     <break time="0.9s"/>
# Or use ellipsis (...) — ElevenLabs reads these as pauses
```
> 💡 Add a 0.5s pause right after the hook line. Viewers need a half-beat to register the claim.

**Step 3 — Generate and review**

Pass criteria:
- ✅ Sounds like a real person — warm, confident, clear
- ✅ Product names and brand name pronounced correctly
- ✅ Total duration matches target length (±5 sec)
- ✅ No robotic cadence or rushed sections

> ⚠️ If pronunciation is off, use ElevenLabs' phonetic spelling override. For "Trulo" enter *troo-loh*.

**Step 4 — Export**
Download → MP3, 192 kbps.
File naming: `trulo_[content-type]_[YYYYMMDD]_v1.mp3`
Example: `trulo_product-explainer_20260525_v1.mp3`

---

## Avatar Production

*(HeyGen · ~15–25 min per video)*

**Step 1 — Open HeyGen and load Brand Template**
[app.heygen.com](https://app.heygen.com) → Video Studio → Open saved Trulo Brand Template.

**Step 2 — Select avatar**
Pick your custom avatar (or chosen stock avatar). Use Avatar IV or V model — do not use older models.

**Step 3 — Upload ElevenLabs audio and disable HeyGen voice**
Audio panel → Upload Audio → select your MP3.
**Set HeyGen voice to "None / Upload Audio."** Do not let HeyGen generate or blend its own voice.

> ⚠️ Most critical step. If HeyGen voice is accidentally left on, your Indian English accent gets replaced. Always verify the audio source in the preview before rendering.

**Step 4 — Preview lip-sync**
Watch a 5–10 second clip. Pass criteria:
- ✅ Lips close on stop consonants (p, b, m)
- ✅ Open on wide vowels (aa, a)
- ✅ No half-second lag between audio and mouth movement

**Step 5 — Set background and overlays**
```
Background options:
  1. Solid brand colour (simplest)
  2. Blurred kitchen / food scene (warm, on-brand)
  3. Gradient (off-white to warm cream — Trulo palette)

Overlays:
  • Trulo logo watermark (top-right, 60% opacity)
  • Product name text card (bottom-left, if product explainer)
  • CTA banner in last 5 seconds (e.g. "trulofoods.com")
```

**Step 6 — Enable and style captions**
Captions → Auto-generate from audio → Correct any mis-transcriptions (especially "Trulo").
```
Style:             Bold white, 36–42px, bottom third
Background:        Semi-transparent dark pill
Max words/line:    5–6 words
Always correct:    "trulo" → "Trulo", all product names
```
> 💡 ~85% of Instagram Reels are watched without sound. Captions are not optional.

**Step 7 — Render and download**
Render → 1080p → MP4.
File naming: `trulo_[type]_[platform]_[YYYYMMDD]_v1.mp4`
Example: `trulo_product-explainer_reels_20260525_v1.mp4`

---

## Post-Production

*(~10–20 min per video)*

**Step 1 — Run the QA checklist** (see next section)
Watch full video on a mobile screen. Fix before publishing.

**Step 2 — Optional light trim in CapCut / InShot (free)**
If trimming a pause at start/end, or adding a product B-roll cutaway, import the HeyGen MP4 into CapCut.
> 💡 Common edit: add a 0.5s static product shot at the very end, after the CTA, before the video loops.

**Step 3 — Write platform copy**

| Element | Notes |
|---------|-------|
| Hook line | Mirrors the video hook — shows in feed before "more" |
| Body (2–3 lines) | Brief expansion of the video's key point. Human tone. |
| CTA | Single action: "Link in bio" / "DM 'TRULO' for 10% off" |
| Hashtags | 5–8 tags: mix broad (#healthyfood) + niche (#cleaneating) + brand (#TruloFoods) |

**Step 4 — Upload specs by platform**
```
Instagram Reels:   9:16, 1080×1920, MP4, max 90 sec. Add cover thumbnail.
YouTube Shorts:    9:16, 1080×1920, MP4. Include #Shorts in title.
YouTube long-form: 16:9, 1920×1080, MP4. Upload custom thumbnail.
LinkedIn:          1:1 or 16:9. Add captions file or rely on auto-captions.
```

**Step 5 — Archive project files**
Save to: `Trulo / Avatar Videos / [YYYY-MM] / [Video Name]`
Folder contents: approved script doc · ElevenLabs MP3 · HeyGen MP4 · published post URL

---

## QA Checklist

*Watch on a phone, full screen. Fix every item before publishing.*

### 🎙️ Audio
- [ ] Voice sounds like natural Indian English — no American vowel shift or robotic cadence
- [ ] Product name and brand name ("Trulo") pronounced correctly
- [ ] Audio is clean — no background noise, hiss, or clipping
- [ ] Pacing feels natural — pauses between sentences, not rushed
- [ ] Volume is consistent throughout

### 👁️ Visual / Avatar
- [ ] Lip-sync is accurate — lips match audio on consonants and vowels
- [ ] No visual glitches — no stuttering, frozen face, or pixelation
- [ ] Avatar framing is correct — head centred, not cut off
- [ ] Background looks clean and on-brand
- [ ] Trulo logo watermark is visible but not intrusive

### 📝 Captions
- [ ] Captions are present and synced throughout the entire video
- [ ] All product and brand names spelled correctly ("Trulo" not "trulo")
- [ ] Caption text is readable on both light and dark backgrounds
- [ ] No caption overlaps with logo or CTA overlay

### 📋 Content
- [ ] Hook lands in first 3 seconds
- [ ] Script matches approved version
- [ ] No unsubstantiated health claims (FSSAI compliance)
- [ ] CTA is clear and appears in the final 5 seconds
- [ ] Video duration matches target length (±5 sec)

### 📐 Technical
- [ ] Exported at 1080p (not 720p)
- [ ] Aspect ratio matches target platform
- [ ] No HeyGen watermark present (confirm Creator plan is active)
- [ ] File size reasonable for upload (<500 MB for a 60-sec video)

---

## Cost Tracker

### Monthly costs

| Tool | Plan | Cost/mo | Included | Upgrade trigger |
|------|------|---------|----------|----------------|
| ElevenLabs | Creator | $11 | 100K credits ≈ 90 min audio · Pro voice clone · 192 kbps | Upgrade to Pro ($99) when >50 min voiceover/mo |
| HeyGen | Creator | $24 | 200 gen credits ≈ 10 min Avatar IV video · Custom avatar · No watermark | Upgrade to Pro ($99) when >10 min avatar video/mo (~8–10 videos) |
| CapCut | Free | $0 | Trim, basic cuts, B-roll overlay | n/a |
| **Total (entry)** | | **~$35/mo** | ~8–10 × 60-sec videos/mo | |
| **Total (scaled)** | | **~$198/mo** | ElevenLabs Pro $99 + HeyGen Pro $99 · ~40–50 videos/mo | |

### Cost per video
- Entry stack ($35/mo, 8 videos): **~$4.40/video**
- Scaled stack ($198/mo, 50 videos): **~$3.96/video**
- Traditional shoot equivalent: **₹15,000–₹50,000/video**
- Saving vs. traditional: **>95% cost reduction**

### HeyGen credit maths (Creator plan)
- 200 gen credits / month included
- Avatar IV = 20 credits / minute = **10 minutes of video / month**
- Extra credits: $15 / 300 credits = 15 extra minutes
- Effective extra cost: **$1 / extra minute**

---

## Quick Reference

| Setting | Value |
|---------|-------|
| Script pace | ~130 words = 60 seconds |
| ElevenLabs model | Multilingual V3 (always) |
| ElevenLabs stability | 55–65 |
| Similarity boost | 75–80 |
| Style exaggeration | 20–30 |
| Speaker boost | ON |
| HeyGen avatar model | Avatar IV or V only |
| Reels / Shorts format | 9:16 · 1080p · MP4 · captions ON |
| YouTube long-form | 16:9 · 1080p · MP4 |
| Voice file naming | `trulo_[type]_[YYYYMMDD]_v1.mp3` |
| Video file naming | `trulo_[type]_[platform]_[YYYYMMDD]_v1.mp4` |
| Entry budget | ~$35/mo (ElevenLabs $11 + HeyGen $24) |

### The golden rule
> **Always generate audio in ElevenLabs first. Always upload that audio to HeyGen. Never use HeyGen's own voice for Indian English.** This single discipline is what keeps the accent, tone, and brand voice consistent across every video.

---

*Trulo Foods Internal · Talking Head Avatar SOP v1.0 · May 2026*
