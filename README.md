# Leonard Law — Portfolio Website

A personal portfolio site built with plain HTML, CSS, and JavaScript.
Hosted for free on GitHub Pages. No build tools or npm required.

---

## File Structure

```
portfolio/
├── index.html              ← Main page (all sections: About, Projects, Blog, Contact)
├── blog/
│   ├── post-template.html  ← Copy this to create a new blog post
│   └── post-1.html         ← First blog post
├── assets/
│   ├── css/style.css       ← All styling
│   ├── js/main.js          ← Mobile nav + scroll behaviour
│   └── images/
│       └── profile-placeholder.svg  ← Replace with your real photo
└── README.md               ← This file
```

---

## How to Update the Site

### Add a New Blog Post

1. Open the `blog/` folder
2. Copy `post-template.html` and rename it — e.g. `post-2.html`
3. Open the new file and update every section marked `<!-- EDIT -->`
   - Page title and meta description (in `<head>`)
   - Post title (`<h1>`)
   - Date — both the `datetime="YYYY-MM-DD"` attribute and the displayed text
   - Reading time estimate
   - Post body content
4. Open `index.html` and find the **Blog** section
5. Copy one of the existing `<article class="card blog-card">` blocks
6. Paste it at the top of the `.blog-grid` div
7. Update the title, date, excerpt, and both `href` links to point to your new file (e.g. `blog/post-2.html`)
8. Delete or update one of the "Coming soon" placeholder cards if needed
9. Save both files and deploy (see Deploying below)

---

### Add a New Project Card

1. Open `index.html` and find the **Projects** section (`<section id="projects">`)
2. Find the `<div class="projects-grid">` block
3. Copy one of the existing `<article class="card">` blocks
4. Update:
   - `<h3 class="card-title">` — project name
   - `<p class="card-description">` — what it does
   - `<span class="tag">` — relevant technology tags
   - `<a href="#">` — link to your project (GitHub, demo, etc.)
5. Save and deploy

---

### Update Your About Me Text

1. Open `index.html`
2. Find `<section id="about">`
3. Edit the three `<p>` paragraphs inside `.about-bio`
4. Save and deploy

---

### Replace Your Profile Photo

1. Prepare your photo: square crop, at least 500×500px
2. Save it as `assets/images/profile.jpg` (use lowercase, no spaces)
3. Open `index.html` and find the `<img>` tag inside `.about-photo`
4. Change `src="assets/images/profile-placeholder.svg"` to `src="assets/images/profile.jpg"`
5. Save and deploy

---

### Deploy to GitHub Pages

After making any changes, run these three commands in your terminal from the `portfolio/` folder:

```bash
git add .
git commit -m "Brief description of what you changed"
git push
```

Your site will update within 1–2 minutes at `https://leonard-law.github.io`.

---

## First-Time GitHub Pages Setup

If you haven't set up GitHub Pages yet:

1. Create a new GitHub repository named exactly: `leonard-law.github.io`
2. In the `portfolio/` folder, run:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio site"
   git remote add origin https://github.com/leonard-law/leonard-law.github.io.git
   git push -u origin main
   ```
3. Go to your repo on GitHub → **Settings** → **Pages**
4. Under **Source**, select: `Deploy from a branch` → Branch: `main` → Folder: `/ (root)` → **Save**
5. Your site will be live at `https://leonard-law.github.io` within a few minutes

---

## Tips

- **All file names must be lowercase** — GitHub Pages runs on Linux, which is case-sensitive. `Style.css` and `style.css` are different files.
- **Test locally first** — open `index.html` in your browser before pushing. If images and styles load locally, they'll load on GitHub Pages.
- **Blog post numbering** — keep incrementing: `post-2.html`, `post-3.html`, etc. Don't reuse numbers.
- **Updating the footer year** — the footer in `index.html` and both blog HTML files includes `© 2026`. Update this each January.
