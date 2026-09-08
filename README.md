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
| [**typography.md**](typography.md) | FF Meta Pro, the substitutes, type rules and the hierarchy with concrete sizes. |
| [**logo.md**](logo.md) | Clear space, positioning, minimum sizes, what is and is not permitted. |
| [**design-principles.md**](design-principles.md) | The black/white/red triad, formal language, and the red line above titles. |
| [**tokens/**](tokens/) | The palette as [JSON](tokens/colors.json), [CSS custom properties](tokens/colors.css) and [Sass variables](tokens/colors.scss). |

## Quick start for developers

```html
<link rel="stylesheet" href="tokens/colors.css">
```

```css
.headline { color: var(--binder-anthracite); }     /* or --binder-gray-800 */
.accent   { color: var(--binder-binder-red); }
.card     { background: var(--binder-porcelain); } /* or --binder-gray-100 */
.border   { border-color: var(--binder-silver); }  /* or --binder-gray-300 */
```

Every gray has both a **name** (`--binder-slate`) and a **number**
(`--binder-gray-600`) — they point at the same value. Names are for talking to
people, numbers are for reading a scale.

The nine grays are **Porcelain 100 · Pearl 200 · Silver 300 · Ash 400 ·
Concrete 500 · Slate 600 · Basalt 700 · Anthracite 800 · Graphite 900**. White
and black carry no number: they sit outside the ramp, as `$white` and `$black`
do in Bootstrap.

## Two things that trip people up

**Hex is for screen, CMYK is for print — do not convert between them.** The
grays carry a slight blue cast on screen but print as pure K. That is
deliberate: converted exactly, the cast comes to under 6 % cyan, and cyan that
low cannot be reproduced reliably in offset printing.

**Fonts are not in this repository.** FF Meta Pro is a licensed typeface and
every weight has to be bought. See [typography.md](typography.md) for sources
and for the substitutes to use where a licence is not available.

## Not here yet

- Logo files (SVG, PNG, EPS) — request from the marketing department
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

Derived from the BINDER Corporate Design Manual (01/2026) and the corporate
colour palette. Where this repository and older documents disagree, the values
here are the current ones — see the change notes in [colors.md](colors.md).
