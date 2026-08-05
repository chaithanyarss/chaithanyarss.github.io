# chaithanyarss.github.io

Personal academic website, served by GitHub Pages at
[chaithanyarss.github.io](https://chaithanyarss.github.io).

## Where things live

| Path | Contents |
| --- | --- |
| `_pages/about.md` | The homepage (bio and publication list). This is the only page with real content. |
| `_config.yml` | Site title, author profile, social links, theme settings. |
| `_data/navigation.yml` | Header links. All are currently commented out, since the site is a single page. |
| `files/` | Uploads such as `CV.pdf`, served from `/files/CV.pdf`. |
| `images/` | Favicons and the author avatar (`profile.jpg`, set as `author.avatar` in `_config.yml`). |
| `_layouts/`, `_includes/`, `_sass/`, `assets/` | Theme internals. Rarely need editing. |

The archive and sitemap templates under `_pages/` are unused scaffolding kept
from the upstream theme, and are the starting point if a Publications, Talks, or
Blog section is ever added, in which case the matching collection is already
declared under `collections:` in `_config.yml`. Their `permalink` is commented
out, which does not disable them: they still build, at a default URL under
`/_pages/`. They carry `sitemap: false` so that search engines are not pointed
at them. To put one into service, give it a real `permalink`, drop the
`sitemap: false`, and add a link in `_data/navigation.yml`.

## Previewing locally

Dependencies are installed into `vendor/bundle` (see `.bundle/config`), so a
one-time setup is:

```bash
brew install ruby       # if the system Ruby is too old
gem install bundler
bundle install
```

Then, to serve the site at `localhost:4000` with live reload on change:

```bash
bundle exec jekyll serve -l -H localhost
```

## Credits

Built on the [Academic Pages](https://github.com/academicpages/academicpages.github.io)
template, itself derived from the
[Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) Jekyll theme,
© 2016 Michael Rose, released under the MIT License (see `LICENSE`).
