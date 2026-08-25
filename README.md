# About

Personal site for **Sandeep Bazar** — <https://sandeepbazar.github.io/About/>

A single hand-written `index.html`: no framework, no build step, no tracker. The only
external request is the IBM Plex webfont from Google Fonts. GitHub Actions publishes the
repository root to Pages on every push to `main`.

## Layout

| Path | What it is |
|------|------------|
| `index.html` | The whole site — markup, styles and the career chart script |
| `assets/profile.jpg` | Hero headshot (800×800). Replace this file to change the photo. |
| `assets/running.jpg` | Photo for the endurance section |
| `.github/workflows/pages.yml` | Static deploy to GitHub Pages |

## Editing

**Career chart.** The plot and the mobile milestone list are both generated from two arrays
near the bottom of `index.html`: `STEPS` (role changes, as `{year, level, label}`) and
`MARKS` (milestones). Edit those and both views stay in sync — there is no hand-drawn SVG
path to maintain.

**Resume.** Do not put one here. Every variant `build_resumes.py` produces carries a phone
number, an email address and a full postal location in its header, and anything in this
repository is publicly downloadable. Resumes stay in the jobs project under `Apply/`, which is
not a git repository. Recruiters are pointed at LinkedIn instead.

## Checks worth repeating after an edit

- No horizontal scroll at 375 px wide.
- Readable in both light and dark colour schemes.
- `prefers-reduced-motion` disables the chart draw-on and scroll reveals.
- Keyboard focus is visible, and every chart milestone is reachable by Tab.
