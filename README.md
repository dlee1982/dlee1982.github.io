# Personal site

A minimal Jekyll blog, hosted free on GitHub Pages.

## One-time setup

1. Create a free GitHub account at <https://github.com> if you don't have one.
2. Create a new **public** repository named exactly:

   ```
   dlee1982.github.io
   ```

   (Use your real username. This exact name is what makes the site live at
   `https://dlee1982.github.io` with no extra config.)

3. Edit `_config.yml` — set `title`, `author`, `email`, `github_username`,
   and change `url` to `https://dlee1982.github.io`.

4. From this folder, push it up:

   ```bash
   git init -b main
   git add .
   git commit -m "Initial site"
   git remote add origin https://github.com/dlee1982/dlee1982.github.io.git
   git push -u origin main
   ```

5. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a
   branch**, branch `main`, folder `/ (root)`. Save.

Give it 1–2 minutes, then visit `https://dlee1982.github.io`.

## Writing a post

Add a Markdown file to `_posts/` named `YYYY-MM-DD-slug.md`:

```markdown
---
title: "The title of the post"
date: 2026-10-05
summary: "One line that shows up on the homepage."
---

Your writing goes here. Plain Markdown.
```

Then:

```bash
git add . && git commit -m "New post" && git push
```

It's live in about a minute.

## Editing without the command line

You can write posts directly on github.com: open the `_posts` folder →
**Add file → Create new file** → name it `YYYY-MM-DD-slug.md` → write → commit.
Same result, no terminal.

## Files

| File / folder        | What it is                                  |
|----------------------|---------------------------------------------|
| `_config.yml`        | All your personal settings. Start here.     |
| `_posts/`            | One Markdown file per post.                 |
| `about.md`           | The About page.                             |
| `assets/css/style.css` | All styling, in one plain CSS file.       |
| `_layouts/`          | Page templates. Rarely need changing.       |

## Custom domain (optional, ~$10/yr)

The site is free forever at `username.github.io`. If you later buy a domain,
add a file named `CNAME` containing just your domain, then point your domain's
DNS at GitHub Pages. HTTPS stays free and automatic.

## Previewing locally (optional)

Requires Ruby. Not needed — GitHub builds the site for you.

```bash
bundle install
bundle exec jekyll serve
```
