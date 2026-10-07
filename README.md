# portfolio.thehappaholic.com

Sivanja's portfolio — a static site. No build step.

```
index.html
CNAME            ← tells GitHub Pages the domain
img/me.jpg       ← polaroid photo (already added)
img/me-full.jpg  ← full-size photo (spare)
```

## Adding project screenshots
Each project file opens into a case study with a "screens" gallery. Drop images into `img/` with these
names and they appear automatically — any that are missing are hidden, so add them whenever you're ready.

| Project         | File names                         | Suggested shots                                   |
|-----------------|------------------------------------|---------------------------------------------------|
| Socials.lk      | `socials-1.png` … `socials-4.png`  | discover page, event page, QR ticket, organiser dashboard |
| drift           | `drift-1.png` … `drift-4.png`      | home screen, intervention, data flow diagram, dashboard |
| As a Happaholic | `blog-1.png`, `blog-2.png`         | landing page, a post                              |

Landscape screenshots around 1600×1000 look best. Captions are next to each `<img>` in `index.html` if you want to change them.

## Links to check
- The **GitHub button** in the drift file points to your GitHub profile. Search `index.html` for
  `Change this to the drift repo URL` and swap in the repo link.
- Your photo is embedded inside `index.html`, so it shows even if the page is opened on its own.
- Case-study text lives in the `<template id="file-…">` blocks near the bottom of `index.html`.

## Host it free on GitHub Pages
1. On GitHub (**thehappaholic**), create a public repo, e.g. `portfolio`.
2. Upload `index.html`, `CNAME` and the whole `img` folder (keep the folder name).
3. Repo → **Settings → Pages** → Source: *Deploy from a branch* → Branch `main`, folder `/ (root)` → Save.
4. Custom domain should show `portfolio.thehappaholic.com`.

## Point the subdomain at it (DNS)
Wherever thehappaholic.com's DNS is managed (on WordPress.com: **Domains → thehappaholic.com → DNS records → Add record**):

| Type  | Name / Host | Value                     |
|-------|-------------|---------------------------|
| CNAME | `portfolio` | `thehappaholic.github.io` |

Your blog at thehappaholic.com is not affected. DNS takes minutes to a few hours; once GitHub shows the
domain as verified, tick **Enforce HTTPS**.

## Updating later
Edit files on GitHub (pencil icon, or "Add file → Upload files" for images) and commit — the site redeploys in about a minute.
