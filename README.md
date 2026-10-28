# Tech Earth Website

A personal website that is mostly a **nice graphic experience**: a glowing, spinning "tech Earth" with moving words around it.

- **Drag** to spin the Earth.
- **Scroll** and the Earth zooms and travels while the words slide and lean with you.
- A short loading screen plays when the page first opens.

It is one plain web page. No frameworks, no installs, no build step, and it works offline because everything it needs is in this folder.

## See it

Double-click `index.html`. It opens in your browser (Chrome, Edge, Safari or Firefox).

> It needs WebGL, which every modern browser has. If the Earth does not appear, update your browser.

## What's in the folder

| File / folder | What it is |
|---|---|
| `index.html` | The whole website: the words, the design and the animation |
| `vendor/` | The 3D library (three.js) that draws the Earth |
| `fonts/` | The two fonts the site uses |

## Make it yours

Open `index.html` in any text editor and search for the words you want to change (your name, the project cards, the email address). Save, refresh the browser, done.

Easy things to change:
- **Your name:** search for `Dimario` and `Wray`.
- **Contact email:** search for `mailto:`.
- **Project cards:** search for `class="card panel"`. Each card is one project.
- **Colors:** at the top of the file, find `--cyan`, `--violet` and `--mint`.

## Put it online for free

**1. Put it on GitHub**

1. Make a free account at github.com and create a new empty repository.
2. Click **Add file → Upload files**, drag in everything from this folder (keep the `vendor` and `fonts` folders), and click **Commit changes**.

If you prefer the terminal:

```bash
git init
git add .
git commit -m "First version"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git push -u origin main
```

**2. Host it (pick one, all free)**

- **Vercel or Netlify:** sign in with GitHub, import the repository, leave the build command empty, and deploy.
- **GitHub Pages:** in the repository go to **Settings → Pages**, choose the `main` branch and the root folder, and save.

You get a live link within a minute or two.

**3. Use your own domain (optional)**

Buy a domain from any registrar, add it in your host's dashboard, then copy the DNS records the dashboard shows into your registrar's DNS settings. HTTPS turns on automatically after a short wait.

## Credits and licenses

- [three.js](https://threejs.org), MIT license (`vendor/LICENSE-three.txt`)
- Space Grotesk and JetBrains Mono fonts, SIL Open Font License (`fonts/LICENSES-fonts.txt`)
