# revolucien.com

Static blog generated with Hugo. No database, no JavaScript, no dependencies to update.

## Where things are

- `content/posts/`: the posts, one `.md` file per piece. This is the only folder you open day to day.
- `content/about.md`: the About page.
- `content/_index.md`: the intro paragraph on the home page.
- `hugo.toml`: configuration (site title, description, Buttondown username).
- `static/style.css`: all the styling.
- `layouts/`: the HTML templates. You never need to touch them.

## Publishing a post

1. On github.com, open the `content/posts/` folder.
2. Click "Add file", then "Create new file".
3. Name the file in lowercase with hyphens, ending in `.md`. The file name becomes the page address: `my-first-essay.md` will be readable at `revolucien.com/my-first-essay/`.
4. Paste this template at the top of the file and write below it:

```
---
title: "The title of my post"
date: 2026-10-01
---

The text starts here.
```

5. Click "Commit changes" (the green button), then "Commit changes" again in the dialog. The site updates within a minute or two.

To fix a published post: open the file, click the pencil icon, edit, "Commit changes".

To keep an unpublished draft: add the line `draft: true` under the date. Remove it to publish.

## Formatting inside a post

- A paragraph = one blank line between two blocks of text.
- `## Subheading` for a section title.
- `**bold**`, `*italic*`.
- `[link text](https://address)` for a link.
- `> quote` at the start of a line for a quote.
- YouTube video: on YouTube, Share, Embed, copy the `<iframe ...></iframe>` code and paste it as is into the post.

## Deployment settings (Cloudflare Pages)

- Build command: `hugo --gc --minify`
- Build output directory: `public`
- Environment variable: `HUGO_VERSION` = `0.166.0`
