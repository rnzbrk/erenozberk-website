# erenozberk.com

## What is where

```
docs/                    ← Netlify serves this folder. Everything visitors see.
  index.html             ← Portfolio homepage
  blog/
    index.html           ← Blog listing page (hand-coded)
    posts/
      mst-ata/
        index.html       ← Rendered blog post
        index_files/     ← Figures for the post

blog/                    ← Quarto source files (not served directly)
  _quarto.yml            ← Quarto config — outputs to ../docs/blog
  posts/
    mst-ata/
      index.qmd          ← Source for the MST/ATA post

netlify.toml             ← Tells Netlify: serve docs/, no build needed
```

## How to add a new blog post

1. Create `blog/posts/my-new-post/index.qmd`
2. Write your post (R/Python code included)
3. In RStudio Terminal: `quarto render blog`
4. Add an entry to `docs/blog/index.html` (copy an existing post-card block)
5. Commit and push to GitHub
6. Netlify deploys automatically

## How to edit the portfolio

Edit `docs/index.html` directly and push.
