# Jiamin Zhao Academic Website

This repository contains the source for a personal academic website built with
[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) and deployed
with GitHub Pages.

## Editing The Site

- Update the homepage bio and profile details in `docs/index.md`.
- Replace the profile photo by saving a new image at
  `docs/assets/images/profile.jpg`. If you use a different filename, update the
  image path in `docs/index.md`.
- Replace the CV by saving the latest PDF at `docs/assets/cv.pdf`.
- Add or edit research papers in `docs/research.md`. Put paper PDFs or slides in
  `docs/assets/` and link to them from the relevant paper card.
- Add or edit publications in `docs/publications.md`.
- Update teaching information in `docs/teaching.md`.
- Update the top navigation in `mkdocs.yml`.

The generated files in the repository root, such as `index.html`, `research/`,
`publications/`, and `assets/`, are deployment output. Edit the source files in
`docs/` and `mkdocs.yml` instead.

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
