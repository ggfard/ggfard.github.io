# ggfard.github.io — Walkthrough

Personal academic site, moved from WordPress.com (ggfard.com) to GitHub Pages.
Plain HTML + one CSS file. No build step: what you see in the preview is exactly what goes live.

## Files

| File / folder         | What it is |
|-----------------------|------------|
| `index.html`          | Home: photo, bio, profile links, News |
| `research.html`       | Research projects |
| `publications.html`   | Papers, book chapters, posters |
| `outreach.html`       | Media coverage, community talks |
| `style.css`           | All styling. **Colors, fonts, sizes are at the top.** |
| `assets/img/`         | Photos (`profile.jpg` = home photo), `research/`, `media/` |
| `assets/files/`       | PDFs (posters, CV) |
| `old-site-media.txt` + `.github/workflows/` | One-time helper that copies images/PDFs from the old site |
| `.nojekyll`           | Tells GitHub to serve the files as-is |

## One-time setup (Mac)

1. Install **VS Code**: https://code.visualstudio.com
2. In VS Code: Extensions (left sidebar, squares icon) → search **Live Preview** (by Microsoft) → Install.
3. Install **GitHub Desktop**: https://desktop.github.com → sign in with your GitHub account.
4. Unzip `ggfard.github.io.zip`, put the folder somewhere permanent (e.g. Documents).

## Edit and preview (nothing goes public)

1. VS Code → File → Open Folder → choose the `ggfard.github.io` folder.
2. Open `index.html`, then right-click in the editor → **Show Preview** (or the preview icon, top right).
3. Edit any file and save (⌘S): the preview updates immediately.
   - Text: edit the words between the tags, e.g. `<p>your bio here</p>`.
   - Colors / fonts / sizes: edit the top block of `style.css`.
   - New news item: copy one `<li>…</li>` line in `index.html`, change date and text.
   - New paper: copy one `<div class="pub">…</div>` block in `publications.html`.
   - Menu or footer: they are repeated at the top/bottom of all 4 pages, change each one.
   - Change font: pick one on fonts.google.com → "Get embed code" → replace the `fonts.googleapis.com` link
     in the `<head>` of each page, and set `--font` / `--heading-font` in `style.css`.
   - Replace a photo: put a new file in `assets/img/` with the same name (or change the `src="…"`).

## Publish (first time)

1. GitHub Desktop → File → **Add Local Repository** → choose the folder.
2. Click **Publish repository**. Name: `ggfard.github.io`. **Untick** "Keep this code private". Publish.
3. On github.com, open the repo → Settings → Pages → Source: "Deploy from a branch",
   Branch: `main`, folder `/ (root)` → Save.
4. Repo → **Actions** tab → "Copy media from old site" → **Run workflow** (copies all images and PDFs).
   Then in GitHub Desktop click **Fetch origin** / **Pull** to get them on your Mac.
5. After ~1 minute the site is live at https://ggfard.github.io

## Publish (every later change)

GitHub Desktop → write a short summary (bottom left) → **Commit to main** → **Push origin**.
Live in about a minute.

## Steps log

1. **Content migration (2026-11-06).** Copied all content from ggfard.com's four pages.
   Fixed "Bradly" → "Bradley"; author names unified as "G. Gharooni-Fard"; dropped WordPress
   comments/share buttons; draft bio added (to be replaced).
2. **Style.** Background #f9f5f1, text #1f2328, muted #6a6f76, links #a0522d; Source Serif 4.
3. **Switched from Jekyll to plain HTML (2026-11-06)** so every edit can be previewed locally
   with VS Code Live Preview before publishing.

## To do
- [ ] Write the bio (`index.html`)
- [ ] Adjust styling to taste (`style.css`)
- [ ] Publish repo, enable Pages, run the copy-media action, check images
- [ ] Optional: add email / CV (commented lines in `index.html`)
- [ ] Decide what to do with ggfard.com (keep, redirect, or let lapse)
