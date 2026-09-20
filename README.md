# CoMPhy Lab — Course Design System

Course-facing layer of the CoMPhy Lab design system: landing and lesson templates, course CSS, self-hosted fonts, and the mkdocs override.

## Files

| File | Purpose |
|---|---|
| `tokens.css` | Shared design tokens (colour, type roles, spacing, radius, shadow). |
| `fonts/` | **Self-hosted webfont pack.** Copy/link this directory with `tokens.css`. |
| `fonts/fonts.css` | `@font-face` sheet (latin + latin-ext, `font-display: swap`). |
| `fonts/OFL.txt` | SIL Open Font License texts for the shipped faces. |
| `CoMPhy Design System.html` | Living style guide (shared base demos). |
| `SKILL.md` | Prompt to hand to an agent when working inside this system. |

Course-only files (`courses.css`, `Course System.html`, `templates/`, `mkdocs/`) are still outstanding — see `IMPORT-STATUS.md`.

## Install (consumers)

```html
<link rel="stylesheet" href="fonts/fonts.css">
<link rel="stylesheet" href="tokens.css">
```

Do **not** use `fonts.googleapis.com`, `fonts.gstatic.com`, Bunny, or other font CDNs. Vendor from this repo’s `fonts/` pack (SoT: `comphy-lab/comphy-design-system` `fonts/`, from the `comphy-lab/club` fuller pack).

### Faces shipped

| Family | Role | Weights / styles |
|---|---|---|
| Cormorant Garamond | Hero / display | italic 500, normal 600 |
| Fraunces | Headings | normal 600 |
| IBM Plex Sans | Body / UI | normal 400, 500, 600 |
| IBM Plex Mono | Code | normal 400 |

Do not rename these families or fall back to system-ui for body text.

## Direction

Same visual language as the core design system: warm paper surface, deep teal interactive accent, four type roles, 28-px panel radius. Course pages extend tokens via `courses.css` when that sheet lands — they do not fork tokens.

— Maintained by V. Sanjay · Durham University
