# Zach Gause — tap card

A static, single-page digital business card. No build step.

```
public/index.html    the card (photo and QR generator are embedded)
public/favicon.svg   browser-tab icon
vercel.json          serves /public, adds security headers
```

## Deploy on Vercel

**Option A — GitHub (recommended, auto-redeploys on every push)**
1. Create a new GitHub repo and upload the contents of this folder (keep `public/` and `vercel.json` at the repo root).
2. In Vercel: Add New → Project → Import that repo.
3. Framework Preset: **Other**. Leave Build Command empty. Deploy.

**Option B — Vercel CLI**
```
cd zach-tap-card
npx vercel          # preview deploy
npx vercel --prod   # production
```

## Editing
Contact details live in the `CONFIG` block near the bottom of `public/index.html`.
Accent color: `--accent` plus the three `rgba()` values beside it at the top of the styles.

## After deploying
- Program your NFC tag / print your QR with the production URL (or a custom domain).
- The on-page "QR code" button always encodes whatever URL the page is served from.
