# REPERTORY / Staff Library

**An internal brand and design resource.** This is a complete, self-contained static website for the fictional Repertory identity system. It brings the identity's philosophy, formal standards, source artwork, exploratory applications, and two accepted interactive tools into one editorial environment.

The site is intended for future Repertory designers and production staff. **It is not a public-facing Repertory website.** The editorial cases are design studies, not announcements of actual ventures, commissioned editorial projects, or partnerships.

## Open the site

**Start at `index.html`.** Everything is already organized. You do not need to rename files, reorganize folders, install packages, configure an API, or run a build step.

For a quick local inspection, you can open `index.html` in your browser. **For reliable use of all browser capabilities**, especially the image-upload/processing features inside the Gnomon Builder and browser clipboard permissions, serve the extracted folder over `localhost`. If Python is installed:

```sh
cd repertory-staff-toolkit
python3 -m http.server 8000
```

Open `http://localhost:8000` in a browser. There is no backend; this command simply serves the already-built files locally. On Windows, `py -m http.server 8000` is an equivalent option.

## What is inside

| Page | Purpose |
|---|---|
| `index.html` | Internal home, manifesto excerpts, four-branch orientation and direct tool access |
| `foundations.html` | Stewardship philosophy, organizational architecture, live branch/figure-ground specimens, Gnomon rules and typography |
| `studies.html` | Four image-led, clearly labeled speculative editorial applications; branch filtering and design rationale |
| `reference.html` | Master document PDFs, source precedence, exact palette values, 48 original stickers, downloadable masters |
| `tools.html` | The two accepted tools, with context and previews |
| `tools/color-lab.html` | Color Lab v5 running inside the staff site |
| `tools/gnomon-builder.html` | Gnomon Builder v5 running inside the staff site |
| `tools/engines/` | **Byte-for-byte original accepted tool HTML**; the site wrappers do not modify the engines |
| `assets/` | Shared website styling/scripts, optimized reference photos, recolored exact-vector specimens, original vectors, approved patterns and the 48 original sticker SVGs |
| `docs/` | Manifesto, original prompt package, toolkit presentation, handoff, and operating notes |

The two tools also offer **Open standalone editor** links. Those files are self-contained and function independently of the surrounding portal.

## Publish to GitHub — the easiest route

1. **Unzip this package.** Keep the `repertory-staff-toolkit` folder together; do not upload the ZIP as the website itself.
2. Install [GitHub Desktop](https://desktop.github.com/) and sign in to GitHub.
3. In GitHub Desktop, choose **File → Add local repository**, browse to the extracted `repertory-staff-toolkit` folder, and select it. If GitHub Desktop says it is not yet a repository, choose its **Create a Repository Here** option.
4. Review the files in GitHub Desktop, enter an initial commit message such as `Initial internal toolkit`, and select **Commit to main**.
5. Choose **Publish repository**, enter the repository name `repertory-staff-toolkit`, and **select Private** unless you have decided to distribute the asset collection openly.

For publishing a static site on GitHub Pages, open the repository's **Settings → Pages**, choose **Deploy from a branch**, select **main** and **/(root)**, then save. Pages serves `index.html` from the repository root; relative links handle the rest, including all nested tools and the PDFs. Deployment may take a few minutes.

**Important:** GitHub Pages is not, by itself, employee access control. Depending on your GitHub plan and repository configuration, a Pages URL can be publicly reachable even when its source repository is private. If this is truly staff-only material, use a hosting service with authentication (such as an organization-managed static host behind SSO/access controls). The site's `noindex` settings discourage indexing but do **not** secure it.

## Using the site

Begin with the manifesto and Foundations. Choose the Repertory branch before assigning any institutional color. Consult the original masters for Gnomon geometry. Use the **Color Lab** to select the correct branch/theme/composition and copy specifications; use the **Gnomon Builder** to explore approved construction configurations, aspect ratios and export-ready transparent assets. Use the Reference desk to inspect/download the exact source SVGs.

The Library's editorial applications are intentionally diverse. The subjects' own colors and cultures are not automatically replaced by Repertory's branch colors. The application pages explain which decisions were made and which creative scenarios remain hypothetical.

## Technical notes

- **Stack:** ordinary HTML, CSS, and vanilla JavaScript; no bundler or third-party runtime dependencies.
- **Hosting:** static only; compatible with a root-level GitHub Pages deployment.
- **Tools:** unchanged accepted Color Lab v5 and Gnomon Builder v5, embedded in responsive same-origin iframes. They can be opened separately.
- **Photography:** optimized WebP derivatives of user-provided reference images, stored locally. Original user photography and outside-party rights should be reviewed before public distribution.
- **Vectors:** exact master paths are preserved. In `assets/marks/`, figure/ground examples recolor the original solid combination's paths only; their geometry is **not** redrawn.
- **Sticker art:** all 48 original, corrected SVG compositions are present in `assets/stickers/{Light,Midtone,Dark}/`.
- **Fonts:** proprietary Source Sans Pro and Meta Pro files were **intentionally not bundled**. The website uses a compatible system-font fallback for distribution. If your organization holds appropriate webfont licenses, your developer can add properly licensed font files and `@font-face` rules later.
- **Privacy:** photo uploads in Gnomon Builder are processed locally in the user's browser, not sent to a server by these tools.
- **Browser downloads:** some browsers may request permission for **multiple file downloads** when the Gnomon Builder produces its SVG and PNG in one click.

## A note on provenance

The formal assets and reference documents remain authoritative. Mockups and newly authored examples are **proposals** and should not silently become additions to Repertory's approved system. See [`docs/SOURCE_AND_RIGHTS.md`](docs/SOURCE_AND_RIGHTS.md).

**Package version:** Staff Library 1.0 / 19 November 2026  
**Accepted engines:** Color Lab v5 / Gnomon Builder v5
