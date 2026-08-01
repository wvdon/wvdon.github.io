# wvdon.github.io

Personal academic website of Weidong Wu — <https://wvdon.github.io>

Built with [Jekyll](https://jekyllrb.com/) and the [al-folio](https://github.com/alshedivat/al-folio) theme.

## Where things live

| What | File |
| --- | --- |
| Site-wide settings (name, URL, feature toggles) | `_config.yml` |
| Homepage bio | `_pages/about.md` |
| Publications | `_bibliography/papers.bib` |
| CV content | `_data/cv.yml` |
| News items on the homepage | `_news/*.md` |
| Blog posts | `_posts/*.md` |
| Social links | `_data/socials.yml` |
| Accent colours | `_sass/_variables.scss` |
| Profile photo | `assets/img/prof_pic.png` |

## Adding a publication

Append a BibTeX entry to `_bibliography/papers.bib`. Useful extra fields: `abbr`, `html`, `pdf`,
`selected={true}` (shows it on the homepage), `additional_info` (e.g. co-first authorship),
`bibtex_show={true}`.

The quickest way to get a clean entry is content negotiation on the DOI:

```bash
curl -LH "Accept: application/x-bibtex" https://doi.org/10.1172/jci.insight.207157
```

## Deployment

Pushing to `master` runs `.github/workflows/deploy.yml`, which builds the site and pushes the result
to the `gh-pages` branch. GitHub Pages must therefore be configured to serve from `gh-pages`
(Settings → Pages → Build and deployment → Deploy from a branch → `gh-pages` / `/ (root)`).

## Local preview

Requires Ruby 3.x and Node 20:

```bash
bundle install
npm ci
bundle exec jekyll serve
```
