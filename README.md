# Portfolio — Static template

This folder contains a simple static portfolio template (HTML/CSS) you can open locally or deploy to GitHub Pages.

Main files:
- `index.html` — main page
- `styles.css` — styles
- `projects.json` — project data shown on the site
- `assets/` — put your `profile.jpg` and `CV.pdf` here (see below)

Before opening locally:
1. Place your profile photo at `assets/profile.jpg` (replace the placeholder if needed).
2. Place your CV PDF at `assets/CV.pdf` so the "Download CV" button works.

Opening locally:
- Double-click `index.html` or open it in your browser.

Deployment (GitHub Pages):
1. Initialize a git repository and push to GitHub.
2. On GitHub: go to Settings → Pages, choose branch `main` and folder `/ (root)`.

Deployment (Vercel):
- Import the repository on `vercel.com` for automatic deployments from GitHub.

Editing project content:
- Edit `projects.json` to change descriptions and add `demo` / `code` links.

If you want, I can:
- Add your photo and CV if you provide them here.
- Customize the text (hero lines, project descriptions) from your CV.

---

## Docker & GCP Deployment

### 1. Build and run locally with Docker
```sh
docker build -t my-portfolio .
docker run -p 8080:80 my-portfolio
# Then open http://localhost:8080
```

### 2. Push to GitHub
1. Initialize git if not done:
```sh
git init
git add .
git commit -m "Initial portfolio with Docker"
# Create a repo on GitHub, then:
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

### 3. Deploy on Google Cloud Run
- Connect your GitHub repo to Google Cloud Run (UI or `gcloud` CLI)
- Cloud Run will auto-build the Dockerfile and deploy your static site
- Docs: https://cloud.google.com/run/docs/quickstarts/deploy-container

### 4. (Option) Custom domain & HTTPS
- Configure in GCP Cloud Run settings

---
