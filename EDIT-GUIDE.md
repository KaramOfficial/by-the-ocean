# By The Ocean — Website Editing Guide

Everything needed to edit this site, written so a person **or an AI assistant
(Claude, ChatGPT, etc.)** can pick it up cold. If you're an AI reading this:
follow the "Rules" section exactly — they exist because of mistakes already made.

## The site

- **Business:** By The Ocean — luxury picnics, events & decor, Halifax, Nova Scotia
- **Live site (main):** https://karamofficial.github.io/by-the-ocean/
- **Live site (v2, Golden Hour colours):** https://karamofficial.github.io/by-the-ocean/v2/
- **Repo:** https://github.com/KaramOfficial/by-the-ocean
- **Booking is Instagram DM only:** every call-to-action points to
  https://www.instagram.com/events.bytheocean/

## How publishing works

- Hosted on **GitHub Pages**, served straight from this repo's `main` branch.
- **To publish: commit + push to `main`.** The live site updates in ~1–2 minutes.
  There is no build step and no other deploy.
- The repo is public (readable by anyone). To push directly you must be added
  as a **collaborator** (repo owner does this under Settings → Collaborators —
  you need a free GitHub account). Without that, fork the repo and open a
  pull request instead.

## Files

| File | What it is |
|---|---|
| `index.html` | The main site — one single file (HTML + precompiled CSS inside) |
| `v2/index.html` | The Golden Hour colour variant — a copy of `index.html` with a colour-override `<style id="golden-hour-overrides">` block in the `<head>`. **Content edits should be made in BOTH files** so the two versions differ only in colour. Its asset paths start with `../assets/` — keep them that way. |
| `assets/` | Photos, logo (`logo.jpg`), and self-hosted fonts (`assets/fonts/` + `assets/fonts/fonts.css`) |
| `EDIT-GUIDE.md` | This file |

Preview locally: run `python3 -m http.server` in the repo root, open
http://localhost:8000 (and http://localhost:8000/v2/ for the variant).

## Rules (important)

1. **Never invent business details.** No phone number, email, address, hours,
   prices, or testimonials — none exist publicly. Contact = Instagram DM only.
   Services/gallery content must come from the real Instagram
   (@events.bytheocean). If something isn't known, leave it out.
2. **Real photos only.** The pictures in `assets/` are the business's real
   Instagram photos. Don't swap in stock or AI images.
3. **Tailwind CSS is PRECOMPILED** into the `<style>` block in the HTML.
   Only utility classes already used somewhere in the file exist.
   **A brand-new Tailwind class will silently do nothing.** For new styling,
   use an inline `style="..."` attribute or reuse a class that already
   appears in the file — and always verify the rendered result (computed
   font-size / a screenshot), not just the markup.
4. **Fonts are self-hosted** (Playfair Display, Lora, Parisienne in
   `assets/fonts/`). Do NOT add Google Fonts links back.
5. **Hero headline style:** Parisienne script, all lowercase, currently:
   line 1 `a moment,` / line 2 `made just for you` — no full stops.
   It's set with an inline style for size (see rule 3 for why).
6. **Colours (main version):** warm clay ink `#6B4232`, cream `#FBF6EC`,
   sand `#F0E1CB` — warm, rustic/pastel, borrowed from the real logo + photos.
   No navy. (v2 differs on purpose: honey/terracotta/champagne + sea-blue
   buttons, all inside its override style block.)
7. **Logo** is only available at 150×150 — display it small (48px in the
   header) or it will look blurry.
8. After pushing, **verify the live URL actually updated** (hard-refresh;
   GitHub Pages/CDN can lag a minute or two) before saying an edit is done.

## A ready-made prompt for your AI

> You are helping me edit a small business website. The repo is
> https://github.com/KaramOfficial/by-the-ocean (GitHub Pages, plain HTML,
> no build step — push to `main` publishes). Read `EDIT-GUIDE.md` in the
> repo root first and follow its rules exactly, especially: never invent
> contact details or prices (booking is Instagram DM only), real photos
> only, Tailwind is precompiled so new utility classes won't work (use
> inline styles), and apply content edits to both `index.html` and
> `v2/index.html`. The change I want is: [DESCRIBE YOUR EDIT]. When done,
> show me a phone-width screenshot of the result before pushing.

## Design history (short)

Design originated in Boosterpack (style "Tidal Letter"), then was rebuilt
by hand on GitHub Pages with the real photos and warmer colours. `/v2/` is
the same site recoloured from an alternate style ("Golden Hour Riviera"),
kept as a preview — the owner may promote it later; don't delete it.
