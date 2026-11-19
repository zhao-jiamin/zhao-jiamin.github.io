# Jiamin Zhao Academic Website

This repository contains the source for a personal academic website built with
[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) and deployed
with GitHub Pages.

## Editing The Site

- Update the homepage introduction and selected research in `docs/index.md`.
- Replace the profile photo by saving a new image at
  `docs/assets/images/profile.jpg`. If you use a different filename, update the
  image path in `docs/index.md`.
- Replace the navbar logo by saving the official IESE Business School logo at
  `docs/assets/iese-logo.png`. Keep that filename, or update the path in
  `overrides/main.html` if you choose a different asset.
- For Google Search Console, paste your real HTML-tag verification token into
  `extra.google_site_verification` in `mkdocs.yml`. Leave it empty until then;
  the generated site will not include a verification tag without a token.
- Update the LinkedIn link in `overrides/main.html`.
- Replace the CV by saving the latest PDF at `docs/assets/cv.pdf`.
- Add or edit research papers in `docs/research.md`, then update the selected
  research links in `docs/index.md`. Put paper PDFs in `docs/assets/` only when
  a public draft is available.
- Replace the public job market paper draft at `docs/assets/job-market-paper.pdf`
  to update the existing PDF links without changing the page content.
- Replace the public NGO-activism paper at `docs/assets/ngo-activism-paper.pdf`
  to update its download link; revise the title and abstract in
  `docs/research.md` if the paper's content changes.
- Replace the coauthored automated-access paper at
  `docs/assets/automated-access-paper.pdf`. Its Figure 1 and Figure 4 images
  are in `docs/assets/images/automated-access-figure-1.png` and
  `docs/assets/images/automated-access-figure-4.png`; update their captions
  and alt text in `docs/research.md` if the figures change.
- The JMP map and topic chart come from slides 3 and 16 of the November 2026
  presentation. Replace `docs/assets/images/labor-activism-geography.png` and
  `docs/assets/images/labor-activism-topic-coefficients.png` to update them;
  review their captions and alt text in `docs/research.md` when doing so. The
  map preview shows the left half of a two-map image; if its layout changes,
  adjust `.paper-figure__image--map` in the stylesheet.
- Add or edit publications in `docs/publications.md`.
- Update teaching information in `docs/teaching.md`.
- Add or edit media mentions and short posts in `docs/insights.md`.
- Update the visible navigation, CV link, and contact email in
  `overrides/main.html`. The `nav` list in `mkdocs.yml` includes secondary pages
  so MkDocs tracks every page, while the visible header stays concise.
- Update typography, spacing, and responsive layout in
  `docs/assets/stylesheets/extra.css`.

The generated files in the repository root, such as `index.html`, `research/`,
`publications/`, `insights/`, and `assets/`, are deployment output. Edit the
source files in `docs/`, `overrides/`, and `mkdocs.yml` instead.

## Local Development

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
mkdocs serve
```

Open the local URL printed by `mkdocs serve`, usually
`http://127.0.0.1:8000/`.

## Deployment

Pushing to `main` runs the GitHub Actions workflow in
`.github/workflows/pages.yml`. The workflow runs `mkdocs build --strict`, copies
the built site to the repository root for the current GitHub Pages setup, and
deploys the MkDocs artifact to GitHub Pages.

## Search Indexing

The site uses `site_url` in `mkdocs.yml`, which lets MkDocs generate
`sitemap.xml`. The `docs/robots.txt` file allows indexing and points crawlers to
the sitemap.
