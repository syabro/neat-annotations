# neat-annotations

Neat hand-drawn CSS annotations: arrows and handwritten labels pointing at things on your page. Pure CSS, no JavaScript, no build step — one self-contained file.

**[Demo →](https://syabro.github.io/neat-annotations/)**

## Use

Copy [`neat-annotations.css`](neat-annotations.css) into your project, or hotlink it:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/syabro/neat-annotations/neat-annotations.css">
```

Labels look best with [Shantell Sans](https://fonts.google.com/specimen/Shantell+Sans) (optional — falls back to system `cursive`):

```html
<link href="https://fonts.googleapis.com/css2?family=Shantell+Sans:wght@400;500;600&display=swap" rel="stylesheet">
```

Then wrap any inline element:

```html
<span class="ann ann-n ann-amber" data-note="open task">[ ]</span>
```

## API

Combine three things: the base class, a direction, and (optionally) a color. The note text comes from the `data-note` attribute.

**Directions** — where the arrow points (`ann-n` points north, so the annotation sits below its target):

`ann-n` `ann-ne` `ann-e` `ann-se` `ann-s` `ann-sw` `ann-w` `ann-nw`

**Colors** — default is a warm gray:

`ann-amber` `ann-blue` `ann-green` `ann-red` `ann-purple`

**CSS variables** — set them on the element for fine-tuning:

| Variable | Default | What it does |
| --- | --- | --- |
| `--ann-color` | warm gray | arrow, label and highlight color |
| `--ann-font` | `'Shantell Sans', cursive` | label font |
| `--ann-target-gap` | `5px` | gap between target and arrow |
| `--ann-label-gap` | `6px` | gap between arrow and label |
| `--ann-lower-label-gap` | `-4px` | adjustment for labels below the target |
| `--ann-arrow-x` / `--ann-arrow-y` | `0px` | nudge the arrow |
| `--ann-text-x` / `--ann-text-y` | `0px` / `5px` | nudge the label |
| `--ann-rotate` | `-4deg` | label tilt |

Annotations are positioned outside the element and don't reserve space — give annotated lines some breathing room (margins).

## License

MIT
