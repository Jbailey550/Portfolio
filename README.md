# Portfolio — GitHub Upload Guide

No terminal, no npm, no build steps needed. Just upload files.

---

## Your files

```
portfolio/
├── index.html          ← Homepage
├── cases.html          ← Case studies list
├── resume.html         ← Résumé
├── contact.html        ← Contact page
├── style.css           ← All colours/fonts (edit to retheme)
└── cases/
    ├── fintech-onboarding.html    ← Case study 1
    ├── analytics-dashboard.html  ← Case study 2
    └── design-system.html        ← Case study 3
```

---

## How to upload to GitHub (first time)

1. Go to **github.com** and sign in
2. Click the **+** icon → **New repository**
3. Name it `portfolio`, set it to **Public**, click **Create repository**
4. On the next screen click **uploading an existing file**
5. Drag ALL your files and folders into the upload area
6. Click **Commit changes**

That's it — your files are on GitHub.

---

## How to turn on GitHub Pages (free hosting)

1. In your repo, click **Settings**
2. Click **Pages** in the left sidebar
3. Under "Source" select **Deploy from a branch**
4. Select branch: **main**, folder: **/ (root)**
5. Click **Save**

Your site will be live at:
`https://YOURUSERNAME.github.io/portfolio`

Takes about 1–2 minutes to go live the first time.

---

## How to connect your custom domain

1. In GitHub Pages settings, type your domain in the "Custom domain" box
2. GitHub will show you DNS records to add
3. Log into your domain registrar (GoDaddy, Namecheap, etc.)
4. Add the DNS records GitHub gives you
5. Wait 10–30 minutes — your domain will point to your portfolio

---

## How to edit content (day-to-day)

**To edit any page:**
1. Go to your repo on github.com
2. Click the file you want to edit (e.g. `index.html`)
3. Click the **pencil ✏️ icon** (top right of the file view)
4. Make your changes — all editable text is marked with `<!-- EDIT -->`
5. Click **Commit changes** → **Commit directly to main**

Your site updates in about 30 seconds.

---

## How to add a new case study

1. In your repo, go into the `cases/` folder
2. Open `fintech-onboarding.html`, click the pencil to edit
3. Select all the text (Ctrl+A), copy it
4. Go back to `cases/`, click **Add file → Create new file**
5. Name it `my-new-project.html`
6. Paste in the content and edit everything marked `<!-- EDIT -->`
7. Add a link to it in `cases.html` by copying one of the `.case-row` blocks

---

## How to add your photo

1. In your repo, click **Add file → Upload files**
2. Create an `images/` folder by typing `images/` before your filename
3. Upload your photo (e.g. `images/photo.jpg`)
4. In `index.html`, find the comment that says:
   ```
   <!-- <img src="images/photo.jpg" ... /> -->
   ```
5. Remove the `<!--` and `-->` to uncomment it
6. Delete the `<div class="photo-placeholder">` block above it

---

## How to make the contact form work (free)

1. Sign up at **formspree.io** (free plan = 50 submissions/month)
2. Click **New Form**, give it a name
3. Copy your Form ID (looks like `xabcdefg`)
4. Edit `contact.html`, find:
   ```
   action="https://formspree.io/f/YOUR_FORM_ID"
   ```
5. Replace `YOUR_FORM_ID` with your actual ID

---

## Changing colours / fonts

Open `style.css` and edit the `:root` block at the top:

```css
:root {
  --bg:     #0d0d0d;   /* page background */
  --accent: #c8b89a;   /* gold highlight colour */
  --text:   #f0ede8;   /* main text */
  ...
}
```

Changing `--accent` will update every highlight across the whole site.
