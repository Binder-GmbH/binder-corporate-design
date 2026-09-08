# Logo files

Download what you need directly from this folder. Rules for using them are in
[../logo.md](../logo.md).

<img src="svg/binder-logo.svg" width="360" alt="BINDER logo">

## Which file to take

| You are doing | Take |
|---|---|
| Website, app, anything on screen | **SVG** — scales to any size |
| Office document, quick placement | **PNG** — transparent background |
| Print, layout, handing to a printer | **PDF** |

## What is here

### SVG

| File | Variant |
|---|---|
| [`binder-logo.svg`](svg/binder-logo.svg) | Red and black, without claim — **the standard version** |
| [`binder-logo-black.svg`](svg/binder-logo-black.svg) | Solid black, without claim |
| [`binder-logo-black-claim.svg`](svg/binder-logo-black-claim.svg) | Solid black, with claim |
| [`binder-logo-white.svg`](svg/binder-logo-white.svg) | Solid white, without claim — for dark backgrounds |
| [`binder-logo-white-claim.svg`](svg/binder-logo-white-claim.svg) | Solid white, with claim |
| [`binder-logo-red-white.svg`](svg/binder-logo-red-white.svg) | Red and white, without claim — for dark backgrounds |
| [`binder-logo-red-white-claim.svg`](svg/binder-logo-red-white-claim.svg) | Red and white, with claim |

### PNG

| File | Variant |
|---|---|
| [`binder-logo.png`](png/binder-logo.png) | Red and black, without claim |
| [`binder-logo-claim.png`](png/binder-logo-claim.png) | Red and black, with claim |
| [`binder-logo-black.png`](png/binder-logo-black.png) | Solid black, without claim |
| [`binder-logo-white.png`](png/binder-logo-white.png) | Solid white, without claim |
| [`binder-logo-white-claim.png`](png/binder-logo-white-claim.png) | Solid white, with claim |
| [`binder-icon.png`](png/binder-icon.png) | Bildmarke only — favicons and similar |

### PDF

| File | Variant |
|---|---|
| [`binder-logo.pdf`](pdf/binder-logo.pdf) | Red and black, without claim |
| [`binder-logo-claim.pdf`](pdf/binder-logo-claim.pdf) | Red and black, with claim |

## The three rules people get wrong

1. **The word mark never appears without the Bildmarke** (the red triangles).
2. **Below 30 mm width, use a version without the claim** — it stops being legible.
3. **Clear space is 1.5 × the height of the Bildmarke** on all sides.

Everything else: [../logo.md](../logo.md).

## Not here

EPS files, the Bildmarke as vector, envelope artwork, and the sub-brand logos
(Customized Solutions, ReFurbished, Quality Management, India, Defence).
Request them from [marketing@binder-world.com](mailto:marketing@binder-world.com).

## Two things to know about these files

### The colour values differ from the corporate design

The files carry three different reds and three different blacks between them,
and none of them is the CD value. Same logo, different file, different colour:

| File | Red | Black |
|---|---|---|
| `binder-logo.svg` | `#ed1c24` | `#231f20` |
| `binder-logo-red-white*.svg` | `#ed1c24` | — |
| `binder-logo-black*.svg` | — | `#231f20` |
| `binder-logo.png`, `binder-logo-claim.png`, `binder-icon.png` | `#e30613` | `#1d1d1b` |
| `binder-logo-black.png` | — | `#000000` ✓ |
| `binder-logo-white*` | — | `#ffffff` ✓ |

The corporate design specifies **`#e60000`** and **`#000000`**. `#e30613` is
the RGB rendering of HKS 14; `#ed1c24` matches a US Web Coated conversion of
CMYK 0/100/100/0. Both look like colour-profile artefacts from different export
workflows rather than deliberate choices.

**For screen work, set the colours from [../colors.md](../colors.md)** instead
of relying on what is inside the files. Otherwise the logo carries a different
red than every other element on the same page.

This is with the marketing department.

### The SVGs are cropped to the artwork

As supplied, every SVG sat on an oversized artboard — between 49 % and 96 %
empty space, with `binder-logo-white.svg` on a full A4 canvas. Embedded that
way, the logo renders small and off-centre inside a large invisible margin.

The `viewBox` of each file has been set to the actual bounding box of the
artwork. **The path data is byte-for-byte unchanged** — only the crop differs.
Clear space is applied in layout, not baked into the asset.
