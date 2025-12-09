# MAED2 demo site

This site consumes the shared `page-template` theme.

## How to run locally
1) Update `_config.yml` `remote_theme: YOUR-ORG_OR_USER/page-template@main` after you push the theme repo.
2) Install deps: `bundle install`.
3) Serve: `bundle exec jekyll serve`.

## Deployment flow
- Source/content stays here.
- Layouts/includes/assets come from `page-template` via `remote_theme`.
- If you need a site-specific override, place a file with the same path/name here (e.g., `assets/img/logo.png`).

Website for MAED

## Non-technical editing via GitHub Issues → Pull Request

Editors can submit content updates without touching code, and the workflow will open a PR automatically for maintainers to review and merge.

1) Create an edit request
- Go to GitHub → Issues → New issue → "Edit existing page/content"
- Choose the page (e.g., `about.markdown`) and paste the new body in Markdown

2) Automation opens a PR
- Workflow `.github/workflows/issue-content-to-pr.yml` creates a pull request that updates the selected file while preserving its front matter
- Maintainers review and merge; GitHub Pages will rebuild

Media uploads
- Upload images in the GitHub web UI to `assets/img/` and reference as `/assets/img/<filename>` in Markdown

## No third-party option (GitHub Issues → PR)

For editors who don’t want to touch code and don’t want external services:

1) Create an edit request
- Go to GitHub → Issues → New issue → "Edit existing page/content"
- Choose the page (e.g., `about.markdown`) and paste the new body in Markdown

2) Automation opens a PR
- Workflow `.github/workflows/issue-content-to-pr.yml` creates a pull request that updates the selected file while preserving its front matter
- Maintainers review and merge; GitHub Pages will rebuild

Notes
- This flow works for the existing Markdown pages listed in the form. Extend the dropdown in `.github/ISSUE_TEMPLATE/edit-content.yml` to allow more files.
- Images: upload to the repo via the GitHub web UI under `assets/img/` and reference as `/assets/img/<filename>` in the Markdown body.
# maed2.github.io
