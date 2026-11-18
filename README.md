# Commerce Notes & Birthday Gift

A static, self-contained site made with plain HTML, CSS, and JavaScript. It has no build step, framework, package installation, external CDN, or runtime network dependency.

## Files

- `index.html` — complete site source; the Notes workbook, gift experience, and bouquet media are embedded in the page.
- `assets/bouquet-still-life.jpg` and `assets/bouquet-still-life.png` — standalone copies of the photo-style bouquet still life.
- `assets/bouquet-companion-cutout.png` — transparent cutout used for the draggable bouquet companion.
- The earlier GLB and bouquet art files are retained in `assets/` as source material; the current site does not need WebGL or a network request to show the bouquet.

## Gift flow and privacy

The first screen is the Commerce Notes cover: 16 workbook pages with 64 sections. Tap **Set 19** three times in quick succession to reveal the birthday gift. The sequence is the opening birthday note, a dedicated bouquet page, Reasons You Matter, the book, and the existing separate closing card.

Using browser Back, switching away/backgrounding the page, or closing it returns to the Notes cover. On reopening, the gift is not displayed automatically; the recipient must deliberately unlock it again. Gift progress is still saved in the browser under `aarna-gift-progress-v1`, so an intentional unlock can continue from the last reading position.

The Reasons page includes a working **Menu** and a visible, draggable bouquet companion. The bouquet page uses a photo-style blush-rose still life and keeps its message: “Here's a bouquet, just as beautiful as you are.”

## Book reader

The reader turns one chapter at a time inside a paper-style book frame, with chapter navigation and a contents panel. The nine existing chapters and the new Chapter 10 are grouped as follows:

1. **The Beginning** — Chapters 1–3
2. **Getting to Know You** — Chapters 4–6
3. **What You Became to Me** — Chapters 7–9, followed by Chapter 10, **“The Year I Got to Know You”**
4. **A Birthday Message** — a separate reserved final part

The separate birthday-message page remains reserved for your own text. Chapter 9, **“Things I Hope You Know,”** remains in the book.

## Preview locally

From this folder, run:

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080`.

## Deploy

Keep `index.html` at the repository root and keep `assets/` alongside it. For Vercel, select **Other**, leave the build command empty, and use the project root as the output directory. For Cloudflare Pages, leave the build command empty and set the output directory to `.`.
