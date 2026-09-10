# Pranavbh1.github.io

Personal portfolio site for **Pranav Bhawsar** — AI Engineer.
Single self-contained `index.html`: no build step, no dependencies, no framework.

Live at → https://pranavbh1.github.io

---

## Publish it (5 minutes)

### 1. Create the repository

On https://github.com/new:

| Field | Value |
|---|---|
| Owner | `Pranavbh1` |
| Repository name | **`Pranavbh1.github.io`** ← must match the username exactly |
| Visibility | **Public** (required for free GitHub Pages) |
| Initialize with README | leave unchecked |

Click **Create repository**.

### 2. Upload the files

Easiest path — no terminal needed:

1. On the new empty repo page, click **uploading an existing file**.
2. Drag in `index.html`, `404.html` and `Pranav_Bhawsar_AI_Engineer_resume.pdf`.
3. Commit directly to `main`.

Or with git:

```bash
git init
git add index.html 404.html Pranav_Bhawsar_AI_Engineer_resume.pdf README.md
git commit -m "Portfolio site"
git branch -M main
git remote add origin https://github.com/Pranavbh1/Pranavbh1.github.io.git
git push -u origin main
```

### 3. Turn Pages on

**Settings → Pages → Build and deployment**
- Source: `Deploy from a branch`
- Branch: `main` / `(root)` → **Save**

Wait 1–2 minutes, then open **https://pranavbh1.github.io**.
(For a `user.github.io` repo Pages is usually enabled automatically — check the Settings page anyway.)

---

## Editing later

Everything lives in `index.html`. The parts you'll touch most:

| What | Where |
|---|---|
| Headline, tagline, intro | `<section class="hero">` near the top of `<body>` |
| Experience entries | `<section id="experience">` — copy a `.tl-item` block |
| Featured projects | `<section id="projects">` — copy an `<article class="card">` block |
| Skills | `<section id="skills">` — chips are `<span class="chip">` (`chip hi` = highlighted) |
| Colours | the `:root` block at the top of `<style>` (`--accent` is the mint green) |

The **From GitHub** section needs no maintenance — it fetches the latest repos from the
GitHub API on page load and sorts by stars, then recency. If the API rate-limits a visitor,
a hard-coded fallback list renders instead.

## Notes

- The résumé button links to `Pranav_Bhawsar_AI_Engineer_resume.pdf` in the repo root — keep the
  filename identical when you replace it with a newer version.
- The phone number from the résumé is deliberately **not** on the page (public pages get scraped
  by spam bots). It's still inside the PDF. To add it anyway, drop another `<span>` into the
  `.meta-row` block in the hero.
- Light and dark themes both ship; the toggle is top-right and the page follows the visitor's
  system preference on first load.

## Custom domain (optional)

Add a file named `CNAME` containing just your domain, e.g. `pranavbhawsar.com`, then point a
`CNAME` DNS record at `pranavbh1.github.io`. Enable **Enforce HTTPS** in Settings → Pages.
