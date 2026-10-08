# Hyperframes Composition Brief: Kinsight (working name)

## Objective
Create a short, polished launch-style brag video for Kinsight, a licensed in-home senior care
platform idea for the US.

## Output
- Composition directory: `brag-output/composition/`
- Rendered video: `brag-output/brag.mp4`
- Format: landscape — 1920x1080, 30fps
- Duration: 23s

## Source Material
- Project root: none (pre-product idea). Source is the founder's written idea in chat.
- Product name: "Kinsight" (placeholder; composition variable `brandName`)
- Tagline / strongest claim: every visit is recorded; AI clips the moments that matter
- Key UI to recreate: the family app (visit in progress, AI highlights, live view with
  instruction, caregiver booking with reviews, before/after checkups)
- Language: Simplified Chinese (founder's request); brand 安见 / KINSIGHT (placeholders)
- Copy that must appear verbatim:
  - 你不可能每次都在场。
  - 现在，每一次都看得见。
  - 几个小时的照护，/ AI 自动剪出关键时刻。
  - 实时观看，/ 随时叮嘱护理员。
  - 护理员你来选，/ 时间你来定，不绑定。
  - 第一天，免费体检。/ 再测一次，进步看得见。
  - 看得见的照护。/ 持牌上门养老服务平台

## Creative Direction
- Tone preset: polished
- Creative direction: a quiet, warm product film for worried adult children; trust, made visible
- Interpretation: few words, long holds, soft staggered transitions, restrained sound
- Angle: answer the adult child's fear ("what happens after I leave?") with the product,
  never by depicting abuse.
- Hook: "You can't be at every visit." over a moving mono day-ruler (9 AM → 3 PM)
- Outro / punchline: Kinsight wordmark, "Care you can see."
- Avoid:
  - Generic SaaS language
  - Abstract filler visuals
  - Invented outcome numbers, ratings counts, or testimonials (stars only, no figures)
  - Real brand names (the Chinese pet-care apps that inspired it, camera makers)

## Visual Identity
- Background: #F3EDE3 (same in every scene), subtle drifting grain
- Text: #1E2B2A; secondary #55615E
- Accent: #B4532A (terracotta, the only accent hue)
- Surface: #FFFCF7; hairline #D8CDBD
- Display font: Noto Serif SC 400/700 (思源宋体; human voice), local glyph subset
- Data font: IBM Plex Mono 400/700 (machine voice: timestamps, REC, AI labels, kickers)
- UI font: Noto Sans SC 400/700 (思源黑体; inside the phone), local glyph subset
- Layout: caption column anchored left; phone as a fixed anchor on the right through scenes 2–6

## Storyboard
Use the storyboard in `brag-output/brag-plan.md` as the creative contract.

1. Hook — 0.00–2.73 — "You can't be at every visit." + day-ruler
2. Reveal — 2.73–6.00 — "Now you can see every one." + phone: visit in progress
3. AI highlights — 6.00–10.37 — scanned timeline, 3 clip cards one by one
4. Live — 10.37–13.64 — live feed, typed instruction, reply, glass of water appears
5. Your caregiver — 13.64–16.38 — caregiver cards with stars, tap, booked
6. Before / after — 16.38–19.66 — checkup bars grow, progress report ready
7. Outro — 19.66–23.00 — wordmark on strong cue, tagline

## Audio
- Audio role: warm bed + sparse professional accents
- Audio arc: steady bed from the first frame, small UI ticks through the app beats, one bell
  under the wordmark, fade out
- Music: `assets/music/happy-beats-business-moves-vol-12-by-ende-dot-app.mp3`
- Music treatment: volume ~0.3; 0.4s fade-in; fade out 21.5→23.0
- Music cue guidance: bundled preset
  `.claude/skills/brag/assets/music/cues/happy-beats-business-moves-vol-12-by-ende-dot-app.music-cues.json`.
  Locks: 19.66 (logo), 17.47 (progress ready). Beat grid: 7.09/8.19/9.29 (clip cards),
  11.46 (send), 12.02 (reply), 15.29 (tap).
- Audio-reactive treatment: subtle; bass/RMS breathes the terracotta glow and REC dot
- Audio-coupled moments: phone landing; 3 clip cards; message send; booking tap; wordmark
- SFX selection guidance: low high-frequency-risk files only, 0.4–0.6 volume
- SFX analysis guidance: `.claude/skills/brag/assets/sfx/sfx-analysis.md`
- Exact SFX choice: chosen after animation (see composition)
- Audio files: copied into `brag-output/composition/assets/`

## Hyperframes Instructions
Built with hyperframes-core / -animation / -creative / -keyframes / -cli. /brag owns the story;
Hyperframes owns structure and timing. Requirements:
- Show real (mock) product UI; keep all text readable; stay within 15–25s
- Music + sparse SFX; cues bias timing only
- Audio-reactive: pre-extracted data, sampled per frame on the one timeline
- `hyperframes check` passes before render
- Keep creation and rendering local; no publishing
