# Cat Love Toys — Jekyll Site

This is the starter site for catlovetoys.com — built with Jekyll so it runs free on GitHub Pages, with a Markdown-based blog and hand-coded pages everywhere else.

## What's in here

```
catlovetoys-site/
├── _config.yml          site settings
├── Gemfile              tells GitHub Pages which Jekyll version/plugins to use
├── CNAME                your custom domain (catlovetoys.com)
├── index.md             homepage
├── blog.md              blog listing page (/blog/)
├── about.md             About / Alfi tribute link
├── toys.md              toy category landing page (/toys/)
├── _posts/               all blog posts (Markdown, one file per post)
├── _layouts/             page templates (default.html, post.html)
├── _includes/            header.html, footer.html
└── assets/css/style.scss  site styling
```

## 1. Push this to GitHub

```bash
cd catlovetoys-site
git init
git add .
git commit -m "Initial site scaffold"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/catlovetoys-site.git
git push -u origin main
```

(Create the empty repo on GitHub first, without a README, so there's no merge conflict.)

## 2. Turn on GitHub Pages

1. Go to your repo → **Settings → Pages**
2. Under "Build and deployment", set **Source: Deploy from a branch**
3. Branch: `main`, folder: `/ (root)`
4. Save. GitHub will build the site automatically (takes 1–2 minutes) and give you a URL like `https://YOUR-USERNAME.github.io/catlovetoys-site/`

## 3. Point your domain (catlovetoys.com) at it

At your domain registrar (wherever you bought catlovetoys.com), add these DNS records:

**For the root domain (catlovetoys.com):**
Add 4 A records pointing to GitHub's IPs:
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**For www (optional but recommended):**
Add a CNAME record:
```
www → YOUR-USERNAME.github.io
```

Then back in **GitHub → Settings → Pages → Custom domain**, enter `catlovetoys.com` and save (the `CNAME` file in this repo already has this set, but GitHub re-checks it here too). Once DNS propagates (can take up to 24–48 hours, often much faster), tick **Enforce HTTPS**.

## 4. Adding a new blog post

Add a new file in `_posts/` named exactly:
```
YYYY-MM-DD-your-slug.md
```
with this front matter at the top:
```yaml
---
layout: post
title: "Your Post Title"
date: 2026-09-01
categories: [behavior-training]   # or health-diet, fun-lifestyle, toys
tags: [your, keywords, here]
excerpt: "One or two sentence summary for previews/SEO."
---
```
Everything below the `---` is your post content in Markdown.

## 5. Local preview (optional, needs Ruby installed)

```bash
bundle install
bundle exec jekyll serve
```
Then open `http://localhost:4000` to preview before pushing.

## Next steps for the site

- [ ] Add real product images/affiliate links once Amazon Associates is approved
- [ ] Build out `/toys/interactive/`, `/toys/teasers-wands/`, etc. as individual category pages
- [ ] Add `/furniture/`, `/food/`, `/treats/`, `/litter/` sections in Phase 2
- [ ] Swap in real Alfi cartoon assets from toonbee once ready
