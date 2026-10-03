# Portfolio DS — Design system and instructions

Source: [Portfolio DS in Figma](https://www.figma.com/design/tXUsH8AsEgUEjARXFpb7dU/Portfolio-DS)

Prepared: 2 October 2026.

> Snapshot, not a live export: Figma’s Starter-plan tool limit prevented a fresh read when this document was created. The values below combine the verified variable creation records and the latest successful reads in this task. Later edits in Figma may not be reflected. Colour hex values are rounded to 8-bit sRGB; Figma can retain more precise channel values.

## My instructions — edit this section

Use this section to record your decisions. Replace the bracketed prompts with your instructions. Unfilled prompts are not requirements.

- **Brand personality:** [Describe the tone and feel.]
- **Primary colour and where to use it:** [Choose a token and its purpose.]
- **Page backgrounds:** [Choose preferred light and dark surface tokens.]
- **Headings:** [Define font, colour, casing, and hierarchy.]
- **Body text:** [Define font, colour, and readability preferences.]
- **Buttons and links:** [Define colour, shape, hover, focus, and disabled states.]
- **Layout and spacing:** [Define content width, margins, gaps, and section spacing.]
- **Photography and graphics:** [Define image treatment and when to use illustration.]
- **Responsive behaviour:** [Define stacking, navigation, and actual website breakpoints.]
- **Accessibility:** [Record requirements and testing expectations.]
- **Avoid:** [List unwanted patterns or styles.]
- **Exceptions:** [Record approved exceptions and why they exist.]

## Proposed working rules

These are editable recommendations, not rules previously authored by John.

1. Reuse the tokens documented below. Prefer an existing semantic token when it fits the intended role.
2. In Figma, bind colours, text properties, and spacing to actual variables; matching a raw value alone does not create a binding.
3. In code, define named tokens centrally and reference them from reusable components. Keep an explicit mapping to the Figma collection and variable name.
4. Preserve existing variable names and IDs when possible. Do not rename or delete them merely to match a coding preference.
5. Use the Desktop or Mobile typography group for the intended layout. Device-size values are reference widths, not automatic breakpoints.
6. Check contrast for the actual text/background pair and test keyboard focus, wrapping, and narrow layouts. A named status or brand token does not guarantee sufficient contrast.
7. Document new tokens and component decisions here. Resolve conflicts between this guide, Figma, and code before overwriting an existing decision.
8. Treat prototype edits as proposals until explicitly applied to Figma or production code.

## What exists

| Collection | Contents |
|---|---|
| Colour base | 59 palette colour variables |
| Colour semantics | 8 aliases for status base colours and tints |
| Font | Heading and Text font-family strings |
| Font weight | Semi Bold and Regular strings |
| Scale | 16 numeric foundations |
| Text | 10 semantic text-colour aliases |
| Responsive | 62 Desktop/Mobile variables plus the existing `Fon` placeholder |
| Collection | Existing `Color 2` placeholder |

All observed collections have one mode. Desktop and Mobile are groups inside Responsive, not separate modes. No local reusable components or text styles were found in the last inspection. Components remain to be designed; this document does not imply a completed component library.

## Colour base

The complete token reference is `Colour base` + the variable name below. These colours were made available in fill, text, stroke, and effect colour pickers.


### Pink

| Variable | Hex |
|---|---|
| `Pink/50` | `#FFF5F9` |
| `Pink/100` | `#FFE7F2` |
| `Pink/200` | `#FECCE2` |
| `Pink/300` | `#FEA8CE` |
| `Pink/400` | `#FD85BA` |
| `Pink/500` | `#FD5FA5` |
| `Pink/Default` | `#FC3A90` |
| `Pink/700` | `#CA2E73` |
| `Pink/800` | `#972356` |
| `Pink/900` | `#65173A` |

### Neutral

| Variable | Hex |
|---|---|
| `Neutral/Black` | `#000000` |
| `Neutral/800` | `#1C1C1C` |
| `Neutral/700` | `#393939` |
| `Neutral/Default` | `#555555` |
| `Neutral/500` | `#717171` |
| `Neutral/400` | `#8E8E8E` |
| `Neutral/300` | `#AAAAAA` |
| `Neutral/200` | `#C6C6C6` |
| `Neutral/100` | `#E3E3E3` |
| `Neutral/White` | `#FFFFFF` |

### Indigo

| Variable | Hex |
|---|---|
| `Indigo/50` | `#F3F3F6` |
| `Indigo/100` | `#E2E1E9` |
| `Indigo/200` | `#C0BECF` |
| `Indigo/300` | `#9491AE` |
| `Indigo/400` | `#68658D` |
| `Indigo/500` | `#39356A` |
| `Indigo/Default` | `#0B0647` |
| `Indigo/700` | `#090539` |
| `Indigo/800` | `#07042B` |
| `Indigo/900` | `#04021C` |

### Purple

| Variable | Hex |
|---|---|
| `Purple/50` | `#F4F3FC` |
| `Purple/100` | `#E5E2F7` |
| `Purple/200` | `#C7BFEF` |
| `Purple/300` | `#A193E3` |
| `Purple/400` | `#7A67D8` |
| `Purple/500` | `#5139CC` |
| `Purple/Default` | `#280AC0` |
| `Purple/700` | `#20089A` |
| `Purple/800` | `#180673` |
| `Purple/900` | `#10044D` |

### Blue

| Variable | Hex |
|---|---|
| `Blue/50` | `#F2F9FF` |
| `Blue/100` | `#E0F1FF` |
| `Blue/200` | `#BDE1FF` |
| `Blue/300` | `#8FCCFF` |
| `Blue/400` | `#61B8FF` |
| `Blue/500` | `#30A2FF` |
| `Blue/Default` | `#008CFF` |
| `Blue/700` | `#0070CC` |
| `Blue/800` | `#005499` |
| `Blue/900` | `#003866` |

### Yellow

| Variable | Hex |
|---|---|
| `Yellow/600` | `#FFC300` |

### Status

| Variable | Hex |
|---|---|
| `Status/Success/Base` | `#15803D` |
| `Status/Success/Tint` | `#F0FDF4` |
| `Status/Warning/Base` | `#B45309` |
| `Status/Warning/Tint` | `#FFFBEB` |
| `Status/Error/Base` | `#DC2626` |
| `Status/Error/Tint` | `#FEF2F2` |
| `Status/Information/Base` | `#0369A1` |
| `Status/Information/Tint` | `#F0F9FF` |

### Palette observations

- The canvas section named Midnight uses variables named `Indigo/...`.
- Pink, Indigo, Purple, and Blue use `Default` for the former 600 shade. Neutral uses `Black`, `Default`, and `White` for the former 900, 600, and 50 shades.
- Only `Yellow/600` is defined. The other swatches in the Impact Yellow row were repeated Blue swatches; no additional yellow shades were invented.
- Some WEB code-syntax metadata may still contain the original numeric names after Figma renames. Verify it before generating a production token mapping.

## Colour semantics

These variables alias Colour base; they do not hold independent raw colours.

| Variable in Colour semantics | Alias in Colour base | Intended use |
|---|---|---|
| `Status/Success/Base` | `Status/Success/Base` | Text, icons, and borders |
| `Status/Success/Tint` | `Status/Success/Tint` | Backgrounds and subtle surfaces |
| `Status/Warning/Base` | `Status/Warning/Base` | Text, icons, and borders |
| `Status/Warning/Tint` | `Status/Warning/Tint` | Backgrounds and subtle surfaces |
| `Status/Error/Base` | `Status/Error/Base` | Text, icons, and borders |
| `Status/Error/Tint` | `Status/Error/Tint` | Backgrounds and subtle surfaces |
| `Status/Information/Base` | `Status/Information/Base` | Text, icons, and borders |
| `Status/Information/Tint` | `Status/Information/Tint` | Backgrounds and subtle surfaces |

## Text colours

| Variable in Text | Alias in Colour base |
|---|---|
| `Heading-Black` | `Neutral/Black` |
| `Heading-White` | `Neutral/White` |
| `Heading-Pink` | `Pink/Default` |
| `Heading-Midnight` | `Indigo/Default` |
| `Heading-Purple` | `Purple/Default` |
| `Heading-Blue` | `Blue/Default` |
| `Body-Dark` | `Neutral/Black` |
| `Body-Light` | `Neutral/White` |
| `Link-Light` | `Blue/Default` |
| `Link-LightHover` | `Blue/400` |

## Fonts

| Collection | Variable | Value |
|---|---|---|
| Font | `Heading` | Anton |
| Font | `Text` | Outfit |
| Font weight | `Semi Bold` | Semi Bold |
| Font weight | `Regular` | Regular |

The available Figma fonts were confirmed as Anton Regular and Outfit with Regular, Medium, SemiBold, Bold, and other weights. The Font weight string `Semi Bold` differs from the available Outfit style spelling `SemiBold`. Verify and map the actual font-style name before binding this string. Do not assume every family has every weight.

## Numeric scale

Values are unitless FLOAT variables; use them as pixels when binding dimensional properties. Token names are scale labels, not their pixel values.

| Variable in Scale | Value |
|---|---|
| `0` | 0 |
| `1` | 1 |
| `50` | 2 |
| `100` | 4 |
| `200` | 8 |
| `300` | 12 |
| `400` | 16 |
| `500` | 20 |
| `600` | 24 |
| `700` | 28 |
| `800` | 32 |
| `900` | 36 |
| `1000` | 40 |
| `1100` | 48 |
| `1200` | 52 |
| `1300` | 64 |

## Responsive typography

Within Responsive, paths follow `{Device}/{Role}/{Property}`. Examples:

- `Desktop/H1/Font size`
- `Mobile/H1/Line height`
- `Desktop/Paragraph/Medium/Paragraph spacing`

The properties are `Font size`, `Line height`, and `Paragraph spacing`. All values below are pixels. Font sizes and line heights follow the referenced tutorial; paragraph spacing is an editable starting point adapted from it.

Source: [Build a Design System — Full Course, responsive variables section](https://www.youtube.com/watch?v=opTANvl9G1g&t=3744s).


### Desktop

`Desktop/Device size`: **1440 px**.

| Role | Font size | Line height | Paragraph spacing |
|---|---|---|---|
| `H1` | 60 | 72 | 64 |
| `H2` | 48 | 56 | 48 |
| `H3` | 40 | 48 | 32 |
| `H4` | 32 | 40 | 20 |
| `H5` | 24 | 28 | 20 |
| `H6` | 20 | 24 | 20 |
| `Paragraph/Large` | 20 | 24 | 20 |
| `Paragraph/Medium` | 16 | 20 | 20 |
| `Paragraph/Small` | 14 | 16 | 20 |
| `Paragraph/Extra small` | 12 | 16 | 20 |

### Mobile

`Mobile/Device size`: **440 px**.

| Role | Font size | Line height | Paragraph spacing |
|---|---|---|---|
| `H1` | 48 | 56 | 64 |
| `H2` | 40 | 48 | 48 |
| `H3` | 32 | 40 | 32 |
| `H4` | 28 | 32 | 20 |
| `H5` | 24 | 28 | 20 |
| `H6` | 20 | 24 | 20 |
| `Paragraph/Large` | 20 | 24 | 20 |
| `Paragraph/Medium` | 16 | 20 | 20 |
| `Paragraph/Small` | 14 | 16 | 20 |
| `Paragraph/Extra small` | 12 | 16 | 20 |

### Responsive bindings and limitations

- 54 of the 62 responsive variables alias existing Scale values. The remaining values are stored directly.
- The typography variables are scoped to their matching Figma property picker; Device size is scoped to width/height.
- Paragraph sizes remain the same between Desktop and Mobile. H1–H4 change.
- Selecting `Mobile/H1/Font size` does not automatically select its matching line height or paragraph spacing. Bind each required property.
- Resizing a Figma frame does not automatically swap Desktop variables for Mobile variables.
- For website implementation, define deliberate CSS breakpoints separately. None have been agreed in this system yet.

## Existing placeholders

These were present in the file and were preserved. They are not recommended design tokens until their purpose is clarified.

| Collection | Variable | Last observed value |
|---|---|---|
| Responsive | `Fon` | 0 |
| Collection | `Color 2` | #FFFFFF |

## Homepage exploration — not yet a Figma screen

The conversation preview explored these choices:

| Role | Starting token or value |
|---|---|
| Page background | `Colour base / Indigo/Default` |
| Main accent | `Colour base / Pink/Default` |
| Supporting accents | `Purple/Default`, `Blue/Default` |
| Light surfaces | `Pink/100` |
| Heading family | `Font / Heading` → Anton |
| Body family | `Font / Text` → Outfit |
| Desktop H1 | 60 px |
| Mobile H1 | 48 px |
| Project gap | 32 px |

The preview is an independent mockup, not a live Figma binding. Its body line height was 24 px at a 16 px body size, whereas the documented Responsive medium paragraph line height is 20 px. Some spacing and layout values were additional design choices.

The preview accent was subsequently changed to `#FF2E8C`. That change was **not** applied to Figma. The last verified `Pink/Default` remains `#FC3A90`.

No homepage frames were created in Figma before the tool limit was reached. Graphic placeholders were used in the preview instead of the website photographs.

## Component decisions to add

Record each component once its design is agreed:

| Component | Variants and states | Tokens and behaviour |
|---|---|---|
| Button | [Add] | [Add] |
| Navigation | [Add] | [Add] |
| Project card | [Add] | [Add] |
| Section heading | [Add] | [Add] |
| Footer | [Add] | [Add] |

## Using this guide in a task

Example instruction:

> Read DESIGN-SYSTEM.md before designing or coding. Follow the completed “My instructions” section and use the documented tokens. Reuse existing project components. Identify missing tokens or conflicting values before changing the system. Verify desktop and mobile layouts and distinguish exploratory choices from approved system rules.

This Markdown file is editable documentation; it does not automatically update Figma or the website. Explicitly reference it in a task when you want it followed.

## Change log

| Date | Change | Applied to |
|---|---|---|
| 2026-10-02 | Created this guide from the latest available verified Figma records | Documentation only |
| [Date] | [Describe your decision] | [Documentation / Figma / code / preview] |


## Website implementation — 3 October 2026

- `tokens.css` exports the 59 verified palette colours and 16 Scale values. Names are lowercase with slashes replaced by hyphens: `Colour base / Blue/Default` becomes `--blue-default`. Fonts are `--font-heading` (Anton) and `--font-text` (Outfit).
- `--home-*` variables are website semantic roles and approved layout choices. The pink accent remains the approved `#FF2E8C` preview variation; `--pink-default` retains the Figma value `#FC3A90`.
- `homepage.css` consumes the shared tokens. Other pages import the foundations through `style.css`, keeping their existing legacy theme values until a separate migration.
- Homepage cards are a two-by-two grid with 60% image / 40% heading panels. At 1000px the grid becomes one column; at 650px images stack above their headings. These are website breakpoints, independent of Figma's reference device widths.
- Case-study headings use Outfit 600 at 24px; intro text is 28px. The main heading uses Anton at 60/72px, changing to 48/56px on mobile.
- First card retains 60px vertical panel padding. Descriptions, Read case study labels and the floating cursor badge are removed. Cards remain ordinary links to existing case studies.
- Hover gently zooms images and shifts panel colours. Keyboard focus has a visible outline and colour shift. Reduced-motion preferences disable transitions and zoom. Hover effects are restricted to fine pointers.
- The homepage uses local repository images and includes no mockup toolbar or preview JavaScript. No Figma frame or variable was edited by this website migration.

### Review and publish

Run `python3 -m http.server 8767 --bind 127.0.0.1` from the repository and open `http://127.0.0.1:8767/`. No build step is needed. Review the pull request before merging; verify the repository's GitHub Pages deployment branch in Settings → Pages before publishing. A branch push alone is not approval to merge or change hosting settings.
