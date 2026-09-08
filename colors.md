# Colours

The BINDER appearance rests on a triad of **black, white and BINDER Red**. This triad is
the core of the corporate design and a primary design element in its own right.
Everything else supports it and must never dilute its contrast.

Machine-readable versions live in [tokens/](tokens/): [`colors.json`](tokens/colors.json),
[`colors.css`](tokens/colors.css) and [`colors.scss`](tokens/colors.scss).

**Hex values apply to screen, CMYK values apply to print.** The grays carry a slight blue
cast on screen but print as pure K with no CMY component: converted exactly, the cast
comes to under 6 % cyan, and cyan that low cannot be reproduced reliably in offset
printing. Use hex on screen and CMYK on paper.

## Primary colours

![Primary colours](assets/primary.svg)

| Colour | Scale | Hex | CMYK | Print references | Use |
|---|---|---|---|---|---|
| **White** | - | `#ffffff` | 0/0/0/0 | RAL 9003 Signal White | Structure, backgrounds, white space, negative applications |
| **Porcelain** | 100 | `#f4f4f5` | 0/0/0/10 | — | Sections, cards, subtle backgrounds |
| **Silver** | 300 | `#d8d8dd` | 0/0/0/25 | — | Borders, secondary elements |
| **Concrete** | 500 | `#9a9aa1` | 0/0/0/45 | — | Muted text, dividers, secondary UI elements |
| **Anthracite** | 800 | `#404043` | 0/0/0/75 | — | Text and important UI elements — the dark tone that is not black |
| **Black** | - | `#000000` | 0/0/0/100 | HKS 88, Pantone 426, RAL 9005 Jet Black | Primary text colour, base for graphics and icons — avoid large full-coverage areas |
| **BINDER Red** | - | `#e60000` | 0/100/100/0 | HKS 14, Pantone 485, RAL 3020 Traffic Red | Highlight colour, graphic elements, icons, emphasis |
| **Red Dark** | - | `#990000` | 24/100/100/27 | HKS 16, RAL 3003 Ruby Red | Accent alongside BINDER Red, contrast, mouseover state of red buttons |

## The gray scale

![Gray scale](assets/scale-gray.svg)

Each gray has a **name** for talking to people and a **number** for code - they point at
the same value. The scale runs 100 (lightest) to 900 (darkest), the same direction as
CSS `font-weight`.

White and black carry no number. They sit outside the ramp, exactly as `$white` and
`$black` do in Bootstrap and Tailwind: a `0` would read as `#000`, which is black.

| Name | Scale | Hex | CMYK |
|---|---|---|---|
| White | - | `#ffffff` | 0/0/0/0 |
| Porcelain | 100 | `#f4f4f5` | 0/0/0/10 |
| Pearl | 200 | `#e6e6e9` | 0/0/0/15 |
| Silver | 300 | `#d8d8dd` | 0/0/0/25 |
| Ash | 400 | `#b8b8c0` | 0/0/0/30 |
| Concrete | 500 | `#9a9aa1` | 0/0/0/45 |
| Slate | 600 | `#7a7a82` | 0/0/0/50 |
| Basalt | 700 | `#5a5a5f` | 0/0/0/65 |
| Anthracite | 800 | `#404043` | 0/0/0/75 |
| Graphite | 900 | `#252527` | 0/0/0/85 |
| Black | - | `#000000` | 0/0/0/100 |

The ramp is denser at the light end on purpose: pale surface tones get used over
large areas, where small differences matter. The dark half steps more widely, because
the eye separates dark tones less well anyway.

## The red scale

![Red scale](assets/scale-red.svg)

| Name | Scale | Hex | CMYK |
|---|---|---|---|
| Blush | 100 | `#ffcccc` | 0/20/20/0 |
| Salmon | 200 | `#ff9999` | 0/40/40/0 |
| Coral | 300 | `#e95e40` | 0/75/75/0 |
| BINDER Red | - | `#e60000` | 0/100/100/0 |
| Red Dark | - | `#990000` | 24/100/100/27 |

BINDER Red and Red Dark carry no number - they are brand colours, not ramp steps.

**Red Dark** is the accent alongside BINDER Red: a calm, high-grade colour for
restrained emphasis in graphics and icons, and the mouseover state of a red button.

## BINDER Green

`#97bf29` - CMYK 75/0/100/0

For **sustainability and eco topics** (BINDER goes green). Not a general-purpose
accent - using it elsewhere weakens the black/white/red triad.

## Chart colours

![Chart colours](assets/chart.svg)

| Key | Hex | CMYK |
|---|---|---|
| A | `#fde800` | 5/0/100/0 |
| B | `#fabb00` | 0/30/100/0 |
| C | `#e95d0f` | 0/75/100/0 |
| D | `#e60000` | 0/100/100/0 |
| E | `#c3077f` | 22/97/0/0 |
| F | `#622181` | 75/100/0/0 |
| G | `#38378b` | 90/90/0/0 |
| H | `#006fb4` | 90/50/0/0 |
| I | `#0099bf` | 80/20/15/0 |
| J | `#26965e` | 80/15/75/0 |
| K | `#97bf29` | 50/0/95/0 |
| L | `#bdcd00` | 35/0/100/0 |

### Which colours for how many values

Do not pick freely - take the prescribed sequence for the number of values in your
chart. This keeps charts recognisable across all BINDER media.

| Values | Sequence |
|---|---|
| 1 | A |
| 2 | A - D |
| 3 | A - D - H |
| 4 | A - D - H - K |
| 5 | A - D - G - J - L |
| 6 | A - C - E - G - I - K |
| 7 | A - C - E - G - I - J - L |
| 8 | A - B - D - F - H - I - K - L |
| 9 | A - B - D - E - G - H - I - K - L |
| 10 | A - B - D - E - G - H - I - J - K - L |
| 11 | A - B - C - D - E - G - H - I - J - K - L |

Text inside charts follows the same rule as everywhere else: never below 6 pt.
See [typography.md](typography.md).
