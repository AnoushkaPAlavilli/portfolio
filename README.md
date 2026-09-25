# portfolio

Personal academic site, built with [Jekyll](https://jekyllrb.com/) and the
[al-folio](https://github.com/alshedivat/al-folio) theme.

## Running it locally

```bash
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000/portfolio/> (the `/portfolio/` suffix comes from
`baseurl` in `_config.yml`, since this is a GitHub project page rather than a user page).

If `bundle install` fails while compiling a native gem with a linker error about
`MacOSX27.0.sdk` and `unknown architecture arm64e.x1`, the Command Line Tools' default
SDK is newer than the linker can read. Pin it to the previous SDK for the build:

```bash
SDKROOT=/Library/Developer/CommandLineTools/SDKs/MacOSX26.5.sdk bundle install
```

## Where the content lives

| What | Where |
| --- | --- |
| Bio, profile photo, homepage layout | `_pages/about.md` |
| News items on the homepage | `_news/*.md` (one file per item) |
| Publications | `_bibliography/papers.bib` — `selected={true}` also puts an entry on the homepage |
| Projects | `_projects/*.md` |
| Resume | `_pages/resume.md`, serving `assets/pdf/Alavilli_Resume.pdf` |
| Site title, name, URL, feature flags | `_config.yml` |
| Social links | `_data/socials.yml` |
| Venue badge colors | `_data/venues.yml` |
| Coauthor links | `_data/coauthors.yml` |

## Deploying

`.github/workflows/deploy.yml` builds the site on every push to `main` and publishes
`_site` to the `gh-pages` branch. GitHub Pages needs to be pointed at `gh-pages` (Settings
→ Pages → Build and deployment → Deploy from a branch → `gh-pages` / `root`).

Responsive WebP generation (`imagemagick` in `_config.yml`) is off, because ImageMagick
isn't installed locally. The CI build does install it, so flipping `enabled: true` works
as long as you also `brew install imagemagick` for local builds.
