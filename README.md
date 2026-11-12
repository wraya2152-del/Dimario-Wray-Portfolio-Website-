# Infinite Zoom Portfolio Website

A personal website built as an **infinite zoom**: scrolling keeps diving deeper, from the Milky Way into the solar system, into Earth, into the island of Jamaica, into an office workflow, and finally into a screen with frames inside frames that never end.

- **Scroll** (or use the scale ruler on the right, or the menu) to zoom in. Everything on the page grows past you and fades as the next level arrives.
- The worlds hold still: nothing spins or drifts by itself, and dragging does nothing. Only scrolling moves you.
- **Tool names around Earth** open a small interactive demo of each tool. The same demos open from the cards.
- Earth uses real continents, and the Jamaica level uses the real outline of the island (open map data, Natural Earth).
- A dot-grid portrait (a coarse halftone, one round dot per cell) sits beside the name at the start and reacts to your mouse, and a soft light follows your cursor. The loading screen is a galaxy that fills with stars and melts into the real one.
- The whole site uses one fixed palette: ice white, cyan and violet on a deep navy background, so every level feels like part of the same place.
- The page watches its own speed. If a computer struggles, it quietly draws fewer stars and drops fancy effects so scrolling stays smooth.

It is one plain web page. No frameworks, no installs, no build step, and it works offline because everything it needs is in this folder.

## See it

Double-click `index.html`. It opens in your browser (Chrome, Edge, Safari or Firefox).

> It needs WebGL, which every modern browser has. If the 3D worlds do not appear, update your browser.

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
- **Contact email:** search for `window.CONTACT` (and `mailto:` for the link under the form).
- **Project cards:** search for `class="card panel"`. Each card is one project.
- **Browser tab title:** search for `<title>` (and `og:title` for link previews).
- **Demos:** the demo code is near the bottom of `index.html`. Look for `function setwork`, `function inventoria`, `function transcripta` and `function letterforge`.
- **Portrait photo:** the About section holds one photo, stored inside `index.html`. To swap it, ask an AI assistant or a photo tool to cut out the background, save it as a 560 by 700 WebP image, convert it to a base64 data link, and paste it over the `src="data:image/webp...` text inside `<figure class="me">`.
- **Colors:** at the top of the file, find `--cyan`, `--violet` and `--mint`.

## Set up the contact form

The contact section has a message form and a "Copy email" button.

- **Out of the box**, the form opens the visitor's email app with their message filled in. That works with no setup.
- **To receive messages straight to your inbox**, use a free form service such as [Formspree](https://formspree.io):
  1. Create a free account and make a new form. Use your email as the destination.
  2. Copy the form link it gives you (it looks like `https://formspree.io/f/xxxxxxx`).
  3. In `index.html`, search for `window.CONTACT` and paste the link between the quotes after `endpoint:`.
  4. Upload the change. Visitors now see "Message sent" and the message arrives in your inbox.

> **If you reuse this site:** the form and email in this copy belong to its original owner. Replace both (`email` and `endpoint` in the `window.CONTACT` line) with your own before publishing.

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

1. Buy a domain from any registrar (Namecheap, Porkbun, Cloudflare and others).
2. In your host's dashboard (on Vercel: Project, then Settings, then Domains) add the domain.
3. The dashboard shows the DNS records to create, usually one for the main domain and one for `www`. Copy them exactly into your registrar's DNS settings.
4. Wait a few minutes to a few hours. HTTPS turns on automatically.

## Credits and licenses

- Map outlines: [Natural Earth](https://www.naturalearthdata.com), public domain, via the world-atlas package.

- [three.js](https://threejs.org), MIT license (`vendor/LICENSE-three.txt`)
- Space Grotesk and JetBrains Mono fonts, SIL Open Font License (`fonts/LICENSES-fonts.txt`)
