# Prompt recipes

Start every prompt with `references/style-prompt.md` verbatim, then append one of these topic sentences. Do not rewrite the style block.

## Blog header / topic banner (`16:9`)

```
Editorial collage infographic of [thesis in one clause]: a cut-out [hero] is pasted over overlapping [object 1] and [object 2], with a giant [magnifier/arrow/icon] pointing at [the idea]. Vintage magazine-scan grain on warm beige newsprint, torn clippings and tape, flat vector color blocks, light pop Ben-day dots. Limited editorial palette of cobalt blue, violet, tangerine, and cream; stacked paper layers, wide banner composition, one oversized element on the left/right third.
```

## Topic cover / magazine column (`3:4` or `2:3`)

```
Editorial collage cover illustrating [thesis]: a paper-cut [hero portrait or object] stacked on encyclopedia clippings, geometric shards, and a circular callout around [key symbol]. Print grain and aged fiber, flat outlines, light pop sticker shapes. Cobalt, violet, tangerine, and beige; portrait editorial layout with the hero large and devices orbiting it like footnotes.
```

## Knowledge explainer (`16:9` or `1:1`)

```
Collage infographic explaining [thesis]: cut-out [person or hands] inspects an oversized [metaphor object], surrounded by arrows, a magnifying glass, and diagram fragments on newsprint. Magazine-scan texture, flat vector geometry, limited editorial colors (cobalt, violet, tangerine, cream). Composition reads left-to-right as "question → device → idea", layers pasted, not a 3D scene.
```

## Restyle existing image (`image_edit`)

```
Restyle this into an editorial collage infographic illustration: keep the subject, convert it into cut-out paper layers on newsprint with magazine-scan grain, flat color blocks, and one explanatory device (magnifier or arrows). Limited palette of cobalt blue, violet, tangerine, and warm beige. Same framing.
```

When a style-anchor file exists, pass `assets/style-anchor.jpg` as an extra reference and say: `match this collage-paper grain, flat blocks, and editorial palette`.
