# Sustainable Mulki: interactive 3D city plan

A static website. No build step, no server, no dependencies: everything (3D engine included) is inside `index.html`.

Files
- `index.html`: the whole app
- `favicon.svg`: browser tab icon
- `og.png`: preview image shown when the link is shared (WhatsApp, LinkedIn, X)
- `.nojekyll`: lets GitHub Pages serve the files as they are

## Host it (pick one, all free)

**Netlify (fastest, about 30 seconds)**
1. Go to app.netlify.com/drop
2. Drag the `mulki-site` folder onto the page
3. You get a link like `https://something.netlify.app`. Rename it in Site settings.

**GitHub Pages**
1. Create a new public repository and upload these four files to the root
2. Settings, then Pages, then Source: "Deploy from a branch", branch `main`, folder `/ (root)`
3. Your site appears at `https://<username>.github.io/<repo>/`

**Vercel / Cloudflare Pages**
Import the folder or repository. Framework preset: "Other", no build command, output directory `.`

## After hosting
- Link previews: in `index.html`, change `content="og.png"` (the `og:image` tag) to the full address, for example `https://yoursite.netlify.app/og.png`. Some platforms ignore relative image paths.
- Custom domain: add it in the host's domain settings. HTTPS is automatic.
- To change numbers or text, edit the `SITES` data inside `index.html` (search for `Rooftop solar homes`), or ask Claude to rebuild it.

## Notes
- Needs a browser with WebGL (any current Chrome, Edge, Firefox or Safari). Others see a clear message instead.
- Works on phones; the detail panel moves to the bottom of the screen.
- File size is about 700 KB, so it loads quickly.
