# Dimario Wray — Tech Earth Portfolio

A single-page, static website (no build step). Open `index.html` in a browser to preview it.

## Put it on GitHub
```bash
cd dimario-wray-portfolio-site
git init
git add .
git commit -m "Initial commit: tech Earth portfolio"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/dimario-wray-portfolio.git
git push -u origin main
```

## Host it free (pick one)
- **Vercel / Netlify:** import the GitHub repo. Framework: "Other". Build command: none. Output directory: `.` (root).
- **GitHub Pages:** repo Settings > Pages > Deploy from branch > `main` / root.

## Custom domain
Add the domain in your host's dashboard, then create the DNS records it shows you at your registrar.
Wait for DNS to propagate (minutes to a few hours) and HTTPS turns on automatically.
