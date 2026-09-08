# BINDER Corporate Design

The visual identity of BINDER GmbH: colours, typography, logo rules and the
design principles behind them. This repository is the reference for anyone
producing material in the BINDER design — **agencies, service providers,
partners, suppliers and integrators**.

**→ [Browse the visual reference](https://binder-gmbh.github.io/binder-corporate-design/)**
— colours you can actually see and click to copy.

## What is here

| | |
|---|---|
| [**colors.md**](colors.md) | Full palette: primaries, gray scale, red scale, chart colours. Hex, CMYK, HKS, Pantone, RAL. |
| [**typography.md**](typography.md) | Source Sans 3, the substitutes, type rules and the hierarchy with concrete sizes. |
| [**logo.md**](logo.md) | Clear space, positioning, minimum sizes, what is and is not permitted. |
| [**logo/**](logo/) | The logo files themselves — SVG, PNG and PDF in all approved variants. |
| [**design-principles.md**](design-principles.md) | The black/white/red triad, formal language, and the red line above titles. |
| [**tokens/**](tokens/) | The palette as [JSON](tokens/colors.json), [CSS custom properties](tokens/colors.css) and [Sass variables](tokens/colors.scss). |

## Quick start for developers

```html
<link rel="stylesheet" href="tokens/colors.css">
```

```css
.headline { color: var(--binder-black); }
.accent   { color: var(--binder-red); }
.card     { background: var(--binder-gray-10); }   /* #f0f0f0 */
.border   { border-color: var(--binder-gray-25); } /* #cdcdcd */
```

The gray shades are named by their print K value, so screen and print use the
same reference: `--binder-gray-10`, `-25`, `-45`, `-65`.

## Two things that trip people up

**Hex is for screen, CMYK is for print.**

**The corporate typeface is free.** Source Sans 3 is open source — get it from
Google Fonts, Adobe Fonts or GitHub, no licence to buy. It replaced FF Meta
Pro, which was licensed per weight. See [typography.md](typography.md).

**The logo files carry different colour values than the corporate design.**
They contain `#ed1c24` and `#231f20`; the CD specifies `#e60000` and `#000000`.
For screen work, take the colours from [colors.md](colors.md).

## Not here yet

- EPS files, the Bildmarke as vector, and the sub-brand logos (Customized
  Solutions, ReFurbished, Quality Management, India, Defence)
- Document, presentation and print templates
- Image guidelines and picture material

## Usage and rights

The BINDER name, logo and word/figurative marks are protected trademarks of
BINDER GmbH. Publishing these guidelines makes them accessible for legitimate
use — press, partners, suppliers and integrators representing BINDER products.
**It does not transfer any rights in the marks themselves.** Modifying the
logo, recolouring it, or using it in a way that suggests an endorsement or
partnership that does not exist is not permitted.

Questions about a specific case: open an issue, or contact
[marketing@binder-world.com](mailto:marketing@binder-world.com).

## Changing a colour

`tokens/colors.json` is the single source of truth. Edit it, then regenerate
everything derived from it:

```bash
python3 tools/build.py
```

That rewrites the CSS, the Sass variables, the swatches, `colors.md` and the
published page in one go. Do not hand-edit the generated files.

## Source

The BINDER Corporate Design Manual, section Company colors / Unternehmensfarben
and The font world / Schriftwelt. This repository restates those specifications
in a form that is easier to work from; it does not extend or reinterpret them.

For anything not covered here, or if something looks wrong, contact
[marketing@binder-world.com](mailto:marketing@binder-world.com).
