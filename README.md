# Pre-Flight Pilot Pal (PFPP) v0.1

A Canadian drone pilot's pre-flight companion — a Progressive Web App (PWA)
built to install directly on your phone's home screen with no App Store fees.

## What's in v0.1

- ✅ **ND Filter Recommender** — pick light condition + frame rate + your ND kit, get the right filter
- ✅ **180° Shutter Rule Calculator** — frame rate + shutter angle → exact shutter speed
- ✅ **Aviation-tech UI** — dark cockpit aesthetic, monospace HUD readouts
- ✅ **Installable PWA** — works offline after first load, installs to phone home screen
- ✅ **No accounts, no tracking** — runs entirely in your browser

## Coming in future versions

- Sun / Moon position with golden-hour countdown
- Customizable pre-flight checklist
- White balance cheat sheet
- Pilot credentials & drone registry
- Local weather (Premium)
- Flight suitability score (Premium)
- GPS compass with magnetic declination (Premium)
- Equipment inventory (Premium)
- Scene-type settings suggestions (Premium)
- Composition guides (Premium)
- PDF flight-report export (Premium)

---

## How to test on your phone

### Option A: host for free on GitHub Pages (public URL)

1. Create a free GitHub account if you don't have one.
2. Create a new repository called `pfpp` (or anything you like).
3. Upload the contents of this folder to it.
4. Go to the repo's **Settings → Pages** and enable Pages from the `main` branch.
5. Wait 1-2 minutes. GitHub gives you a URL like `https://yourname.github.io/pfpp/`.
6. Open that URL on your phone.
7. In Safari (iOS) or Chrome (Android), use "Add to Home Screen" from the share menu.
8. You now have Pre-Flight Pilot Pal as an app icon.

### Option B: host for free on Cloudflare Pages (faster, custom domain support)

1. Create a free Cloudflare account.
2. Pages → Create project → connect your GitHub repo.
3. Build settings: leave blank (it's static files).
4. Deploy. Cloudflare gives you a URL.

### Option C: test on the same computer first

1. Open Command Prompt.
2. `cd` into this folder.
3. Run: `python -m http.server 8000`
4. Open `http://localhost:8000` in your browser.
5. For phone testing from your laptop, use your laptop's local IP instead of localhost
   (e.g. `http://192.168.1.50:8000`). Phone must be on the same Wi-Fi.

---

## Adding an access code before public sharing

The app currently has no access code. Before you share the URL with beta testers
who aren't you, ask Claude to add a simple access-code gate so random URL-finders
can't use it without the code.

---

## File layout

```
pfpp/
├── index.html           Main app (HTML + CSS + JS in one file)
├── manifest.webmanifest PWA manifest (tells phones this is installable)
├── sw.js                Service worker (offline support)
└── README.md            This file
```

Everything is in one HTML file for simplicity. When the project grows, we can
split it into modules — but for v0.1, single-file is the right call.
