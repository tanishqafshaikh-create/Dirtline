# Dirtline

A website for buying and selling used mountain bikes. It is one file (`index.html`) with no build step and nothing to install.

## What it does

- Opening scene: a rider on a mountain bike rolls in along a trail (click "Replay" to watch it again)
- Browse bikes and filter by type of riding, wheel size, frame size, suspension, condition and max price (in ₹)
- Search, sort, and save bikes with a heart
- Compare up to 3 bikes side by side
- A "Featured ads" banner with moving graphics: a scrolling ticker, bikes that roll in with speed lines, and ads that rotate every few seconds (pauses on hover, respects reduced-motion settings)
- Open a bike to see its specs, description and seller contact
- Sell a bike in three steps, with an optional photo and a live preview card
- Light and dark themes follow the visitor's device settings

## Run it on your computer

Double-click `index.html`. It opens in your browser.

## Put it on GitHub and publish it for free (GitHub Pages)

1. Go to https://github.com/new and create a public repository, for example `dirtline`.
2. Click **uploading an existing file**, drag in `index.html` and `README.md`, then click **Commit changes**.
3. Open **Settings**, then **Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, then click **Save**.
5. After a minute or two the site is live at `https://YOUR-USERNAME.github.io/dirtline/`.

With git in a terminal instead:

```bash
cd dirtline
git init
git add index.html README.md
git commit -m "Add Dirtline"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/dirtline.git
git push -u origin main
```

## Important: listings are saved per browser

The eight bikes marked "Sample" are made-up examples. On this static version, a bike someone posts is stored only in that visitor's own browser (localStorage), so other visitors will not see it.

To share listings between everyone, the site needs a backend such as Supabase or Firebase to store listings and photos. In `index.html`, `submitListing` and the `db` block near the end of the script are where it would connect.

## About the photos

The six bike photos are embedded inside `index.html` (as `STOCK` near the top of the script), and the sample listings and the ad banner use them. They are example images. Before you publish, replace them with photos you own or have permission to use.

To edit the ad banner text, find the `ADS` list in the last script in `index.html`.

## Files

- `index.html`: the whole site (HTML, CSS and JavaScript)
- `README.md`: this file

Fonts (Bricolage Grotesque, Instrument Sans, DM Mono) load from Google Fonts. Without internet the page falls back to system fonts.
