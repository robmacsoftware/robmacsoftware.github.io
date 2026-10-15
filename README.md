# RobMac Software

Local foundation for the bilingual RobMac Software website. English is served
at `/` and Spanish at `/es/`. Both pages use shared CSS and original SVG assets.
Engineering Toolkit is presented as **In Development** / **En desarrollo**.

## Structure

```text
index.html               English home page
es/index.html            Spanish home page
assets/css/styles.css    Shared responsive styles and automatic theme
assets/images/           Original official SVG artwork (unchanged)
.gitignore               Local-only files and credential exclusions
README.md                Local development and scope notes
```

## Local preview

From this directory, double-click `RobMac_Local_Preview.bat`.
It uses installed Python 3.12 (the `py -3.12` launcher or `python`), binds only
to `127.0.0.1:8003`, and opens the English page in the default browser.
PHP, Node.js and dependency installation are not required.

- English: <http://127.0.0.1:8003/>
- Spanish: <http://127.0.0.1:8003/es/>
- Stop the server with **Ctrl+C** in its terminal.

Alternatively, from this directory with Python 3.12:

```powershell
python -B RobMac_Local_Preview.py
```

Run one preview server at a time. The helper copies only the seven explicit
`PUBLIC_FILES` into a fresh `.local-preview/site-*` directory and serves that
isolated copy. It never serves the repository directory. Git metadata, local
launchers, README, unused SVG variants, credentials and unapproved pages are not
copied. Missing pages and directories without an approved index return HTTP 404.

The launcher, Python helper and `.local-preview/` are ignored by Git and remain
local-only. Normal Ctrl+C shutdown removes that run's temporary copy; closing or
forcibly terminating the process may leave an ignored copy. Existing project
files and previous snapshots are never overwritten or deleted by the helper.

After editing public files, stop and restart the launcher to refresh the copy.
When adding an approved page or asset, explicitly add its relative file path to
`PUBLIC_FILES` in `RobMac_Local_Preview.py`; do not replace the allowlist with
recursive directory copying. The `--no-browser` option supports validation.

## Implementation

- Semantic HTML5, CSS3 and system fonts; no JavaScript or frameworks.
- CSS `prefers-color-scheme` selects light or dark colors. A `picture` element
  selects `RobMac_Logo_Claro.svg` on light backgrounds and
  `RobMac_Logo_Oscuro.svg` on dark backgrounds. The color monogram retains a pale
  backdrop in both themes; `RobMac_App_Black.svg` is the favicon.
- Keyboard skip link, visible focus indicators, labeled navigation, current
  language indicators, responsive layouts and equivalent English/Spanish copy.
- Mobile and desktop language selectors occupy their natural reading positions;
  CSS hides the inactive selector from layout, accessibility and keyboard focus.
- Relative assets and alternate-language links work under the local preview.
- Titles, descriptions, language attributes and viewport metadata are included.
- All rendering assets are local. The email and official GitHub links are ordinary
  visitor-initiated links. No trackers, third-party fonts, forms or remote scripts.

## Scope and future work

This phase is local implementation only. It does not enable hosting, configure
GitHub Pages, publish files or modify repository/organization settings.
No Engineering Toolkit source files are part of this work.

The following privacy routes are reserved and deliberately **not implemented**:

```text
/engineering-toolkit/privacy/
/engineering-toolkit/privacy/es/
```

Privacy content requires separate technical approval. There are no placeholder
policies or public links to those routes. No download links, release dates,
screenshots, testimonials or store availability are asserted.

Both pages include self-referencing English, Spanish and `x-default` alternate
links using `https://robmacsoftware.github.io/` and
`https://robmacsoftware.github.io/es/`. Visible navigation and assets remain
relative. Canonical URLs and deployment configuration remain future work.
Do not publish or commit this phase without explicit approval.

## Local validation performed

- Both language pages and all referenced assets returned HTTP 200.
- Basic HTML nesting, unique IDs, one H1 per page, image alternatives, metadata,
  local asset paths and fragment/language destinations passed automated checks.
- Both languages rendered without horizontal overflow at 320, 375, 640, 641,
  768, 900 and 1280 CSS pixels. Original SVG images loaded at each size.
- The browser's automatic dark theme selected the dark-background logo. Light
  rendering was checked by temporarily inverting the theme media query in the
  isolated preview copy only; original source was preserved and the copy restored.
- Normal text and button color pairs exceeded 4.5:1 contrast in both themes
  (minimum checked ratios: light 5.73:1, dark 7.82:1).
- Keyboard focus, skip-to-main, product/contact anchors, back-to-top and language
  switching in both directions passed browser checks. No console warnings or
  errors appeared during those checks.
- Actual Tab-key navigation matched visual order in both languages at mobile and
  desktop widths; only one language selector was exposed at each breakpoint.
- The isolated copy contained exactly the seven approved public files. Git
  metadata, `.gitignore`, launchers, README, reserved privacy routes, directory
  listings and unknown routes returned HTTP 404. The listener bound only to
  `127.0.0.1:8003`.
- The Windows launcher opened the default browser, and Ctrl+C stopped the server
  and removed its run's copy. Original SVG hashes were unchanged. No dependencies
  were installed; no commits or publishing were performed.

These are local checks, not formal accessibility certification or exhaustive
cross-browser/screen-reader testing. Production route handling remains untested.
