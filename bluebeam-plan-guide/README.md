# Bluebeam Plan Guide

An interactive page for customers: a plan finder, CAD pricing comparison, free Bluebeam training links, and a walkthrough for assigning licenses. Prepared by Michael, IMAGINiT Technologies.

## What's in here

| File | What it does |
| --- | --- |
| `public/index.html` | The whole page (HTML, CSS and JavaScript in one file). This is the file you edit. |
| `server.js` | A tiny web server Railway runs. No dependencies. |
| `package.json` | Tells Railway to run `npm start`. |

## Making changes

Everything lives in `public/index.html`. Common edits:

- **Prices:** search for `const PLANS=` near the bottom. Each plan has a `price:` value in CAD.
- **Features per plan:** the `adds:` lists in `PLANS`, and the `MATRIX` list right below it.
- **Plan finder questions:** the `<fieldset class="q">` blocks in the "Plan finder" section, and the matching `REASONS` text in the script.
- **Contact details:** search for `604-551-4181` or `msorgiovanni@rand.com`.
- **Date:** search for `October 5, 2026`.

To preview locally, run `npm start` and open http://localhost:3000 (needs Node 18 or later), or just double-click `public/index.html`.

## Put it on GitHub

1. Create a new repository on github.com (for example `bluebeam-plan-guide`). Leave it empty.
2. In this folder, run:

   ```bash
   git init
   git add .
   git commit -m "Initial Bluebeam plan guide"
   git branch -M main
   git remote add origin https://github.com/<your-account>/bluebeam-plan-guide.git
   git push -u origin main
   ```

   Or use GitHub Desktop: File > Add Local Repository, then Publish.

## Host it on Railway

1. Sign in at railway.com and select **New Project** > **Deploy from GitHub repo**.
2. Pick the `bluebeam-plan-guide` repository. Railway detects Node and runs `npm start` automatically.
3. Open the service, go to **Settings** > **Networking**, and select **Generate Domain** to get a public URL.
4. Optional: add a custom domain in the same place.

Every time you push a change to `main`, Railway redeploys automatically.
