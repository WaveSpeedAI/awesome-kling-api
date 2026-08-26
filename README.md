# Awesome Kling API 🎞️ — Prompts, Variants & One-Call Video Generation

> The most complete open guide to **Kuaishou Kling — the cinematic AI video model (Kling v3.0, o3, motion-control, lipsync, effects)** — a community prompt library and a single API to run every variant.

<p align="center">
  <a href="https://wavespeed.ai/kling-3-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-kling-api"><img src="https://img.shields.io/badge/▶_Run_Kling_3.0-Get_API_Key-00E5FF?style=for-the-badge&labelColor=0B0B0F" alt="Run Kling 3.0"></a>
  <a href="https://wavespeed.ai/kling-o3-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-kling-api"><img src="https://img.shields.io/badge/Kling_o3-Try_Now-7C3AED?style=for-the-badge&labelColor=0B0B0F" alt="Kling o3"></a>
</p>

<p align="center">
  <b>🌊 Powered by <a href="https://wavespeed.ai?utm_source=github&utm_medium=readme&utm_campaign=awesome-kling-api">WaveSpeedAI</a> — serverless Kling API, pay-as-you-go, zero cold starts.</b><br>
  <a href="https://wavespeed.ai/kling-3-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-kling-api"><b>→ Get a Kling 3.0 API key</b></a> &nbsp;·&nbsp; <a href="https://wavespeed.ai/kling-o3-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-kling-api"><b>→ Try Kling o3</b></a>
</p>

<p align="center">
  🖥️ <b>No code?</b> Generate in your browser (no setup, free to start) → <a href="https://wavespeed.ai/video-generator?utm_source=github&utm_medium=readme&utm_campaign=awesome-kling-api"><b>WaveSpeedAI Video Generator</b></a>
</p>

---

> **Generate right now**
> ```bash
> npm i -g @wavespeed/cli && wavespeed login
> wavespeed run kwaivgi/kling-v3.0-pro/text-to-video -p "your prompt"
> ```
> No GPU, no cold start — the same endpoint powers every prompt below.

---

