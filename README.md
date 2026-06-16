# Pawse 🐾

Your personal dance breakdown studio — import a video, then mirror it, slow it down, and loop any section to learn choreography.

舞蹈练习台 —— 导入视频，镜像、变速、循环任意片段，轻松扒舞。

## Features
- 🪞 Horizontal mirror (practice facing a mirror)
- 🐢 Speed control (0.5× – 1.25×)
- 🔁 Loop any section (set in/out points)
- 🌐 中 / EN language toggle
- 📱 Installable as a PWA (Add to Home Screen)
- 💾 Saved routines list (names persist across sessions)

---

## Deploy — Option A: Netlify Drop (fastest)

1. Open https://app.netlify.com/drop in a desktop browser
2. Drag this **entire `pawse` folder** into the drop zone
3. Wait a few seconds → you get a live link like `your-app.netlify.app`
4. Open that link on your iPhone → tap Share → **Add to Home Screen**

> Tip: To keep the site permanently, sign up for a free Netlify account (you can claim the site you just dropped).

## Deploy — Option B: GitHub + Vercel

1. Create a new repo on GitHub (e.g. `pawse`)
2. Upload all files in this folder to the repo
3. Go to https://vercel.com → New Project → import your repo
4. Framework preset: **Other** (no build step needed)
5. Deploy → you get `pawse.vercel.app`
6. Open on iPhone → Share → **Add to Home Screen**

Every time you push changes to GitHub, Vercel redeploys automatically.

---

## Files
- `index.html` — the whole app (HTML + CSS + JS in one file)
- `manifest.json` — PWA config (name, icons, colors)
- `sw.js` — service worker (offline caching)
- `icon-*.png` — app icons
- `make_icons.py` — script that generated the icons (not needed for deploy)

## Note on videos
Videos are stored locally in your browser (IndexedDB), so saved routines open straight to the player — no need to re-pick the file each time. Everything stays on your device; nothing is uploaded. If your browser clears its storage, you'll be asked to re-select the video for that routine.
