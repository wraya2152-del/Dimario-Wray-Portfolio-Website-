# Tech Earth Website

A personal website that is mostly a **nice graphic experience**: a glowing, spinning "tech Earth" with moving words around it.

- **Drag** to spin the Earth.
- **Scroll** and the Earth zooms and travels while the words slide and lean with you.
- When the page opens, a little rocket lands each letter of the name. (Visitors who have "reduce motion" switched on in their device settings skip this. The **Replay intro** link in the footer plays it on request.)
- Each project card has a **See it work** button that opens a small interactive demo of the tool, running on sample data.
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
- **Contact email:** search for `window.CONTACT` (and `mailto:` for the link under the form).
- **Project cards:** search for `class="card panel"`. Each card is one project.
- **Browser tab title:** search for `<title>` (and `og:title` for link previews).
- **Demos:** the demo code is near the bottom of `index.html`. Look for `function setwork`, `function inventoria`, `function transcripta` and `function letterforge`.
- **Colors:** at the top of the file, find `--cyan`, `--violet` and `--mint`.

## Set up the contact form

The contact section has a message form and a "Copy email" button.

- **Out of the box**, the form opens the visitor's email app with their message filled in. That works with no setup.
- **To receive messages straight to your inbox**, use a free form service such as [Formspree](https://formspree.io):
  1. Create a free account and make a new form. Use your email as the destination.
  2. Copy the form link it gives you (it looks like `https://formspree.io/f/xxxxxxx`).
  3. In `index.html`, search for `window.CONTACT` and paste the link between the quotes after `endpoint:`.
  4. Upload the change. Visitors now see "Message sent" and the message arrives in your inbox.

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

- [three.js](https://threejs.org), MIT license (`vendor/LICENSE-three.txt`)
- Space Grotesk and JetBrains Mono fonts, SIL Open Font License (`fonts/LICENSES-fonts.txt`)
