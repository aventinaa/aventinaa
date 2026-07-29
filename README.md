# Aventinaa — Website

A single-page, minimal, animated website for Aventinaa, built with plain HTML/CSS/JS
(no build step, no folder structure — everything lives in the repo root so it works
directly with GitHub Pages).

## Files

- `index.html` — the entire site (markup, styles, and script all in one file)
- `logo.png` — brand logo, used in the navbar, hero, about section, and footer
- `image1.jpg ... image8.jpg` — gallery photos (placeholders, replace with real jewellery photos)
- `link1.txt ... link8.txt` — one line each: the buy/enquiry link for the matching image
- `desc1.txt ... desc8.txt` — the description shown in the popup for the matching image

## How to update content

**To change a photo:** just replace `imageN.jpg` with your new photo, keeping the same filename
(e.g. overwrite `image3.jpg`). No code changes needed.

**To change a buy link:** open `linkN.txt` and replace the URL with your new link
(WhatsApp link, store link, Instagram DM link, anything).

**To change a description:** open `descN.txt` and edit the text — this is what shows up
in the popup when someone clicks a photo.

**To add more photos (9th, 10th, ...):** just add `image9.jpg`, `link9.txt`, `desc9.txt`
(and so on) to the repo root. The gallery automatically detects them — no code edits
required. It keeps checking `image1.jpg`, `image2.jpg`, `image3.jpg`... and stops at the
first missing number, so don't leave gaps in the numbering.

## Hosting on GitHub Pages

1. Push all files above to a single branch (e.g. `main`) at the repo root — no subfolders.
2. In the repo settings, go to **Pages** and set the source to that branch, root folder.
3. Your site will be live at `https://<username>.github.io/<repo-name>/`.

> Note: the automatic image/description/link detection uses `fetch()`, which requires
> the site to be served over `http(s)` — it will **not** work if you just double-click
> `index.html` on your computer (opening it as a `file://` URL). To test locally, run a
> simple local server, e.g. `python3 -m http.server` in the folder, then open
> `http://localhost:8000`.

## Customising

- Colors, fonts, and the gold/green/black theme are all defined as CSS variables at the
  top of the `<style>` block in `index.html` (`--green`, `--gold`, `--white`, `--black`).
- WhatsApp number and email are set in two places in `index.html`: the "Contact Us"
  section and the floating contact button — search for `wa.me/910000000000` and
  `hello@aventinaa.com` and replace with your real number/email.