## 📖 Contents
1. [What is Kling?](#what-is-kling)
2. [Run it via API](#run-it-via-api)
3. [Model Variants](#model-variants)
4. [Prompt Library](#prompt-library) — 11 community prompts
5. [Related Model Guides](#related-model-guides)
6. [Contributing](#contributing)

---

## What is Kling?

**Kling** (by Kuaishou) is a cinematic AI video model known for smooth motion, strong physics, and long-shot coherence. WaveSpeed serves the full lineup — **Kling v3.0** (pro / 4k / turbo), **Kling o3**, motion-control, lipsync, elements, and effects.

---

## Run it via API

One endpoint, submit + poll. Swap the model path for any variant below.

```bash
curl -s -X POST "https://api.wavespeed.ai/api/v3/kwaivgi/kling-v3.0-pro/text-to-video" \
  -H "Authorization: Bearer $WAVESPEED_API_KEY" -H "Content-Type: application/json" \
  -d '{"prompt": "A samurai drawing a katana in slow motion, cherry blossoms, cinematic", "aspect_ratio": "16:9"}'
# → {"data": {"id": "<prediction_id>"}}

curl -s "https://api.wavespeed.ai/api/v3/predictions/<prediction_id>/result" \
  -H "Authorization: Bearer $WAVESPEED_API_KEY"
# → status: completed → outputs: ["<url>"]
```

**[→ Get your Kling 3.0 API key](https://wavespeed.ai/kling-3-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-kling-api)** · pay-as-you-go, live pricing on each model page.

---

## Model Variants

All variants open in-browser with a copy-paste API snippet.

### Kling v3.0 — flagship &nbsp;[▶ API](https://wavespeed.ai/kling-3-api)
[v3.0-pro t2v](https://wavespeed.ai/models/kwaivgi/kling-v3.0-pro/text-to-video) · [v3.0-pro i2v](https://wavespeed.ai/models/kwaivgi/kling-v3.0-pro/image-to-video) · [v3.0-4k](https://wavespeed.ai/models/kwaivgi/kling-v3.0-4k/text-to-video) · [v3-turbo-pro](https://wavespeed.ai/models/kwaivgi/kling-v3-turbo-pro/text-to-video)

### Kling o3 & tools &nbsp;[▶ API](https://wavespeed.ai/kling-o3-api)
[motion-control](https://wavespeed.ai/models/kwaivgi/kling-v3.0-pro/motion-control) · [lipsync](https://wavespeed.ai/models/kwaivgi/kling-lipsync/text-to-video) · [effects](https://wavespeed.ai/models/kwaivgi/kling-effects) · [elements](https://wavespeed.ai/models/kwaivgi/kling-elements)

> Full catalog: **[wavespeed.ai/kling-3-api](https://wavespeed.ai/kling-3-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-kling-api)**

---

## Prompt Library

11 prompts curated from the Kling creator community. Credit stays with the original author. Fill in `{...}` placeholders.

### 1. Cinematic shot of a sunlit Scandinavian bedroom. A seale…
*by [@Salmaaboukarr](https://x.com/Salmaaboukarr)*

```
{
  "description": "Cinematic shot of a sunlit Scandinavian bedroom. A sealed IKEA box trembles, opens, and flat pack furniture assembles rapidly into a serene, styled room highlighted by a yellow IKEA throw on the bed. No text.",
  "style": cinematic",
  "camera": "fixed wide angle",
  "lighting": "natural warm with cool accents",
  "room": "Scandinavian bedroom",
  "elements": [
    "IKEA box (logo visible)",
    "bed with yellow throw",
    "bedside tables",
    "lamps",
    "wardrobe",
    "shelves",
    "mirror",
    "art",
    "rug",
    "curtains",
    "reading chair",
    "plants"
  ],
  "motion": "box opens, furniture assembles precisely and rapidly",
  "ending": "calm, modern space with yellow IKEA accent",
  "text": "none",
  "keywords": [
    "16:9",
    "IKEA",
    "Scandinavian",
    "fast assembly",
    "no text",
    "warm & cool tones"
  ]
}
```

### 2. A woman stands in a completely empty kids bedroom in the…
*by [@StelfieTT](https://x.com/StelfieTT)*

```
{
  "scene and action": "A woman stands in a completely empty kids bedroom in the morning light. A sealed box sits on the floor with the label 'Kids Room in a box'. The box rattles, then opens. Colorful, playful furniture pieces rapidly assemble , snapping, sliding, and unfolding across the room. As a bookshelf clicks into place and the bed rolls in, the girl watches calmly and says, 'Well..." and while the room finishes assembling into a bright, tidy, playful kids space takes her phone out and start scrolling and say "let[s see....husband in a box.... .",
  "camera angle": "fixed static ",
  "lighting": "natural soft morning light",
  "room": "kids bedroom",
  "ratio": "16:9",
"character" : blonde woman
"voice" : joyful and funny
  "furniture": [
    "low bed with animal-print sheets",
    "toy storage",
    "bookshelves",
    "desk and chair",
    "morning light",
    "wall decals",
    "rug",
    "plush toys",
    "bean bag",
    "child’s wardrobe",
    "curtains",
    "carton box with text Kids Room in a box"
  ],
  "action and motion": "box opens, elements move quickly into place, sliding, folding, stacking automatically",
  "keywords": [
    "kids room",
    "no text",
    "fast motion",
    "pastel tones",
    "room kids design"
  ]
}
```

### 3. A dull backyard seen from above. An Amazon package sits …
*by [@techhalla](https://x.com/techhalla)*

```
{
  "scene_description": "A dull backyard seen from above. An Amazon package sits in the center. It opens instantly, triggering a fast, rhythmic transformation: sofas, pergola, fire pit, table, chairs, trees, plants, and lights blop into place, turning the space into a lush, high-end garden.",
  "visual_style": "realistic",
  "camera_movement": "aerial descent, then slow tracking-in as the garden builds",
  "main_subject": "Amazon box triggering the creation of a furnished modern garden",
  "background_setting": "residential backyard",
  "lighting_mood": "warm natural afternoon light",
  "audio_cue": "clean blop sounds for each object; soft ambient nature background"
}
```

### 4. A white classic Vans sneaker floats mid-air, slowly spin…
*by [@techhalla](https://x.com/techhalla)*

```
{ "scene_description": "A white classic Vans sneaker floats mid-air, slowly spinning. Suddenly, a burst of vibrant paint splashes across it — black and neon green. The shoe transforms instantly into a bold fashion-forward version in black with acid green details. In the blurred background, a skatepark can be seen, but the focus remains solely on the shoe.", "visual_style": "high-fashion streetwear", "camera_movement": "slow-motion rotation of the sneaker, locked-on shot with shallow depth of field", "main_subject": "Vans sneaker transforming mid-air from classic white to black and neon green", "background_setting": "blurred skatepark with ramps and urban textures", "lighting_mood": "even, soft light with focus on color contrast and texture", "audio_cue": "slow whoosh, paint burst impact, subtle tone shift at the transformation" }
```

### 5. A skateboarder flips a board over a set of stairs in slo…
*by [@techhalla](https://x.com/techhalla)*

```
{ "scene_description": "A skateboarder flips a board over a set of stairs in slow motion. As the board spins, it reveals the Supreme logo underneath. The landing is hard and clean. The logo is reflected in a puddle next to the skater’s feet.", "visual_style": "gritty skate aesthetic", "camera_movement": "360 rotation during kickflip, locked-on landing", "main_subject": "Supreme board in mid-air with logo reveal", "background_setting": "concrete urban plaza", "lighting_mood": "late afternoon city shadows", "audio_cue": "board wheels, air whip, stomp, puddle ripple" }
```

### 6. A photographer points a Canon EOS camera at a tiger walk…
*by [@techhalla](https://x.com/techhalla)*

```
{ "scene_description": "A photographer points a Canon EOS camera at a tiger walking slowly toward frame. The lens clicks — instantly, the scene freezes into a crystal-clear photo. The tiger disappears. Only the image remains, with the Canon logo in the bottom corner.", "visual_style": "wildlife cinematic", "camera_movement": "handheld feel, quick snap to static composition", "main_subject": "Canon camera capturing a wild animal mid-action", "background_setting": "jungle or dry grassland", "lighting_mood": "natural light with rich saturation", "audio_cue": "camera shutter snap, then ambient cutout to silence"}
```

### 7. A circuit board pulses with red energy. Sparks travel ac…
*by [@techhalla](https://x.com/techhalla)*

```
{ "scene_description": "A circuit board pulses with red energy. Sparks travel across its paths until they converge and explode into the ROG logo, which hovers above the board glowing in red and silver.", "visual_style": "futuristic high-tech", "camera_movement": "fast tracking over circuit paths, ending in dramatic logo reveal", "main_subject": "ROG logo forming from energy traveling across circuitry", "background_setting": "dark tech environment", "lighting_mood": "moody dark with neon red highlights", "audio_cue": "electric pulses, deep bass hum, digital spark"}
```

### 8. A torero stands alone in an empty bullring, holding an u…
*by [@techhalla](https://x.com/techhalla)*

```
{
  "scene_description": "A torero stands alone in an empty bullring, holding an ultra-slim LG TV like a shield. The screen shows a vivid, pure red. He shouts 'Hey!' and the camera cuts to a massive black bull. It charges. Right before impact, the scene cuts to solid red. The LG logo appears in white, then the words 'Pure Red'. Finally, the bull crashes through the red screen, shattering it visually.",
  "visual_style": "cinematic",
  "camera_movement": "push-in on torero, whip-pan to bull, sharp cut to red, final VFX screen break from off-screen",
  "main_subject": "torero with LG TV showing pure red, ending with bull breaking the final screen",
  "background_setting": "sunlit empty bullring",
  "lighting_mood": "golden-hour with strong contrast",
  "audio_cue": "wind, torero's shout, bull snort and charge, silence, glass break",
  "dialog": "0:04 — Torero: 'Hey!'\n0:08 — [Bull breaks screen]",
  "subtitles": "OFF"
}
```

### 9. A climber reaches a summit, gasping. As they raise their…
*by [@techhalla](https://x.com/techhalla)*

```
{ "scene_description": "A climber reaches a summit, gasping. As they raise their arms, a sudden gust of wind pushes back their hood — revealing the North Face logo on their shoulder. Quick cut to a wide shot of the climber silhouetted against the sky with the logo clear.", "visual_style": "epic outdoor documentary", "camera_movement": "POV pan + wide drone reveal", "main_subject": "North Face jacket worn during a summit achievement", "background_setting": "mountaintop above clouds", "lighting_mood": "harsh, high-altitude natural light", "audio_cue": "wind roar, breath, short dramatic swell" }
```

### 10. Cinematic close-up of a cold, dewy Corona bottle sitting…
*by [@Ror_Fly](https://x.com/Ror_Fly)*

```
{ "description": "Cinematic close-up of a cold, dewy Corona bottle sitting alone on a weathered beach table. It begins to hum, vibrate. The bottle cap *pops*—and the entire environment unfolds from inside: palm trees rise, lights string themselves, speakers assemble mid-air, sand shifts into a dance floor. A DJ booth builds from driftwood. Music kicks in. A beach rave is born. No text.",
  "style": "cinematic, magical realism", "camera": "starts ultra close, zooms out and cranes overhead as the world expands", "lighting": "sunset turning to neon—golden hour into party glow", "environment": "quiet beach transforms into high-energy beach rave", "elements": [ "Corona bottle (label visible, condensation dripping)", "pop-top cap in slow motion", "exploding citrus slice", "sand morphing into dance floor", "palm trees rising", "neon lights snapping on", "DJ booth building itself", "crowd materializing mid-dance", "fire pit lighting", "surfboards as signage"], "motion": "explosion of elements from bottle, everything assembles in rapid time-lapse", "ending": "Corona bottle in foreground, beach rave in full swing behind it", "text": "none", "keywords": ["Corona", "beach party", "bottle transforms", "rave build", "sunset to night", "cinematic", "no text"] 
}
```

### 11. Apple earbuds appear in flashes over black void. Each fl…
*by [@aziz4ai](https://x.com/aziz4ai)*

```
{
  "video_length": 8,
  "scenes": [
    {
      "start": 0.0,
      "end": 0.7,
      "visual": "Apple earbuds appear in flashes over black void. Each flash reveals angle: top, side, front. Particles burst with light impact.",
      "camera": "snap zooms, hard cuts",
      "sound": "tight bass drops per cut"
    },
    {
      "start": 0.7,
      "end": 2.0,
      "visual": "Case pops open mid-air. Earbuds launch out in sync with beat, glowing rim light follows motion arcs.",
      "camera": "explosive transitions, 3D spin",
      "sound": "fast-paced pulse"
    },
    {
      "start": 2.0,
      "end": 3.5,
      "visual": "Earbuds split apart mid-flight. Internal parts float, orbiting like choreography.",
      "camera": "slow-motion breakaway",
      "sound": "digital glitch rhythm"
    },
    {
      "start": 3.5,
      "end": 5.0,
      "visual": "Floating parts twist and merge into Apple logo. Logo turns pitch black, neon rim lights glow softly.",
      "camera": "cinematic orbit + pull back",
      "sound": "echoing synth + Apple tone"
    },
    {
      "start": 5.0,
      "end": 8.0,
      "visual": "Apple logo holds center with ambient glow. Background fades to deep black. Silence.",
      "camera": "static frame",
      "sound": "quiet fade-out"
    }
  ]
}
```

*Add yours via a PR — keep the original author's credit. See [Contributing](#contributing).*

---

## Related Model Guides
Part of the WaveSpeedAI **Awesome Model** series — one guide per frontier model, all runnable through one API:

- 🎬 [awesome-seedance-api](https://github.com/WaveSpeedAI/awesome-seedance-api) — ByteDance Seedance video
- 🌊 [awesome-wan-api](https://github.com/WaveSpeedAI/awesome-wan-api) — Alibaba Wan video
- ⚡ [awesome-minimax-h3-api](https://github.com/WaveSpeedAI/awesome-minimax-h3-api) — MiniMax Hailuo H3 video
- 🎞️ [awesome-kling-api](https://github.com/WaveSpeedAI/awesome-kling-api) — Kling video *(this repo)*
- 🖼️ [awesome-seedream-api](https://github.com/WaveSpeedAI/awesome-seedream-api) — ByteDance Seedream image
- 🎨 [awesome-gpt-image-api](https://github.com/WaveSpeedAI/awesome-gpt-image-api) — OpenAI GPT Image
- 🍌 [awesome-nano-banana-api](https://github.com/WaveSpeedAI/awesome-nano-banana-api) — Google Nano Banana image

---

## Contributing
PRs welcome:
1. Reusable prompts (`{placeholders}` for swappable parts).
2. **Credit the original author** with a link.
3. No output images unless you own and can license them.

## License
[CC0-1.0](LICENSE) — text & prompts are free to use. Model outputs follow the model provider's and [WaveSpeed](https://wavespeed.ai)'s terms.

---
<p align="center"><sub>Maintained by <a href="https://wavespeed.ai?utm_source=github&utm_medium=readme&utm_campaign=awesome-kling-api">WaveSpeedAI</a> — the fastest way to run frontier image & video models via one API. <a href="https://wavespeed.ai/kling-3-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-kling-api"><b>Run Kling →</b></a></sub></p>
