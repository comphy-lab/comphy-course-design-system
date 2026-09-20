# comphy-course-design-system

Course-facing layer of the CoMPhy Lab design system: landing and lesson templates, course CSS, bundled fonts, and the mkdocs override.

Mirror of the Claude Design project **CoMPhy Lab Course Design System** (`841ad5ee-807b-4db4-b8dc-aefcc4470e1c`). Claude Design is upstream for authored design work; this repository is the durable, reviewable record.

## Layout

| Path | Role |
|---|---|
| `tokens.css` | Shared design tokens. Load first after fonts. |
| `fonts/` | Self-hosted webfont pack (`fonts.css`, `*.woff2`, `OFL.txt`). |
| `fonts/fonts.css` | `@font-face` sheet (latin + latin-ext, `font-display: swap`). |
| `courses.css` | Course-specific layer on top of the tokens. |
| `Course System.html` | Living guide for the course layer. |
| `templates/course-landing/`, `templates/course-lesson/` | Design-component templates plus their `ds-base.js` and `support.js`. |
| `mkdocs/course-extra.css` | Override sheet for mkdocs-published course material. |
| `_ds_manifest.json`, `_ds_bundle.js`, `_adherence.oxlintrc.json` | Claude Design build products. Generated — re-import, do not hand-edit. |

## Install (fonts + tokens)

```html
<link rel="stylesheet" href="fonts/fonts.css">
<link rel="stylesheet" href="tokens.css">
```

Do **not** load `fonts.googleapis.com`, `fonts.gstatic.com`, Bunny, or other font CDNs. Copy or symlink the whole `fonts/` directory.

Families (do not rename; do not switch body to system-ui): Cormorant Garamond, Fraunces, IBM Plex Sans, IBM Plex Mono.

## Rules

- Fonts are **self-hosted here**. Pack SoT is `comphy-lab/comphy-design-system` `fonts/` (club fuller pack). If you change a font file, update `fonts/fonts.css` in the same commit.
- Never redefine a core token. `courses.css` extends `tokens.css`; it does not fork it.
- The mkdocs sheet is an override, not a second design system. Anything reusable belongs in `courses.css`.
- Keep landing and lesson templates structurally parallel — they share `ds-base.js` and `support.js` by design.

See `IMPORT-STATUS.md` for exactly which files came from the live project and which are still outstanding.
