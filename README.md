# Personal homepage + blog (Jekyll, GitHub Pages)

## Put it online (about 10 minutes, free)

1. Sign in to GitHub as **liplahm** and create a new **public** repository named exactly
   `liplahm.github.io`.
2. Upload everything in this folder to the repository: on the repository page choose
   **Add file → Upload files**, drag the *contents* of the folder in (not the folder itself),
   and commit.
3. Open **Settings → Pages**. Under *Build and deployment* choose **Deploy from a branch**,
   branch **main**, folder **/ (root)**, and save.
4. After a minute or two the site is live at **https://liplahm.github.io**.
   (The Actions tab shows the build; a red cross there means a typo in a file.)

To use a different repository name (for example `homepage`), set in `_config.yml`:
`baseurl: "/homepage"`. The site is then at `https://liplahm.github.io/homepage`.

## Edit your details

| What | Where |
|---|---|
| Name, email, links, office, CV, photo | `_config.yml` |
| Intro paragraphs, research interests, education | `index.html` |
| Papers and manuscripts | `_data/papers.yml` |
| Projects | `_data/projects.yml` |
| Notes and reports | `_data/notes.yml` |
| Colours and fonts | `assets/css/style.css` (tokens at the top) |

- **Photo:** upload a square image to `assets/img/profile.jpg`, then set
  `photo: "/assets/img/profile.jpg"` in `_config.yml`.
- **CV:** upload `assets/files/cv.pdf`, then set `cv_pdf: "/assets/files/cv.pdf"`.
  A "CV" link appears in the header and contact block.
- **Paper PDFs:** put them in `assets/files/` and set `pdf: "/assets/files/name.pdf"` for the entry.
  Empty fields (`""`) are simply hidden.

## Write a blog post

Create a file in `_posts/` named `YYYY-MM-DD-short-title.md`, e.g.
`_posts/2026-11-02-syndrome-decoding.md`, starting with:

```markdown
---
title: "Syndrome decoding for reconciliation"
summary: "One line shown on the blog index."
tags: [LDPC, CV-QKD]
---

Your text in Markdown.
```

You can do this directly on github.com (**Add file → Create new file**); the post is live a
minute after you commit. It appears on `/blog/`, in the "From the blog" list on the homepage,
and in the RSS feed (`/blog/feed.xml`). Delete `_posts/2026-10-20-starting-this-blog.md` once
you have a real first post.

**Maths:** write `$$ ... $$` for every equation. Inside a sentence it renders inline
(`the rate $$\beta I_{AB} - \chi_{BE}$$ is ...`); on its own lines, with a blank line before
and after, it renders as a displayed equation. Single `$` is not supported, so that ordinary
dollar signs stay safe.

**Images:** put them in `assets/img/` and write `![alt text](/assets/img/figure.png)`.

## Preview on your own computer (optional)

Install Ruby, then in this folder run `bundle install` once and `bundle exec jekyll serve`,
and open http://localhost:4000.
