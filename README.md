# Visa Way ✈️

![CI](https://github.com/YOUR_USERNAME/visa-way/actions/workflows/ci.yml/badge.svg)
![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)

**Visa requirements for 199 passports on an interactive 3D globe.**
Pick your passport and a destination to see the visa type, required documents, rules to respect, study and work guidance, and where to apply. Works in Arabic (RTL), French, English and Spanish.

**Live demo:** https://YOUR_USERNAME.github.io/visa-way/

<!-- Add a screenshot: save it as docs/screenshot.png and uncomment the next line -->
<!-- ![Visa Way screenshot](docs/screenshot.png) -->

## Features
- 🌍 3D globe with real country shapes, coloured by requirement (🟢 visa-free, 🟡 e-visa or visa on arrival, 🔴 visa required). Drag to rotate, tap a country to select it.
- 🛂 199 passports × 199 destinations, with the real number of visa-free days.
- 🔎 "Where can I go?" filters with live counts, plus a country search in every language.
- 🎓 Tabs for **students**, **work** and **laws**, with official portals and search links.
- 🌐 4 languages, mobile first, light and dark friendly.
- Zero build step: plain HTML, CSS and JavaScript.

## Run locally
```bash
git clone https://github.com/YOUR_USERNAME/visa-way.git
cd visa-way
python3 -m http.server 8000   # then open http://localhost:8000
```

## Project structure
```
index.html          page markup
css/style.css       styles
js/app.js           application logic
js/data.js          generated visa data (do not edit by hand)
data/               source CSV (Passport Index)
scripts/build_data.py   CSV -> js/data.js
.github/workflows/ci.yml   data + syntax checks on every push
```

## Update the visa data
1. Replace `data/passport-index-matrix-iso2.csv` with a newer matrix.
2. Run `python3 scripts/build_data.py`.
3. Commit `data/` and `js/data.js`. CI fails if `js/data.js` is out of date.

## Data and credits
Visa requirements come from the [Passport Index dataset](https://github.com/ilyankou/passport-index-dataset) (MIT license, data up to January 2025). World shapes come from [datamaps](https://github.com/markmarkoh/datamaps); 3D with [three.js](https://threejs.org). Libraries load from cdnjs.

> ⚠️ Visa rules change often and depend on individual circumstances. Always confirm with the official embassy or government website before applying.

## Roadmap
- [ ] More recent data and a visible "last updated" date per passport
- [ ] Visa fees and processing times
- [ ] One page per country (SEO) and a shareable URL for each passport and destination
- [ ] Installable PWA with offline support
- [ ] Higher-resolution borders and small islands
- [ ] Interactive document checklist (tick, save, print)
- [ ] Translations: Darija, Portuguese, German

## Contributing
Ideas, bug reports and pull requests are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License
[MIT](LICENSE)
