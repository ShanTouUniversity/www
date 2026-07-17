# AGENTS.md — ShanTou.University (www)

## What this is

A [Zola](https://www.getzola.org) static site (v0.22.1, theme: [tabi](https://github.com/welpo/tabi) as git submodule). Unofficial Shantou University alumni platform. Bilingual: `zh-Hans` (default) + `en`.

## Build & dev

```sh
# Build (downloads Zola, then runs `zola build`)
./build.sh

# Or with local Zola:
zola build      # outputs to public/
zola serve      # dev server with live reload
```

`public/` is gitignored. No CI workflows exist.

## Content structure

```
content/
  _index.md         # homepage (zh-Hans), section_path points to blog/_index.md
  _index.en.md      # homepage (en)
  blog/             # posts — each post is a dir with index.md + index.en.md
  projects/         # projects — same bilingual dir pattern
  archive/          # archive page
```

Every bilingual post uses `content/some-post/index.md` (zh-Hans) and `content/some-post/index.en.md` (en).

## Theme

Theme is tabi, pinned via git submodule at `themes/tabi`. Only one template override exists: `templates/tabi/extend_head.html` (Google AdSense). Do not edit theme files directly.

To update the theme:
```sh
git submodule update --remote themes/tabi
```

## Key config (`config.toml`)

- `base_url = "https://shantou.University"`
- `default_language = "zh-Hans"`
- Taxonomies: `tags` only (with feeds per language)
- Email in config is base64-encoded
- `remote_repository_url` is set (GitHub integration in tabi)
- Mermaid, copy button, author display enabled
- `public/` in `.gitignore`

## Content conventions

- Zola front matter in `+++` delimiters
- Default `sort_by = "date"`, `paginate_by = 5` on blog
- Tags in front matter under `[taxonomies]` section
- Quick nav buttons, ToC toggle available via `[extra]`
- Post filenames: `/index.md` (zh-Hans) and `/index.en.md` (English) per directory
- Archive page at `content/archive/_index.md`

## Static assets

- `static/logo.webp` — site favicon & header image
- `static/.well-know/Security.txt` — security contact
- `static/ads.txt` — ad network verification
- `static/css/`, `static/res/` — additional assets

## What not to do

- Do not edit `themes/tabi/` files directly (submodule)
- Do not commit `public/` (gitignored)
- Do not overwrite `content/` posts without understanding bilingual structure
- Do not remove `build.sh` (also referenced by CI-like manual builds)
