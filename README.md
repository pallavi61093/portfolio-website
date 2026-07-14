# Pallavi — Personal Portfolio

A single-page personal portfolio (plus a blog) for **Pallavi Agrawal** — Technology
Leader, Speaker, Community Builder & Writer. Built as a plain static site (HTML + CSS +
a little JavaScript) so it can be hosted on GitHub Pages with zero build tooling.

The design is an editorial cream-and-navy theme inspired by a Canva template: serif
display headings (Playfair Display), a clean sans body (Inter), alternating light/dark
sections, and a contact footer.

## Structure

```
portfolio-website/
├── index.html          # The main one-page site (hero, about, career, speaking, community, writing, now, contact)
├── styles.css          # All styling (shared by the site and the blog)
├── script.js           # Mobile nav toggle + footer year
├── .nojekyll           # Tells GitHub Pages NOT to run Jekyll (keeps _template.html etc.)
├── assets/
│   └── README.txt      # Drop your portrait here as pallavi.jpg
└── blog/
    ├── index.html      # Blog listing page
    └── posts/
        ├── design-observability-before-you-buy.html   # Starter post
        └── _template.html                              # Copy this to add new posts
```

## Add your photo

Save a portrait photo as `assets/pallavi.jpg` (see `assets/README.txt`). Until then the
hero shows a labelled placeholder.

## Add a blog post

1. Copy `blog/posts/_template.html` to a new file, e.g. `blog/posts/my-new-post.html`.
2. Edit the parts marked `CHANGE:` (title, meta line, headline, body).
3. Add a card linking to it in `blog/index.html` (copy the existing `<a class="post-card">` block).

That's it — no build step.

## Deploy to GitHub Pages

Your repo already exists: https://github.com/pallavi61093/portfolio-website

From this folder, push the site to the repo's `main` branch:

```bash
git init
git add .
git commit -m "Add portfolio website"
git branch -M main
git remote add origin https://github.com/pallavi61093/portfolio-website.git
git push -u origin main
```

Then enable Pages:

1. Go to the repo on GitHub → **Settings** → **Pages**.
2. Under **Build and deployment**, set **Source** = *Deploy from a branch*.
3. Choose branch **main** and folder **/ (root)**, then **Save**.
4. After a minute, your site is live at:

   **https://pallavi61093.github.io/portfolio-website/**

## Things to double-check / personalise

- **LinkedIn URL** — currently set to `https://www.linkedin.com/in/pallavi-agrawal/` as a
  best guess. Update it in `index.html` (hero social link + contact section) if different.
- **Email** — set to `pallavi.61093@gmail.com` (from your CV).
- **Photo** — add `assets/pallavi.jpg`.
- **Talks / posts** — add more as you go.
