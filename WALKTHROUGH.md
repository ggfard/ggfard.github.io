# ggfard.github.io — Walkthrough

Personal academic site, moved from WordPress.com (ggfard.com) to GitHub Pages.
GitHub builds it with Jekyll automatically on every push; nothing needs to be installed.

## Where things live

| To change…                         | Edit this file              |
|-----------------------------------|-----------------------------|
| Colors, fonts                     | `_config.yml` → `style:`    |
| Email / CV link (empty = hidden)  | `_config.yml` → `email`, `cv` |
| Menu, profile links               | `_config.yml` → `nav`, `social` |
| Bio                               | `index.html`                |
| News                              | `_data/news.yml`            |
| Papers, chapters, posters         | `_data/publications.yml`    |
| Research projects                 | `_data/projects.yml`        |
| Media coverage, community talks   | `_data/media.yml`           |
| Page layout (header/footer)       | `_layouts/default.html`     |
| Spacing, sizes                    | `assets/css/style.css`      |
| Images / PDFs                     | `assets/img/`, `assets/files/` |

Adding a news item = add two lines at the top of `_data/news.yml`:
```yaml
- date: Dec 2026
  text: Something happened, with a [link](https://example.com).
```
You can edit any file directly on github.com (pencil icon) — the site rebuilds in ~1 minute.

## Steps log

1. **Content migration (2026-11-06).** Copied all content from ggfard.com's four pages
   (Home/News, Research Projects, Publications, Media & Outreach) into YAML data files.
   - Fixed "Bradly" → "Bradley" (npj Complexity author list).
   - Author names unified as "G. Gharooni-Fard" across all entries.
   - Added a draft bio on the home page (to be edited).
   - Dropped the WordPress comment box and share buttons.
2. **Design.** Clean single-column layout; colors and fonts are variables in `_config.yml`.
3. **Media.** The old site's images/PDFs are listed in `old-site-media.txt`.
   Run the GitHub Action *Copy media from old site* once (Actions tab → Run workflow) to copy
   them into the repo. Until then, gray placeholders are shown.
   Two portrait photos are copied: `profile.jpg` (shown) and `profile-alt.jpeg` (spare).
4. **Deploy.** Repo `ggfard/ggfard.github.io`, Settings → Pages → Deploy from branch `main` / root.

## To do
- [ ] Choose final colors/fonts
- [ ] Edit the bio
- [ ] Add email and CV (optional)
- [ ] Run the copy-media action, check images
- [ ] Decide what to do with ggfard.com (keep pointing to WordPress, redirect, or let it lapse)
