# marcobalduini.com

Personal website of Marco Balduini, built with [Jekyll](https://jekyllrb.com/) and the
[Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) theme, published with
GitHub Pages from the `master` branch.

## Structure

- `_config.yml`: site settings, theme version (`remote_theme`, pinned), per-folder language
  defaults (`lang`, `locale`, `author`).
- `_data/authors.yml`: sidebar bio and links, one entry per language (`en`, `it`).
- `_data/navigation.yml`: top menu per language (`main`, `main_it`) and language homes.
- `_data/publications.yml`: publications list, rendered by `_includes/publications.html`.
- `_data/projects.yml`, `_data/teaching.yml` (and `*_it.yml`): Projects and Teaching
  entries, rendered as cards by `_includes/cards.html`.
- `index.md`: home page (intro, pillars, Now section).
- `_pages/`: English pages (About, Projects, Teaching, Publications, Contact, Privacy,
  Cookies, 404); `_pages/it/`: Italian pages. Pages that translate each other share the
  same `ref`, used for hreflang links and the IT/EN switcher.
- `_includes/masthead.html`, `_includes/footer.html`: theme overrides for the bilingual
  menu and the footer.
- `_includes/head/custom.html`: favicons, hreflang links, external links in a new tab,
  GoatCounter analytics (production builds only).
- `_includes/schema.html`: overrides the theme file (4.28.1) with a schema.org `Person`
  JSON-LD block. Re-check it whenever the theme version is bumped.
- `_pages/awards.md`: redirect from `/awards/` to `/publications/#awards`.
- `assets/css/main.scss`: theme stylesheet plus a few custom rules (font size, home grid,
  timeline, cards, publications).

## Local build (Docker)

No local Ruby is needed:

```bash
docker run --rm -it -p 4000:4000 -v "$PWD":/srv/site -v mb-gems:/usr/local/bundle \
  -w /srv/site ruby:3.3 \
  bash -c "bundle install && bundle exec jekyll serve --host 0.0.0.0 --force_polling"
```

Then open http://localhost:4000.

Link check on a fresh build:

```bash
docker run --rm -v "$PWD":/srv/site -v mb-gems:/usr/local/bundle -w /srv/site ruby:3.3 \
  bash -c "bundle install && bundle exec jekyll build && bundle exec htmlproofer _site --disable-external"
```

## Updating the theme

Change the version in `remote_theme: mmistakes/minimal-mistakes@<version>`, rebuild,
compare `_includes/schema.html`, `masthead.html` and `footer.html` with the theme's versions and check every page.
