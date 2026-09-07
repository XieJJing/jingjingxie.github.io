# Jingjing Xie — Academic Website

A single-file, dependency-free academic homepage. Everything lives in `index.html`
(inline CSS + a tiny theme-toggle script). No build step, no framework.

## Preview locally

Just open the file:

```bash
open index.html          # macOS
```

Or serve it (so relative paths / the avatar load cleanly):

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Photo

The About section shows `photo.jpg` (at the repo root, next to `index.html`).
Replace that file to change the picture — any landscape image works well.

## Deploy to GitHub Pages (free)

1. Create a repo named `<your-username>.github.io`.
2. Put `index.html` and `assets/` at the repo root and push:
   ```bash
   git init && git add . && git commit -m "site"
   git branch -M main
   git remote add origin git@github.com:<your-username>/<your-username>.github.io.git
   git push -u origin main
   ```
3. In the repo: **Settings → Pages → Source → main / root**.
4. Your site is live at `https://<your-username>.github.io` in ~1 minute.

To use a custom domain later, add a `CNAME` file with your domain and set the DNS record.

## Editing

- **Publications / News / Experience** — each is a plain HTML block in `index.html`;
  copy an existing entry and edit the text.
- **Scholar link** — replace the `scholar.google.com/` href in the header with your
  profile URL once you have one.
- **Colors** — tweak the `:root` variables at the top of the `<style>` block.
