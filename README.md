# Jiamin Zhao Academic Website

This repository contains the source for a personal academic website built with
[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) and deployed
with GitHub Pages.

## Local Development

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
mkdocs serve
```

The site configuration is in `mkdocs.yml`, and page content lives in `docs/`.

## Deployment

Pushing to `main` runs the GitHub Actions workflow in
`.github/workflows/pages.yml`, builds the MkDocs site, and deploys it to GitHub
Pages.
