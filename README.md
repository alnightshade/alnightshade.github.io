# alnightshade.github.io

Author website for **A.L. Nightshade**, built as a static site and served with GitHub Pages.

## Layout

- `index.html` — the whole site (single page)
- `style.css` — dark literary theme
- `images/` — cover art (generated; do not edit by hand)
- `images-src/*.b64` — base64 sources for the cover art

## How images work

The GitHub file API used to publish this repo only accepts text, so cover
images are committed as base64 text under `images-src/`. The
`.github/workflows/decode-images.yml` workflow decodes them into real binary
files under `images/` on every push that touches `images-src/`.

To replace a cover: overwrite the corresponding `images-src/<name>.jpg.b64`
with fresh base64 and push — the workflow handles the rest.
