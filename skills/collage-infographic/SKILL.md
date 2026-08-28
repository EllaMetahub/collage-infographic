---
name: collage-infographic
description: >
  Generate editorial collage infographic illustrations (拼贴感信息图插画)
  mixing vintage paper media, flat vector, and light pop. Use when the user
  asks for collage infographic, editorial illustration, magazine-scan collage,
  blog header, topic cover, knowledge explainer art, 拼贴插画, 信息图插画,
  编辑式插画, 复古纸媒配图, or runs /collage-infographic.
metadata:
  short-description: "Editorial collage infographic illustration"
  author: EllaMetahub
  version: "1.0.0"
argument-hint: topic or viewpoint to illustrate
license: MIT
compatibility: Requires Grok Imagine image_gen and image_edit
---

# Collage Infographic Illustration

Generate **editorial collage infographic** images: cut-and-paste paper layers that
explain one idea. Not a painted scene, not a photoreal photo, not a data chart.

Follow the `imagine` skill for `image_gen` / `image_edit`, real-people references,
and when to build exact text or data in code instead of generating it.

Load `references/palettes.md` only when picking a named palette other than Default.
Load `references/recipes.md` only when matching a specific format (header, cover, explainer).

Style anchors (pass to `image_edit` to lock the look):

- `assets/style-anchor.jpg` — Default editorial, `16:9`
- `assets/style-anchor-encyclopedia.jpg` — Encyclopedia palette, `3:4`

## Tool choice

| Need | Tool |
|------|------|
| Look / mood / concept art | `image_gen` (this skill) |
| Restyle, iterate, keep the collage look | `image_edit` seeded from the previous image or `assets/style-anchor.jpg` |
| Exact headline, numbers, chart values, readable labels | HTML/CSS overlay on top of the illustration — do not ask the image model to typeset them |
| Named real person | `image_edit` with a real photo reference (imagine skill) |

If the user wants a true infographic with correct labels, generate the collage as the visual field, then set type in code.

## Style contract (every image)

Lock all five. If one is missing, the image is off-style.

1. **Collage construction** — people, objects, and textures look cut out and pasted. Overlapping layers, torn or hard-cut edges, tape/glue presence. Depth comes from stacking, not vanishing-point perspective.
2. **Paper / print texture** — magazine-scan grain, newsprint speckle, aged fiber, slight misregistration. Encyclopedia / newspaper / column-illustration atmosphere.
3. **Flat vector + light geometry** — clean outlines, solid color blocks. No cinematic lighting, no realistic skin pores, no 3D product render. Concept, not observation.
4. **Info-viz thinking** — the picture explains a viewpoint. Include at least one explanatory device: magnifier, arrow, oversized icon, diagram shard, callout circle, scale contrast.
5. **Limited high-contrast editorial palette** — few colors, high recognition. Default: cobalt / violet / tangerine / beige / cream / charcoal. See `references/palettes.md`.

Light pop is a *seasoning*: Ben-day dots, one sticker-like shape, one exaggerated scale jump. Do not turn the image into a Lichtenstein pastiche or a comic page.

## Prompt recipe

Own the prompt unless the user supplied one verbatim. 2–5 sentences, prose, positive description.

Order: **subject (the idea) → collage pieces → paper field → style words → composition → palette.**

Always include this style spine (adapt, do not drop):

> editorial collage infographic illustration; cut-out paper figures and objects pasted in overlapping layers; vintage magazine-scan grain and newsprint texture; flat vector color blocks with clean outlines; light pop graphic devices; limited editorial palette of cobalt blue, violet, tangerine, and warm beige

Then fill:

- **One thesis** — what viewpoint is being explained (one sentence).
- **3–7 collage pieces** — hero subject + 1–2 explanatory devices + 1–2 paper textures (torn clipping, graph shard, tape, halftone).
- **Field** — cream/beige newsprint, encyclopedia page, or editorial board. Not a sky-and-ground landscape.
- **Composition** — stacked layers, off-center hero, one oversized element. Asymmetric editorial layout.
- **Aspect ratio** — from the table below.

Do not write keyword-tag soup. Do not list a long "no photoreal, no 3D, no…" block; state the collage/paper/flat look instead.

### Aspect ratio

`image_gen` accepts `1:1`, `3:4`, `4:3`, `9:16`, `16:9`, `2:3`, `3:2`. Do not pass `4:5`.

| Use | Ratio |
|-----|--------|
| Blog header, topic banner, YouTube / article hero | `16:9` |
| Social square, avatar-adjacent card | `1:1` |
| Phone story, poster story | `9:16` |
| Magazine column, Pinterest, cover-like | `3:4` or `2:3` |
| Unspecified editorial illustration | `16:9` |

## Workflow

1. Extract the **one idea** to explain. If the request is a vague topic, pick a concrete visual metaphor and state it before generating.
2. Cast collage pieces (hero + devices + paper textures). Name them in the prompt.
3. Choose palette (Default unless the user names a mood). Choose aspect ratio.
4. If a series, or the user attached a reference: start from that image / `assets/style-anchor.jpg` with `image_edit`. Otherwise `image_gen`.
5. Generate. Read the image back against the checklist below.
6. One targeted `image_edit` if a contract point failed. If exact text is wrong, stop iterating the pixels — overlay type in code.
7. Deliver the image path and a one-line note of the thesis + palette + ratio.

## Verification (pass/fail)

Describe what the image actually shows, then score:

- Cut-and-paste layers visible (not a continuous scene)
- Paper grain / newsprint / scan texture present
- Flat blocks + clean outlines (not photoreal light)
- At least one explanatory device (magnifier, arrow, symbol, scale jump)
- Palette is limited and editorial (blue / violet / orange / beige family, or the named variant)
- Reads as explaining an idea, not telling a story scene

Any fail → one `image_edit` restating the missing contract point. Do not "good enough" a cinematic 3D render.

## Series

First image is the look master. Every follow-up is `image_edit` from that master (or from `assets/style-anchor.jpg` plus the master). Restate the five contract points in each edit prompt. Do not `image_gen` a "matching" sibling from scratch.
