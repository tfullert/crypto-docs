# crypto-docs

Cryptography notes built with [Quarto](https://quarto.org/) and published to GitHub Pages.

## Local development

1. Install Quarto: https://quarto.org/docs/get-started/
2. Preview: `quarto preview`
3. Build: `quarto render`

## Layout

- `index.qmd` — home page
- `about.qmd` — scope and tooling notes
- `topics/` — topic folders and `.qmd` notes (sidebar uses `contents: auto` via the `topics` directory in `_quarto.yml`)

## Publishing

This repo uses **GitHub Actions** to render on push to `main` and publish to the **`gh-pages`** branch.

After creating the remote repository on GitHub:

1. Enable **Settings → Actions → General → Workflow permissions → Read and write**.
2. Push `main`. The first successful run creates `gh-pages` and deploys the site.
3. If Pages does not auto-switch to `gh-pages`, set **Settings → Pages → Build from branch → `gh-pages` / root**.

Optional one-time local setup (requires Quarto): `quarto publish gh-pages` from a clone with `origin` configured.
