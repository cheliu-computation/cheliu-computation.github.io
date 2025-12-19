## Academic homepage

This repository contains a simple, single-page academic homepage that you can deploy with GitHub Pages.

### Local preview

```bash
cd /Users/cl522/Documents/homepage
python3 -m http.server 8000
# then open http://localhost:8000 in a browser
```

### How to deploy to GitHub Pages

1. Create a new public repository on GitHub (for example `your-username/your-username.github.io`).  
   If you prefer to keep the code in another repo, you can still publish via Pages—any public repo works.
2. Push this code:
   ```bash
   git init
   git add .
   git commit -m "Add academic homepage"
   git branch -M main
   git remote add origin git@github.com:your-username/your-username.github.io.git
   git push -u origin main
   ```
3. In GitHub: Settings → Pages → Build and deployment → Source: **Deploy from a branch** → Branch: **main** → Folder: **/ (root)** → Save.
4. Your site will be available at `https://your-username.github.io/` within a minute or two.

### Customization tips

- Update content in `index.html` (name, bio, publications, news, links, etc.).
- Replace the placeholder portrait at `assets/img/profile.jpg` (or point to an external image).
- Adjust colors and spacing in `assets/css/style.css`.
- Add PDFs for CV or papers under `assets/files/` and link to them from the page.


