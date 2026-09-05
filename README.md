# Portfolio site — setup guide

## Pages in this site
- `index.html` — Home (name, tagline, social icons at the bottom)
- `about.html` — About
- `portfolio.html` — Portfolio (project list)
- `articles.html` — Articles
- `contact.html` — Contact
- `resume.html` — Resume (embeds `resume.pdf`)
- `project-template.html` — case study template, duplicate this once per real project
- `style.css` — shared styling (dark charcoal palette + top-right horizontal nav)

Every page shares the same fixed top navigation bar — your name on the left, page links on the right. If you add or rename a page, update the `<ul class="topnav-links">` block in all 7 HTML files to keep them in sync.

## 1. Add your resume
Put your actual resume PDF in this same folder and name it exactly `resume.pdf` (or update the `href`/`src` references in `resume.html` and elsewhere to match your filename).

## 2. Fill in your content
Replace in every file:
- `you@email.com`, `yourusername` (GitHub/LinkedIn) — your real links (used in the nav, the home page social icons, and the contact page)
- Placeholder text in `about.html`, `contact.html`, `articles.html`

For `portfolio.html`, update the three project rows with your real project names, tags, and thumbnails.

For each real project, copy `project-template.html` to a new file (e.g. `project-revenue-analysis.html`) and fill in the seven sections with your actual work. Then update the "View case study" links on `portfolio.html` (and the featured project on `index.html`) to point to the new filename instead of `project-template.html`.

## 3. Test locally
Double-click `index.html` to open it in your browser — no server needed. Click through every nav link to check they resolve.

## 4. Deploy to GitHub Pages
1. Create a new repository on GitHub named exactly `yourusername.github.io`.
2. Upload all the files in this folder to the repository root.
   ```
   git init
   git add .
   git commit -m "Portfolio site"
   git branch -M main
   git remote add origin https://github.com/yourusername/yourusername.github.io.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages**, set Source to the `main` branch and `/ (root)`, then save.
4. Your site goes live at `https://yourusername.github.io` within a minute or two.

## Notes
- Replace every `https://via.placeholder.com/...` image with a real screenshot before considering a project page done.
- Keep each project's GitHub repo public with a clear README.
- Once you have real case studies, delete `project-template.html` from what you push live (keep it locally as your template for the next project).
