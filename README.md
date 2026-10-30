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
- Update the Google Search Console verification tag by replacing the
  `PASTE_GOOGLE_SEARCH_CONSOLE_VERIFICATION_CODE_HERE` value in
  `overrides/main.html` with the verification code from Google.
- Update the LinkedIn link in `overrides/main.html`.
- Replace the CV by saving the latest PDF at `docs/assets/cv.pdf`.
- Add or edit research papers in `docs/research.md`, then update the selected
  research links in `docs/index.md`. Put paper PDFs in `docs/assets/` only when
  a public draft is available.
- Replace the public job market paper draft at `docs/assets/job-market-paper.pdf`
  to update the existing PDF links without changing the page content.
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
