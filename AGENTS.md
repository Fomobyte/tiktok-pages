# Repository Guidelines

## Project Structure & Module Organization

This repository is a small content-only site for `Creator Stats App`. All published content lives at the top level as Markdown files:

- `index.md`: landing page content
- `app-description.md`: short app summary
- `privacy-policy.md`: privacy notice
- `terms-of-service.md`: terms page

Keep new public pages in the repository root unless a real need for subdirectories appears. Use descriptive, kebab-case filenames such as `data-deletion.md`.

## Build, Test, and Development Commands

There is no build pipeline or package manager config in the current repo. Typical local checks are lightweight:

- `ls -1 *.md`: confirm expected page files exist
- `sed -n '1,80p' privacy-policy.md`: inspect a page quickly
- `python3 -m http.server`: preview the directory locally if you need a simple static server

If GitHub Pages or another static publisher is used, keep files plain Markdown with no generator-specific assumptions unless that tooling is added to the repo.

## Coding Style & Naming Conventions

Write in clear, professional Markdown. Use ATX headings (`#`, `##`) and short sections. Prefer sentence case for body text and consistent title case for headings. Keep lists flat and concise.

For policy pages, preserve the existing style:

- leading title heading
- `_Last updated: YYYY-MM-DD_` near the top when applicable
- short paragraphs and direct bullet lists

Use lowercase kebab-case for filenames. Avoid embedding secrets, tokens, account IDs, or private contact details in tracked files.

## Testing Guidelines

No automated test suite is present. Before submitting changes, manually verify:

- headings render correctly
- internal wording is consistent across related pages
- dates match the actual revision
- app purpose and data-handling statements do not conflict

If a markdown linter is added later, run it before opening a PR.

## Commit & Pull Request Guidelines

Local Git history is not available in this workspace, so no repository-specific commit convention could be derived. Use short, imperative commit subjects such as `docs: update privacy policy date`.

Pull requests should include:

- a brief summary of the document changes
- affected files
- any policy or compliance reason for the update
- rendered screenshots only if formatting changed materially in the published site
