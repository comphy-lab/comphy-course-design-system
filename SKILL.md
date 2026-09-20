# CoMPhy Lab Course Design System — SKILL.md

Use this when producing course landing pages, lessons, or mkdocs course material for the CoMPhy Lab.

## Start every file

1. Load the self-hosted webfont pack:

```html
<link rel="stylesheet" href="fonts/fonts.css">
```

Copy or symlink the whole `fonts/` directory (css + woff2 + `OFL.txt`). Do **not** load Google Fonts, Bunny, or other third-party font CDNs.

2. Link `tokens.css`. Do not redefine tokens locally — reference the CSS variables.

3. When present, link `courses.css` after tokens for course-only patterns. Do not fork tokens into the course sheet.

4. On `<html>` add `data-theme="light"` (default) or `data-theme="dark"`. The token file handles the rest.

## The non-negotiables

- **Paper, not white.** `background: var(--c-paper)` on body. Never `#fff`.
- **Teal is the only interactive accent.** Buttons, focus rings, hover states all resolve to `--c-accent-teal`. Do not introduce new hues.
- **Hero gradient is for the hero only.** The four-stop gradient clips into Cormorant Garamond on the lab / course title and nowhere else.
- **Four font roles:** Cormorant Garamond = hero / display. Fraunces = headings. IBM Plex Sans = body / UI. IBM Plex Mono = code / DOI / email. Do not rename these families or fall back to system-ui for body.
- **Panel radius stays at 28 px** (`--r-lg`). Do not shrink it to fit more content.
- **Eyebrows are always purple + uppercase + tracked.** Use `<span class="eyebrow">…</span>`.

## Course templates

Landing and lesson templates must stay structurally parallel and share `ds-base.js` / `support.js` when those files are present. Prefer patterns already in `courses.css` over one-off mkdocs overrides.
