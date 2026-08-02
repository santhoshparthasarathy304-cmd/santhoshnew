# Santhosh P. — Portfolio

Single-file static site (`index.html`). No backend, no database, no build step.

## 1. Before you deploy

Open `index.html`, search for `CHANGE THIS PASSWORD`, and set your own admin
password (currently `Santhosh@2026`). This is a client-side password only —
fine for keeping casual visitors out of edit mode, not bank-grade security,
since anyone can view the page source.

## 2. Deploy

**GitHub Pages**
1. Create a repo (e.g. `portfolio`) and push these files to it.
2. Repo → Settings → Pages → Source: `main` branch, `/ (root)`.
3. Live at: `https://your-username.github.io/portfolio/`

**Netlify**
1. Drag the project folder into Netlify's "Deploy manually" panel, or connect the GitHub repo.
2. The included `_headers` file is picked up automatically.
3. Live at: `https://your-site-name.netlify.app/`

**Vercel**
1. Import the folder/repo in the Vercel dashboard (framework preset: "Other").
2. The included `vercel.json` is picked up automatically.
3. Live at: `https://your-site-name.vercel.app/`

## 3. How editing works

- Log in via the small **Admin Login** link in the footer.
- Edit content, upload images, click each Save button — you'll see "Changes Saved Successfully".
- These saves write to *your current browser's* local storage only (this is what "no backend" means in practice — there's nowhere else for a static site to write to).

## 4. Publishing your edits so every visitor sees them — read this part

This is the one requirement worth being upfront about, because two things you
asked for pull in opposite directions: **"no backend server"** and
**"every visitor on every device always sees my latest saved edits
automatically."** A pure static site (GitHub Pages / Netlify / Vercel with no
server) has no shared database, so there's no way for an edit made in your
browser to teleport into a stranger's phone by itself. Any tool that claimed
to do that without a backend would be lying to you.

What **is** solved, and what this file already does:

- **Stale-cache problem** — fixed. The added `Cache-Control: no-cache` meta
  tags and the `_headers` / `vercel.json` files stop browsers and CDNs from
  serving an old cached copy once you *have* redeployed a new version.
  (GitHub Pages doesn't support custom response headers at all — this part
  only applies on Netlify/Vercel. On GitHub Pages, a hard refresh, or simply
  waiting a few minutes for their CDN to expire, resolves it.)
- **Getting your edits live for everyone** — this is the part that needs one
  manual step, and it's already built into the Admin Toolbar:
  1. Log in as Admin and make all your edits.
  2. Click **Download Updated File** in the admin toolbar. This bakes
     everything you saved into a fresh `index.html` with your edits as the
     new defaults for anyone who opens the site.
  3. Replace `index.html` in your repo/hosting with that downloaded file and
     redeploy (commit + push for GitHub Pages; drag-and-drop or `git push`
     for Netlify/Vercel).
  4. Now every visitor, on every device, sees the update — because it's
     baked into the file itself, not sitting in your browser's storage.

Use **Export Backup (JSON)** any time as a safety copy of your content, and
**Import Data** to restore it into a browser if needed.

## 5. What's included

- `index.html` — the site
- `_headers` — Netlify cache-control rule
- # Santhosh P. — Portfolio

Single-file static site (`index.html`). No backend, no database, no build step.

## 1. Before you deploy

Open `index.html`, search for `CHANGE THIS PASSWORD`, and set your own admin
password (currently `Santhosh@2026`). This is a client-side password only —
fine for keeping casual visitors out of edit mode, not bank-grade security,
since anyone can view the page source.

## 2. Deploy

**GitHub Pages**
1. Create a repo (e.g. `portfolio`) and push these files to it.
2. Repo → Settings → Pages → Source: `main` branch, `/ (root)`.
3. Live at: `https://your-username.github.io/portfolio/`

**Netlify**
1. Drag the project folder into Netlify's "Deploy manually" panel, or connect the GitHub repo.
2. The included `_headers` file is picked up automatically.
3. Live at: `https://your-site-name.netlify.app/`

**Vercel**
1. Import the folder/repo in the Vercel dashboard (framework preset: "Other").
2. The included `vercel.json` is picked up automatically.
3. Live at: `https://your-site-name.vercel.app/`

## 3. How editing works

- Log in via the small **Admin Login** link in the footer.
- Edit content, upload images, click each Save button — you'll see "Changes Saved Successfully".
- These saves write to *your current browser's* local storage only (this is what "no backend" means in practice — there's nowhere else for a static site to write to).

## 4. Publishing your edits so every visitor sees them — read this part

This is the one requirement worth being upfront about, because two things you
asked for pull in opposite directions: **"no backend server"** and
**"every visitor on every device always sees my latest saved edits
automatically."** A pure static site (GitHub Pages / Netlify / Vercel with no
server) has no shared database, so there's no way for an edit made in your
browser to teleport into a stranger's phone by itself. Any tool that claimed
to do that without a backend would be lying to you.

What **is** solved, and what this file already does:

- **Stale-cache problem** — fixed. The added `Cache-Control: no-cache` meta
  tags and the `_headers` / `vercel.json` files stop browsers and CDNs from
  serving an old cached copy once you *have* redeployed a new version.
  (GitHub Pages doesn't support custom response headers at all — this part
  only applies on Netlify/Vercel. On GitHub Pages, a hard refresh, or simply
  waiting a few minutes for their CDN to expire, resolves it.)
- **Getting your edits live for everyone** — this is the part that needs one
  manual step, and it's already built into the Admin Toolbar:
  1. Log in as Admin and make all your edits.
  2. Click **Download Updated File** in the admin toolbar. This bakes
     everything you saved into a fresh `index.html` with your edits as the
     new defaults for anyone who opens the site.
  3. Replace `index.html` in your repo/hosting with that downloaded file and
     redeploy (commit + push for GitHub Pages; drag-and-drop or `git push`
     for Netlify/Vercel).
  4. Now every visitor, on every device, sees the update — because it's
     baked into the file itself, not sitting in your browser's storage.

Use **Export Backup (JSON)** any time as a safety copy of your content, and
**Import Data** to restore it into a browser if needed.

## 5. What's included

- `index.html` — the site
- `_headers` — Netlify cache-control rule
- `vercel.json` — Vercel cache-control rule
- `README.md` — this file

- `vercel.json` — Vercel cache-control rule
- `README.md` — this file
