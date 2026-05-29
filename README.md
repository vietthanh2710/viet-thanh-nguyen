# Personal Website — GitHub Pages

Static personal site for researchers, with **Publications** in **3 columns** (one per research area), plus **Education** and **Industrial Experience** sections.

## Project structure

```
.
├── index.html          # Main content — edit here
├── css/style.css       # Styles
├── js/main.js          # Mobile menu, footer year
├── assets/
│   └── photo.svg       # Placeholder — replace with photo.jpg
└── README.md
```

## Editing content

1. Open `index.html` and replace placeholders: name, email, bio, ORCID, address.
2. Update **Education** and **Industrial Experience** timeline entries (`<li class="cv-entry">...</li>`).
3. Rename the three **Research Area** column headers under Publications and add papers per column.
4. Profile photo: add `assets/photo.jpg` and update:
   ```html
   <img src="assets/photo.jpg" alt="Your Name" ... />
   ```

## Local preview

```bash
cd /path/to/1.PersonalWebsite
python3 -m http.server 8080
```

Open http://localhost:8080 in your browser.

---

## Deploy free on GitHub Pages

### Step 1: Create a GitHub repository

1. Sign in to [GitHub](https://github.com).
2. **New repository**:
   - **User site** (recommended): repo name `yourusername.github.io` → `https://yourusername.github.io`
   - **Project site**: any name (e.g. `personal-website`) → `https://yourusername.github.io/personal-website/`

### Step 2: Push code

```bash
git init
git add .
git commit -m "Initial personal website"
git branch -M main
git remote add origin https://github.com/yourusername/yourusername.github.io.git
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Repo → **Settings** → **Pages**
2. **Source**: Deploy from a branch
3. **Branch**: `main` / folder **`/ (root)`**
4. **Save** — the site is live in 1–3 minutes.

### Updates

```bash
git add .
git commit -m "Update publications"
git push
```

---

## Tips

- Custom domain: **Settings → Pages → Custom domain**
- Import publications from Google Scholar or BibTeX and paste into each column manually
- Relative paths (`css/`, `js/`, `assets/`) work for both user and project sites

## License

Your site content is yours. Template code is free for personal use.
