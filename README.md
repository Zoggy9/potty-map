# 🚽 Potty Map

A fun, fully client-side restroom finder built with Leaflet.js and OpenStreetMap. No backend required — runs entirely in your browser.

## Features

- 🗺️ **Real interactive map** — powered by Leaflet + OpenStreetMap, with full zoom and pan
- 📍 **Double-click to add** — drop a pin anywhere on the map to add a new restroom
- ⭐ **Ratings & reviews** — users can leave star ratings and written reviews; average rating updates live
- 🏷️ **Accessibility tags** — mark locations as ADA accessible, free to use, key-required, or outdoors
- 🔍 **Filter sidebar** — filter by star rating or accessibility features
- 💾 **Persistent storage** — all data saved to `localStorage`, survives page refreshes
- 🗑️ **Delete locations** — remove a pin with a confirmation prompt
- 📬 **Address links** — clickable address opens Google Maps

## Getting Started

### Run locally

Just open `index.html` in any modern browser — no build step, no server needed.

```bash
# Optional: serve with a local server
npx serve .
# or
python3 -m http.server
```

### Deploy to GitHub Pages

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)` folder
4. Your map will be live at `https://yourusername.github.io/your-repo-name`

## Project Structure

```
potty-map/
└── index.html     # Everything — HTML, CSS, and JS in one file
└── README.md
```

## Tech Stack

- [Leaflet.js](https://leafletjs.com/) — interactive map
- [OpenStreetMap](https://www.openstreetmap.org/) — map tiles (free, no API key needed)
- [DM Sans + DM Mono](https://fonts.google.com/) — typography via Google Fonts
- `localStorage` — client-side persistence

## Customization

**Change the default map location** — edit the `setView` call in the script:
```js
map = L.map('map', ...).setView([YOUR_LAT, YOUR_LNG], ZOOM_LEVEL);
```

**Add more tags** — extend the `TAG_DEFS` array:
```js
const TAG_DEFS = [
  { id: 'ada', label: '♿ ADA accessible', cls: 'tag-ada' },
  // add your own here
];
```

**Persist to a backend** — replace the `save()` and `loadData()` functions with `fetch()` calls to your API.

## License

MIT — do whatever you want with it.
