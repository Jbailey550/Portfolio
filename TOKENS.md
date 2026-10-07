# Original site with design tokens

This local branch starts from the original site's main branch. Its HTML, images, layout and legacy theme remain unchanged. Nothing is deployed by editing these files.

`tokens.css` contains the verified Figma palette, spacing scale and font foundations. It is a snapshot, not an automatic Figma sync. `style.css` imports it but keeps its original values so the site initially looks the same.

## Apply tokens gradually

In `style.css`, replace a value in the existing `:root` block when you want to try it:

```css
--bg: var(--indigo-default);
--accent: var(--pink-default);
--text: var(--neutral-white);
```

You can also use tokens directly in a component, for example `padding: var(--scale-600)` (24px). The stylesheet loads Outfit (weights 100–900). The legacy `--serif`, `--sans`, and `--mono` roles all alias `--font-text`, so headings, body text, navigation and labels use Outfit. Form controls use the same token.

Figma mapping: `Colour base / Blue/Default` → `--blue-default`; `Scale / 600` → `--scale-600`.

Open `http://127.0.0.1:8768/` while the local preview server is running, then save and refresh to see edits. The working branch is `original-site-tokens`. Do not merge or deploy until explicitly approved.

## Responsive typography

Outfit is used throughout. H1–H6 use weight 600; lead and body use weight 400.
Sizes and line heights below are in pixels at the default 16px root size; CSS tokens use rem. Mobile applies at 640px and below.

| Role | Desktop size / line | Mobile size / line |
|---|---|---|
| H1 | 60 / 72 | 48 / 56 |
| H2 | 48 / 56 | 40 / 48 |
| H3 | 40 / 48 | 32 / 40 |
| H4 | 32 / 40 | 28 / 32 |
| H5 | 24 / 28 | 24 / 28 |
| H6 | 20 / 24 | 20 / 24 |
| Lead | 20 / 28 | 20 / 28 |
| Body | 16 / 24 | 16 / 24 |

Edit `--type-h1-size`, `--type-h1-line`, and `--type-h1-weight` (and equivalent roles) in tokens.css.
Card headings retain semantic H3 markup and use H5 visual tokens. Lead roles cover page introductions and About me copy. Navigation, tags and captions keep their component sizing.

Homepage H1 override: `--type-hero-size` scales fluidly from 32px at 384px viewport width to 54px at 1440px, capped at those sizes (at the default 16px root). `--type-hero-line` is a proportional 1.185185, giving approximately 38px–64px line height. Weight stays 600; the shared H1–H6 scale is unchanged.
