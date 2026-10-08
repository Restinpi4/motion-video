# Hyperframes Composition Brief: 安见 Kinsight — 40s version (working name)

## Objective
Create a short, polished launch-style brag video for Kinsight, a licensed in-home senior care
platform idea for the US.

## Output
- Composition directory: `brag-output-2026-10-08-141941/composition/`
- Rendered video: `brag-output-2026-10-08-141941/brag.mp4`
- Format: landscape — 1920x1080, 30fps
- Duration: 41.5s (founder asked for ~40s)

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
  - 离开之后，/ 洗澡认真吗？饭菜用心吗？
  - 重点片段，/ 饭有没有好好做，一看就知道。
  - 订单更多，/ 收入也更多。
  - 三方都受益。
  - 婴儿潮一代正在变老，/ 上门照护的需求，只会越来越大。
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
Use the storyboard and copy table in `brag-output-2026-10-08-141941/brag-plan.md` as the creative contract (12 scenes).

1. Hook — 0.00–3.27 — 你不可能每次都在场。 + day ruler
2. Problem — 3.27–6.56 — 离开之后，洗澡认真吗？饭菜用心吗？ + unseen hours
3. Reveal — 6.56–9.83 — 现在，每一次都看得见。 + phone: visit in progress
4. AI highlights — 9.83–13.64 — scanned timeline, 3 clip cards
5. Rewatch — 13.64–16.93 — tap lunch clip, player with AI tags + key frames
6. Live — 16.93–20.19 — live feed, typed instruction, reply, glass of water
7. Booking — 20.19–23.46 — caregiver cards with stars, tap, booked
8. Checkup — 23.46–26.74 — baseline vs follow-up bars, report ready
9. Caregivers — 26.74–30.01 — new orders arrive, week fills up
10. Three parties — 30.01–34.38 — 子女 / 老人 / 护理员 cards
11. Why now — 34.38–37.65 — 婴儿潮一代正在变老 + homes light up
12. Outro — 37.65–41.50 — wordmark on 38.20 strong cue, tagline

## Audio
- Audio role: warm bed + sparse professional accents
- Audio arc: steady bed from the first frame, small UI ticks through the app beats, one bell
  under the wordmark, fade out
- Music: `assets/music/happy-beats-business-moves-vol-12-by-ende-dot-app.mp3`
- Music treatment: volume ~0.32; 0.5s fade-in; fade out 39.9→41.5; master to about −17 LUFS
- Music cue guidance: bundled preset
  `.claude/skills/brag/assets/music/cues/happy-beats-business-moves-vol-12-by-ende-dot-app.music-cues.json`.
  Locks: 24.56 (report), 27.30 (new order), 38.20 (logo). Beat grid: 10.93/11.46/12.02 (clip cards),
  14.20 (tap), 17.47 (send), 18.02 (reply), 21.84 (tap), 31.10/31.65/32.19 (cards), 35.47–37.11 (homes).
- Audio-reactive treatment: subtle; bass/RMS breathes the terracotta glow and REC dot
- Audio-coupled moments: phone landing; 3 clip cards; clip tap; message send + reply; booking tap; new order; wordmark
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
