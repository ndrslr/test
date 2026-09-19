# Your academic website

A simple, self-contained site: `index.html` + `style.css`. No build step —
GitHub Pages will serve it as-is.

## 1. Fill in your content

Open `index.html` in any text editor (or GitHub's web editor) and replace
every `[bracketed placeholder]` — name, department, links, bio, papers, CV
highlights. I've highlighted editable placeholder text with a light
yellow background so it's easy to scan for; that's just a CSS class
(`editme`) and won't show once you replace the text and it no longer
matches that pattern — or you can just delete the `class="editme"` bits
once you're done.

Add your actual CV as `cv.pdf` in this same folder — the "Download CV"
button already points to `cv.pdf`.

**Photos & logos (optional):** the page has spots wired up for:

- `photo.jpg` — your portrait, shown in a circle in the header. Until you
  add one, it falls back to showing your initials, so nothing looks broken.
- `penn-logo.png` and `vt-logo.png` — small icons next to your degrees in
  the timeline.
- `left-01.jpg` through `left-08.jpg` — 8 photos running down the left
  margin, outside the text column, slightly rotated like photos pinned to
  a corkboard.
- `right-01.svg` through `right-08.svg` — 8 diagrams running down the
  right margin: cylinder, pair-of-pants, one-handle, two-handle bordisms,
  then tree-level, one-loop, two-loop, and open-string worldsheet
  diagrams. These are already included — compiled straight from your
  TikZ code, recolored to the site's ink-gray, transparent background,
  no border, so they read as part of the page rather than as inserted
  images. If you'd rather have photos here too, just replace them with
  `.jpg` files of the same name (update the `src` in `index.html` from
  `.svg` to `.jpg` for that slot).
- `topic-bordism.jpg` and `topic-symmetry.jpg` — two small square images
  next to the "Bordisms, TQFTs & the Swampland" and "Generalized
  symmetries in SCFTs" entries under Research Interests.

Portrait and left-rail images work best roughly 4:5 (portrait aspect),
since they're cropped to that shape automatically. The right-rail SVGs
size themselves automatically — no cropping needed.

Just drop image files with those exact names into the same folder as
`index.html` and they'll appear automatically — no code changes needed.
If a file is missing, that spot just quietly disappears rather than
showing a broken image icon.

**A note on the margin images:** they're hidden below roughly 1240px of
browser width, since there isn't room for three columns below that — so
on laptops with a narrower window, or on phones/tablets, only the center
column shows. This is intentional (nothing looks broken), but it does
mean most visitors on mobile won't see them.

## 2. Get it online with GitHub Pages (free)

**Option A — personal site at `yourusername.github.io`:**
1. Create a new GitHub repo named exactly `yourusername.github.io`
   (replace with your actual GitHub username).
2. Upload `index.html`, `style.css`, and `cv.pdf` to the repo root
   (drag-and-drop works on github.com, or `git push`).
3. Go to **Settings → Pages**. It should auto-detect and deploy from the
   `main` branch, root folder.
4. Your site is live at `https://yourusername.github.io` within a
   minute or two.

**Option B — project site (any repo name), e.g. for a subpage:**
1. Create/use any repo, e.g. `physics-site`.
2. Upload the same files to the repo root.
3. Go to **Settings → Pages**, set source to the `main` branch.
4. Your site is live at `https://yourusername.github.io/physics-site`.

Either way, this is a real, permanent web address you can put on
applications, in email signatures, and on your CV itself — free, and
you can swap in a custom domain later (Settings → Pages → Custom domain)
if your university or department offers one, or if you buy one later.

## 3. Updating it later

Any time you edit `index.html` (new paper, new talk, updated bio) and
push to the same repo, GitHub Pages redeploys automatically within a
minute — no separate "publish" step.

## Notes

- Fonts (Spectral, IBM Plex Sans/Mono) load from Google Fonts via the
  `<link>` tags in the `<head>` — no local font files needed.
- The faint equation behind your name in the header is the Polyakov
  action, a foundational equation in string theory — swap it for
  something more personal to your subfield if you like (it's just text
  in the `.hero-equation` div in `index.html`).
- The site has no analytics, tracking, or external dependencies beyond
  Google Fonts, so it's fast and privacy-friendly by default.
