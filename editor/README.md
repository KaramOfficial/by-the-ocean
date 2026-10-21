# Editing the By The Ocean website — the easy way (no AI, no code)

This folder is your **word-processor version** of the homepage. You change
the words in one file, press one button, and out comes the finished page.

## What you need (one-time setup, ~5 minutes)

1. Install **RStudio** — it's free and it includes everything else:
   https://posit.co/download/rstudio-desktop/
2. Get this project onto your computer: on the GitHub page
   (https://github.com/KaramOfficial/by-the-ocean) click the green
   **Code** button → **Download ZIP**, then unzip it.

## Making a change (every time after that)

1. Open the folder, go into the **editor** folder, and double-click
   **index.qmd** (it opens in RStudio).
2. At the top of RStudio, click the **Visual** tab — the document now
   looks like a normal word-processor page. Click any words and type.
   *That's really all you edit — the words.*
3. Please don't delete lines that start with `:::` or anything between
   the `---` lines at the very top — those are the page machinery.
   (In Visual mode you mostly won't even see them.)
4. When you're happy, click **Render** (the blue arrow at the top).
   A finished page called **index.html** appears in the same editor
   folder. Open it in your browser to check it — what you see is
   exactly what visitors will get.

## Putting it live

Pick whichever is easier:

- **Easy:** send the new `index.html` file to Karam and he'll publish it.
- **Do it yourself** (once Karam has added your GitHub account as a
  collaborator): on the GitHub repo page click **Add file → Upload
  files**, drag your new `index.html` in, and press **Commit changes**.
  It replaces the old homepage, and the site updates in about 2 minutes:
  https://karamofficial.github.io/by-the-ocean/

## Good to know

- **Photos** live in the `assets` folder one level up. To swap a photo,
  replace the file there with a new one using the *exact same file
  name*, then Render again.
- **The golden-coloured version** of the site (the /v2/ page) is *not*
  covered by this editor — it shares the same words, so if you make a
  big wording change, tell Karam and he'll mirror it there.
- **Never add** a phone number, email, prices, or reviews to the page —
  the business takes bookings by Instagram DM only, on purpose.
- Stuck? The file **EDIT-GUIDE.md** in the main folder explains the
  whole setup, and any AI assistant (Claude, ChatGPT) can read it and
  help you from there.
