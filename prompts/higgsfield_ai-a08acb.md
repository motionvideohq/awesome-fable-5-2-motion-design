# One scene in three hand-painted styles

A Claude Fable 5.2 motion design video by [@higgsfield_ai](https://x.com/higgsfield_ai). [Original post](https://x.com/higgsfield_ai/status/2120005482018750680) · [Watch on MotionVideo](https://motionvideo.xyz/videos/higgsfield_ai-a08acb?utm_source=github&utm_medium=readme&utm_campaign=awesome-fable-5-2-motion-design)

[![One scene in three hand-painted styles](https://assets.motionvideo.xyz/motion/higgsfield-ai-a08acb/poster-15ceedc3c4.jpg)](https://motionvideo.xyz/videos/higgsfield_ai-a08acb?utm_source=github&utm_medium=readme&utm_campaign=awesome-fable-5-2-motion-design)

- **Creator:** [@higgsfield_ai](https://x.com/higgsfield_ai)
- **Model:** Claude Fable 5.2
- **Stack:** Canvas 2D
- **Categories:** Characters and illustration
- **Posted:** 2026-11-10

## Prompt

```text
# Style tests — 8 × 10 s, pure 2D code

Goal: the SAME 10-second mini-scene drawn in 8 different illustration/animation styles, so the client can pick a look for

"The Cloud Shepherd" (a wordless short about a girl and a small cloud spirit). Each test must look like it was entirely

hand-made in that style — painted/drawn, never 3D-rendered, never "vector clip-art". Quality bar: a festival-grade style frame

that moves. Original characters only — no existing film/series characters, logos or famous artworks copied.

## The scene (identical beats in every style, 10.0 s, 1920×1080, 24 fps)

1. 0.0–3.5 s  WIDE: a grassy hill under a big sky, one lone tree on top, wind moving grass/leaves/clouds. A small figure

   (the girl) runs up the slope from the lower left toward the tree.

2. 3.5–6.5 s  MEDIUM: the girl (≈7 y.o., black bob hair, straw hat with a red ribbon, light-blue dress, white collar)

   arrives at the tree, catches her breath, holds her hat in the wind, looks around.

3. 6.5–10.0 s CLOSE-ish two-shot: a tiny white cloud spirit (round puffy body, two dot eyes, pink blush, no mouth or a tiny one)

   peeks from behind the trunk; she sees it, her face lights up; it floats out shyly and settles on the brim of her hat; she laughs.

Hard cuts between the three shots. Camera: locked or a slow smooth drift — no shake, no fast zooms. Characters can animate on

twos (12 fps poses) where that suits the style; wind/clouds smooth.

Interpret the characters FULLY in the style (proportions, line, colour, shapes, pattern) — they must stay recognisable

(bob hair, straw hat w/ red ribbon, blue dress; white puffy cloud spirit) but redesigned for the style.

## Tech

- Your folder: `~/Claude/motion-studio/films/style-tests/<slug>/` with `index.html` + any js modules. Canvas2D (or SVG) only.

  No three.js / WebGL 3D. Offscreen canvases for heavy static paintings (paint once in setup, reuse).

- Contract for the renderer (headless Chrome): the page must define

  `window.HF = { meta: { w: 1920, h: 1080, fps: 24, duration: 10 }, isReady: false, seek: async (t) => { drawFrame(t) } }`

  and set `HF.isReady = true` when ready. Every frame is a PURE function of t (seeded rng, never Math.random/Date/rAF).

- Stills: `cd ~/Claude/motion-studio && node engine/render.mjs films/style-tests/<slug>/index.html --stills 1,4.5,8,9.5 --outdir /tmp/st_<slug>`

  Look at them (Read the PNGs) and iterate until it really looks like the style — at least 3 rounds of self-critique against

  what a real artist of that style would draw.

- Final: `node engine/render.mjs films/style-tests/<slug>/index.html --mb 1 --workers 4 --crf 16 --out films/style-tests/<slug>/<slug>.mp4`

- Frame cost < 200 ms. Fonts: none needed (no on-screen text — the lead adds labels).

- Shared helpers you MAY copy from (not required): `~/Claude/motion-studio/films/cloud-shepherd-2d/lib/paint.js` (watercolor wash,

  pencil strokes, grass field, crowns, cumulus), `lib/time.js` (easing, rng, noise). Don't edit files outside your folder.

## Report back (short)

Path to the mp4, 3–5 lines on the style decisions (palette, line, texture, motion), and what is still weak.
```

More Claude Fable 5.2 motion design, each with its prompt: [motionvideo.xyz/model/fable-5-2](https://motionvideo.xyz/model/fable-5-2?utm_source=github&utm_medium=readme&utm_campaign=awesome-fable-5-2-motion-design)
