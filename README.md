# adaaka.com

Personal academic website of Ada Aka, built with [Hugo](https://gohugo.io) and published with GitHub Pages.

**To change the website's content, see [EDITING.md](EDITING.md).**

## Layout

- `content/` — all page text (Markdown). One file per page, one file per paper.
- `static/images/` — headshot, paper figures, teaching photos.
- `hugo.toml` — site name, menu, homepage links.
- `layouts/`, `assets/css/style.css` — page templates and styling (rarely need changing).
- `.github/workflows/deploy.yml` — builds and publishes the site on every push to `main`.

## Local preview

```
brew install hugo
hugo server
```

Then open http://localhost:1313.

## Publishing

In the GitHub repository: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
Every push to `main` then rebuilds the site. To use the custom domain, enter `adaaka.com`
under **Settings → Pages → Custom domain** and point the domain's DNS at GitHub Pages.
