# Nainar Shanmuganathan for CTS Vice President — Campaign Site

A simple two-page static site: `index.html` (Home) and `about.html` (About).

## Adding your photos and logo

Every placeholder box on the site (the dashed-border blocks that say things like
"Add a volunteering photo here") is meant to be swapped for a real `<img>` tag.

1. Add your image files to the `images/` folder (e.g. `images/hero.jpg`, `images/logo.png`).
2. Open `index.html` or `about.html` in a text editor and find the matching HTML comment,
   e.g.:
   ```html
   <!-- Replace this placeholder with <img src="images/hero.jpg" alt="Nainar Shanmuganathan volunteering"> -->
   <div class="photo-frame">
     <span class="placeholder-label">Add a volunteering photo here (portrait, roughly 4:5)</span>
   </div>
   ```
3. Replace the whole `<div class="photo-frame">...</div>` block with:
   ```html
   <div class="photo-frame">
     <img src="images/hero.jpg" alt="Nainar Shanmuganathan volunteering" style="width:100%;height:100%;object-fit:cover;">
   </div>
   ```
   Keep the outer `photo-frame` div — it controls the shape/border — just put your `<img>` inside it.

The logo works the same way: replace `<div class="nav-logo">LOGO</div>` (it appears in the
nav and footer of both pages) with `<img src="images/logo.png" alt="CTS logo" class="nav-logo">`.

## Adding your contact info

Search for `[add email here]` and `[add phone here]` in the footer of both pages and replace
with your real contact details (or a form link, if you set one up later).

## Deploying to GitHub Pages

1. **Create a GitHub account** if you don't have one: https://github.com/join

2. **Create a new repository**
   - Click the "+" in the top right of GitHub → "New repository"
   - Name it something like `nainar-for-vp` (this becomes part of your site's URL)
   - Set it to **Public**
   - Don't add a README, .gitignore, or license (we already have files)
   - Click "Create repository"

3. **Upload your files**
   - On the new repo's page, click "uploading an existing file"
   - Drag in all files and folders from this project: `index.html`, `about.html`,
     `css/`, `js/`, `images/`
   - Scroll down and click "Commit changes"

   (If you're comfortable with git/command line instead, you can do:
   ```bash
   git init
   git add .
   git commit -m "Initial campaign site"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/nainar-for-vp.git
   git push -u origin main
   ```
   )

4. **Enable GitHub Pages**
   - In your repo, go to **Settings** → **Pages** (left sidebar)
   - Under "Build and deployment" → "Source", select **Deploy from a branch**
   - Under "Branch", select **main** and folder **/ (root)**, then click **Save**

5. **Get your live URL**
   - Wait 1–2 minutes, then refresh the Settings → Pages screen
   - Your site will be live at:
     `https://YOUR-USERNAME.github.io/nainar-for-vp/`

6. **Making updates later**
   - Edit files locally and re-upload via "Add file" → "Upload files" on GitHub
     (or `git add . && git commit -m "update" && git push` if using git)
   - GitHub Pages automatically redeploys within a minute or two of any push to `main`

## File structure

```
.
├── index.html          Home page
├── about.html           About page
├── css/
│   └── styles.css       All site styling
├── js/
│   └── main.js           Mobile nav toggle
└── images/               Add your photos and logo here
```
