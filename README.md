# Boxing Interval Timer

A web app timer for boxing training. Single page, no build step, no dependencies.

**Default workout (15:10 total)**
- 10 s preparation
- 4 rounds of 3 minutes, alternating 10 s sprint / 20 s normal
- 1 minute break between rounds

**Sounds:** a short beep between sprint and normal intervals, a long tone at the start and end of each break, a final signal when the workout is done, and optional 3-2-1 pips at the end of preparation and breaks. Sound starts after you tap Start.

**Settings:** preparation, sprint, normal, round length, break, number of rounds and volume. Values are saved in the browser.

**Keyboard:** Space starts / pauses, R resets.

## Install as an app

The app has a web manifest, icons and a service worker, so it can be installed and works offline after the first visit. It must be served over HTTPS (or localhost) for that.

Free hosting with GitHub Pages: Settings → Pages → "Deploy from a branch" → `main`, `/ (root)`. The timer is then at `https://<user>.github.io/boxing-timer/`.
- Android / desktop Chrome: tap "Install app" or use the browser menu → Install app.
- iPhone (Safari): Share → Add to Home Screen.

To run locally: `python3 -m http.server 8000` and open http://localhost:8000.

## Files
- `index.html` – the whole app (HTML, CSS, JS)
- `manifest.webmanifest`, `sw.js` – install and offline support
- `icon.svg`, `icon-192.png`, `icon-512.png` – app icons
