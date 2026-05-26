# How to Produce a Talking Head Video
**From raw idea → ElevenLabs audio → HeyGen lip-synced video**

---

## Overview

**Stack:** `/video-idea` skill → ElevenLabs (audio) → HeyGen (avatar + lip-sync) → CapCut (optional trim)
**Time per video:** ~45–90 minutes end-to-end
**Cost:** ~$35/mo at entry volume (~8–10 × 60-sec videos/month)

---

## Step 0 — Run the `/video-idea` skill

Before touching any tool, run this Claude Code slash command with your raw script.

### What is `/video-idea`?

A Claude Code slash command at `D:\Intern\Trulo\.claude\commands\video-idea.md` that converts a raw, human-written script into a complete production package. It handles the planning work so you go into ElevenLabs and HeyGen with everything already decided.

### What it does (automatically, in order)

1. **Parses your input** — separates spoken narration from visual direction notes
2. **Creates a new idea folder** — auto-numbered (`idea_N_[topic]/`) inside the SOP directory
3. **Saves your raw script** verbatim as `rudimentary_script`
4. **Writes a TTS-optimized script** as `text_to_speech` — cleaned for spoken delivery, with pause markers added, FSSAI compliance checked, and phonetic guides for brand names
5. **Reads the visual asset inventory** and maps each scene to an existing image (or flags gaps)
6. **Writes a full `README.md`** containing:
   - Scene-by-scene animation breakdown (table with timestamps and spoken lines)
   - New element generation prompts (Midjourney / DALL-E 3) for any missing assets
   - AI video animation prompts (Runway Gen-3 / Kling / Luma) for every scene
   - Assembly order (which clip plays when, avatar vs. fullscreen cutaway)
   - Asset checklist (what's ready vs. what needs generation)

### How to run it

```
/video-idea [paste your raw script here]
```

Or just type `/video-idea` and paste the script when prompted.

### What you get out of it

```
idea_N_[topic]/
  ├── rudimentary_script     ← your raw input, saved verbatim
  ├── text_to_speech         ← TTS-ready script, go straight into ElevenLabs
  └── README.md              ← full animation plan, prompts, asset checklist
```

**The `text_to_speech` file is your ElevenLabs input for Step 2.**
**The `README.md` is your visual production brief for the animation layer.**

### What a rudimentary script looks like

A raw script typically has two things mixed together:

| What you have | What it becomes |
|---------------|-----------------|
| **Spoken text** — what the avatar says | → `text_to_speech` file (ElevenLabs input) |
| **Visual direction** — what the video looks like | → Animation plan in `README.md` (HeyGen/Kling/Runway) |

The skill separates these automatically. If your script is pure narration with no visual notes, that is fine — it proceeds with narration only.

> **When NOT to run `/video-idea`:** If you already have a polished, TTS-ready script and no animation layer (pure talking head, no cutaways), skip this step and go straight to Step 1.

---

## Step 1 — Review and lock the TTS script

Open the `text_to_speech` file the skill created. Read it aloud before proceeding.

### Rules the skill enforces (verify they were applied)

1. **One idea per sentence** — long compound sentences should be split
2. **~130 words = 60 seconds** — check the word count matches your target duration
3. **No parenthetical asides** — everything in the file will be spoken aloud
4. **Phonetic guides** — brand names have square-bracket guides: *Trulo [troo-loh], allulose [al-yoo-lohs]*
5. **Pause markers** present — look for `[PAUSE 0.5s]` after hook, `[PAUSE 0.9s]` between sections
6. **FSSAI compliance** — no disease-prevention or cure language ("cures diabetes", "prevents heart disease"). Valid: "high protein," "no added sugar," "natural ingredients."

### Script structure to verify

| Section | Timing | What it does |
|---------|--------|--------------|
| **HOOK** | 0–3 sec | One punchy line. States the problem or a bold claim. This is what stops the scroll. |
| **SETUP** | 3–10 sec | One sentence: who this is for / what the video covers. |
| **VALUE BODY** | 10–45 sec | 2–3 points. Each point = 1–2 short sentences. Conversational, no jargon. |
| **PROOF** | 45–55 sec | One specific, credible detail — an ingredient, a stat, a mechanism. |
| **CTA** | 55–60 sec | One clear action. Echo the hook. |

**Read it aloud and time it.** If it's over target, cut — don't speed up. The avatar will pace at ~130 wpm naturally.

**Lock the script before moving to Step 2.** Re-generating audio after changes wastes ElevenLabs credits and your time.

---

## Step 2 — Generate the voiceover in ElevenLabs

*(~10–20 min per video)*

### Step 2a — Open ElevenLabs Studio

Go to [elevenlabs.io/studio](https://elevenlabs.io/studio) → New Project → select your saved Trulo voice clone.

Set the model to **Eleven Multilingual v3** — this is the one with the best Indian English output. Do not use the default English-only model.

### Step 2b — Paste the script and convert pause markers to SSML

Paste your `text_to_speech` file. Replace the `[PAUSE Xs]` markers with SSML break tags:

```
[PAUSE 0.3s]  →  <break time="0.3s"/>    ← short pause, like a comma
[PAUSE 0.5s]  →  <break time="0.5s"/>    ← after hook line
[PAUSE 0.6s]  →  <break time="0.6s"/>    ← sentence end
[PAUSE 0.9s]  →  <break time="0.9s"/>    ← section transition
```

Alternatively, use ellipsis `...` in the text — ElevenLabs reads these as natural pauses. Either works; SSML gives more precision.

### Step 2c — Generate and review

Click Generate. Listen to the full output on earphones (not speakers — compression hides issues). Check:

- [ ] Sounds like a real person — warm, confident, clear. Not robotic.
- [ ] Indian English cadence is intact — no American vowel shifts.
- [ ] Product and brand names pronounced correctly.
- [ ] Pacing matches the script's intent — the hook lands with weight, the CTA sounds decisive.
- [ ] Total duration is within ±5 seconds of your target length.

**If pronunciation is off:** Use ElevenLabs' phonetic spelling override (click the word → edit pronunciation). For "Trulo" enter `troo-loh`. For any other brand or ingredient names, spell them phonetically.

**If pacing feels rushed:** Add more break tags around that section and regenerate. Keep the script locked — do not edit the words to fix pacing.

### Step 2d — Export the audio

Download → **MP3, 192 kbps**.

Save with this naming convention:
```
trulo_[content-type]_[YYYYMMDD]_v1.mp3

Example:
trulo_glucose-spike_20260526_v1.mp3
```

This MP3 goes directly into HeyGen in the next step.

---

## Step 3 — Build the talking head video in HeyGen

*(~15–25 min per video)*

### Step 3a — Open HeyGen and load the Brand Template

Log in at [app.heygen.com](https://app.heygen.com) → Video Studio → open your saved Trulo Brand Template.

### Step 3b — Select the avatar

In the avatar panel, select your custom Trulo avatar (or chosen stock avatar). Confirm the framing looks correct in the preview. For explainer-style videos, use the **upper body** framing — it allows natural-feeling gestures and feels less static than a tight headshot.

Always use **Avatar IV or V** — do not use older models. Quality is visibly worse on older versions.

### Step 3c — Upload the ElevenLabs audio

This is the most critical step in the entire workflow.

Audio panel → **Upload Audio** → select your exported MP3.

**Set HeyGen's own voice to "None / Upload Audio."** The lip-sync engine will now drive the avatar's mouth movements from your ElevenLabs audio. This is how the Indian English accent stays intact.

> If you accidentally leave HeyGen's voice generator active, it generates a different voice and your accent gets replaced. Always verify this setting before rendering — check that the audio source shown in the panel is your uploaded file, not a HeyGen-generated voice.

### Step 3d — Preview the lip-sync

Use HeyGen's preview function to watch a 5–10 second clip. Check:

- [ ] Lips close on stop consonants — **p**, **b**, **m**
- [ ] Lips open wide on broad vowels — **aa**, **a**
- [ ] No visible lag between when you hear a word and when the mouth moves

If the sync looks off, try re-uploading the audio normalised to -3 dB (use Audacity or an online normalizer). Do not re-record — the audio is usually fine; the upload level is the issue.

### Step 3e — Set the background and overlays

Background options:
```
Option 1:  Solid warm cream — clean, no distraction, good for captions
Option 2:  Blurred kitchen / food scene — on-brand for Trulo content
Option 3:  Off-white to warm gradient — versatile, platform-neutral
```

Overlays to add:
```
• Trulo logo watermark — top-right corner, ~60% opacity
• Topic text card (optional) — e.g. "Why You Crash After Lunch" bottom-left
• CTA banner in last 5 seconds — e.g. "trulofoods.com" or "Link in bio"
```

> For videos with animation cutaways (flagged in the README.md from `/video-idea`), those clips are assembled in CapCut in Step 4 — not in HeyGen.

### Step 3f — Enable and style auto-captions

Captions → Auto-generate from audio → review every line for mis-transcriptions.

Common corrections to always make:
- `trulo` → `Trulo`
- `allulose` → `Allulose`
- Any other product or ingredient names

Caption style:
```
Font:            Bold white, 36–42px
Background:      Semi-transparent dark pill behind text
Position:        Bottom third
Max words/line:  5–6 words
```

~85% of Instagram Reels are watched without sound. Captions are not optional — they are the primary read path for most viewers.

### Step 3g — Render and download

Click **Render → 1080p → MP4**. Rendering takes 2–5 minutes per minute of video.

Save with this naming convention:
```
trulo_[type]_[platform]_[YYYYMMDD]_v1.mp4

Examples:
trulo_glucose-spike_reels_20260526_v1.mp4
trulo_glucose-spike_shorts_20260526_v1.mp4
```

---

## Step 4 — Optional: Light trim and animation assembly in CapCut

HeyGen doesn't support edits after rendering. Use CapCut (free, web or mobile) if you need to:

- Trim a silence at the start or end
- Insert animation cutaways — use the animation clips from the README.md plan (generated in Runway/Kling/Luma)
- Add a product shot or B-roll at the end after the CTA

**How to assemble with cutaways:**
1. Import the HeyGen MP4 as the main layer
2. At each cutaway point from the README.md assembly order, split the timeline and insert the animation clip as a fullscreen layer
3. The talking head audio continues under all cutaways — do not mute it
4. Do not recolour or apply skin-tone filters to the avatar — it breaks realism

Common light edit: add a 0.5-second static product image after the CTA so the frame lands before the video loops.

---

## Step 5 — QA before publishing

Watch the full video on a phone at full screen — the actual viewer experience. Fix every item before publishing.

### Audio
- [ ] Voice sounds like natural Indian English — no American vowel shift or robotic cadence
- [ ] Product name and "Trulo" pronounced correctly
- [ ] Audio is clean — no background noise, hiss, or clipping
- [ ] Pacing feels natural — pauses between sentences, not rushed
- [ ] Volume is consistent throughout

### Visual / Avatar
- [ ] Lip-sync is accurate — lips match audio on consonants and vowels
- [ ] No visual glitches — no stuttering, frozen face, or pixelation
- [ ] Avatar framing is correct — head not cut off at top or side
- [ ] Background looks clean and on-brand
- [ ] Trulo logo watermark visible but not intrusive

### Captions
- [ ] Captions present and synced throughout
- [ ] All product and brand names spelled correctly
- [ ] Caption text readable on both light and dark backgrounds
- [ ] No caption overlap with logo or CTA overlay

### Content
- [ ] Hook lands in first 3 seconds
- [ ] Script matches approved version — no unreviewed ad-libs
- [ ] No unsubstantiated health claims (FSSAI compliance)
- [ ] CTA is clear, in the final 5 seconds

### Technical
- [ ] Exported at 1080p
- [ ] Aspect ratio matches target platform (9:16 for Reels/Shorts; 16:9 for YouTube)
- [ ] No HeyGen watermark (confirm Creator plan is active)

---

## Step 6 — Publish

Write the platform caption before opening the app — reduces ad-libbing.

| Element | Notes |
|---------|-------|
| Hook line | Mirror the video's opening line — this is what shows in the feed before "more" |
| Body (2–3 lines) | Brief expansion of the key point. Conversational tone. |
| CTA | Single action: "Link in bio" / "DM 'TRULO' for 10% off" |
| Hashtags | 5–8 tags: mix broad (#healthyfood) + niche (#cleaneating) + brand (#TruloFoods) |

Upload specs:
```
Instagram Reels:   9:16, 1080×1920, MP4, max 90 sec. Add cover thumbnail.
YouTube Shorts:    9:16, 1080×1920, MP4. Include #Shorts in the title.
YouTube long-form: 16:9, 1920×1080, MP4. Upload a custom thumbnail.
LinkedIn:          1:1 or 16:9. Enable auto-captions.
```

---

## Step 7 — Archive the project

Save everything to:
```
Trulo / Avatar Videos / [YYYY-MM] / [Video Name] /
  ├── approved-script.md
  ├── trulo_[topic]_[YYYYMMDD]_v1.mp3      ← ElevenLabs output
  ├── trulo_[topic]_[platform]_[YYYYMMDD]_v1.mp4   ← final video
  └── published-url.txt
```

The idea folder created by `/video-idea` stays in `talking-head-avatar-sop/idea_N_[topic]/` — it is the production brief. The archive folder above is for finished outputs only.

---

## Quick Reference

| Setting | Value |
|---------|-------|
| Script pace | ~130 words = 60 seconds |
| ElevenLabs model | Eleven Multilingual v3 (always) |
| ElevenLabs stability | 55–65 |
| Similarity boost | 75–80 |
| Style exaggeration | 20–30 |
| Speaker boost | ON |
| HeyGen avatar model | Avatar IV or V only |
| HeyGen voice setting | None / Upload Audio (always) |
| Audio export format | MP3, 192 kbps |
| Video export format | MP4, 1080p |
| Reels / Shorts | 9:16, 1080×1920 |
| YouTube long-form | 16:9, 1920×1080 |
| Audio file naming | `trulo_[topic]_[YYYYMMDD]_v1.mp3` |
| Video file naming | `trulo_[topic]_[platform]_[YYYYMMDD]_v1.mp4` |
| Monthly cost (entry) | ~$35/mo (ElevenLabs $11 + HeyGen $24) |

---

## The one rule to never break

**Always generate audio in ElevenLabs first. Always upload that audio to HeyGen. Never let HeyGen generate or blend its own voice.**

HeyGen's built-in voice clone drifts toward an American inflection mid-video. Your Indian English accent — and Trulo's brand voice — stays locked only when the avatar lip-syncs to audio you produced in ElevenLabs.

---

*Trulo Foods Internal · Talking Head Avatar Production Guide v1.0 · May 2026*
