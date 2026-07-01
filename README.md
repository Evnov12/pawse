# Pawse 🐾

Your personal dance breakdown studio — import a video, then mirror it, slow it down, and loop any section to learn choreography.

Break down any dance video — slow it down, flip it, and loop the tricky parts until you've got it.

## Features

### Playback
- ▶️ Immersive full-screen player (controls auto-hide while playing, tap to reveal)
- 🔍 Custom scrub handle on the timeline — drag to seek
- 🖥️ CSS pseudo-fullscreen on iOS (keeps mirror transform); native fullscreen on desktop

### Tools
- 🪞 **Mirror** — horizontal flip so you can practice facing a mirror
- 🐢 **Speed control** — 0.5× to 1.5× via a smooth slider
- 🔁 **A–B loop** — drag the A and B handles directly on the timeline to set your in/out points, then tap Loop to repeat that section

### Routines
- 💾 Videos stored locally in IndexedDB — reopen any routine without re-picking the file
- 🖼️ Auto-generated thumbnails (grabbed from the first few seconds of each video)
- 📅 Last-opened date shown per routine, sorted newest first
- ✏️ Rename routines inline
- 🗑️ Delete routines (removes the stored video too)
- 🔗 Re-link flow if the browser clears storage — just pick the file again

### Other
- 🌐 中 / EN language toggle
- ⌨️ Keyboard shortcuts (desktop): `Space` play/pause · `←/→` ±5 s · `M` mirror · `I/O` set in/out · `L` toggle loop
- 📱 Installable as a PWA (Add to Home Screen on iOS/Android)
- 🐶 Animated loading state with progress bar

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
- `icon-*.png` — app icons (180, 192, 512, 512 maskable)

## Note on videos
Videos are stored locally in your browser (IndexedDB), so saved routines open straight to the player — no need to re-pick the file each time. Everything stays on your device; nothing is uploaded. If your browser clears its storage, you'll be asked to re-select the video for that routine.
