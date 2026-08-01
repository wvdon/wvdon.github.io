# wvdon.github.io

Personal academic website of Weidong Wu — <https://wvdon.github.io>

Built with [Jekyll](https://jekyllrb.com/) and the [al-folio](https://github.com/alshedivat/al-folio) theme.

## Where things live

| What | File |
| --- | --- |
| Site-wide settings (name, URL, feature toggles) | `_config.yml` |
| Homepage bio | `_pages/about.md` |
| Publications | `_bibliography/papers.bib` |
| News items on the homepage and `/news/` | `_news/*.md` |
| Social links | `_data/socials.yml` |
| Accent colours | `assets/css/main.scss` |
| Profile photo | `assets/img/prof_pic.jpg` |

The site is deliberately kept to two nav entries, about and publications. The
theme also ships CV and blog sections; they are unused here. To bring one back,
restore `_pages/cv.md` + `_data/cv.yml` or `_pages/blog.md` + `_posts/` from git
history and re-enable `latest_posts` in `_pages/about.md`.

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
