# Import status

Imported from Claude Design project `841ad5ee-807b-4db4-b8dc-aefcc4470e1c` ("CoMPhy Lab Course Design System") on **2026-08-09**.

**This import is the least complete of the three.** Only the shared design-system base is present; the entire course layer is still outstanding.

## Provenance

- **april-export** — copied byte-for-byte from the 2026-04-24 export at `comphy-lab.github.io/comphy-lab-design-system/project/` (verified byte-identical to the live project on `tokens.css` and `README.md` in the core design-system project).

| File | Source |
|---|---|
| `tokens.css` | april-export (verified identical to live) |
| `CoMPhy Design System.html` | april-export (Google Fonts CDN removed; loads `fonts/fonts.css`) |
| `CoMPhy Website v2.html` | april-export (same) |
| `Red Team Audit.html` | april-export (same) |
| `CoMPhy Design System (standalone).html` | april-export |
| `assets/images/**`, `assets/logos/**`, `uploads/**` | april-export |
| `README.md`, `SKILL.md`, `AGENTS.md` | authored in-repo for self-host install path |

## Webfont pack (added in-repo)

| Path | Source |
|---|---|
| `fonts/fonts.css` + `fonts/*.woff2` (14 faces) + `fonts/OFL.txt` | `comphy-lab/comphy-design-system` branch `rayleigh-cloud/self-host-webfont-sot-eeb6` `fonts/` (club fuller pack; urls already `url(./…)`) |

Demos and docs load `fonts/fonts.css` locally. Google Fonts CDN is no longer the documented install path.

## Outstanding

The course layer — the reason this repo exists — has not been imported yet.

| File | Why | Fix |
|---|---|---|
| `Course System.html` | Not yet pulled | DesignSync `get_file` |
| `courses.css` | Not yet pulled | DesignSync `get_file` |
| `mkdocs/course-extra.css` | Not yet pulled | DesignSync `get_file` |
| `templates/course-landing/{CourseLanding.dc.html,ds-base.js,support.js}` | Not yet pulled | DesignSync `get_file` |
| `templates/course-lesson/{CourseLesson.dc.html,ds-base.js,support.js}` | Not yet pulled | DesignSync `get_file` |
| `_ds_manifest.json`, `_ds_bundle.js`, `_adherence.oxlintrc.json` | Not yet pulled | DesignSync `get_file` / self-check |
| `CoMPhy Design System (standalone).html` | Generated build still embeds prior Google Fonts preconnect / install snippet | Re-generate from the living guide after DesignSync; do not hand-edit the 5 MiB bundle beyond clearing CDN strings |
| `uploads/blog_ref-17836725*.png` (3 files) | Binary; not present in the April export | DesignSync `get_file` (base64) |
