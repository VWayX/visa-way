# Contributing to Visa Way

Thanks for helping! Good first contributions:

- **Fix wrong information**: open an issue with the passport, the destination, what the page shows, and an official source (embassy or government link).
- **Add or improve a translation**: strings live in the `L` and `M` objects at the top of `js/app.js`.
- **Add official links** for a country: see the `LK` object in `js/app.js`.
- **Update the data**: see "Update the visa data" in the README.

## Workflow
1. Fork the repository and create a branch (`git checkout -b fix-turkey-link`).
2. Make a focused change with a clear commit message.
3. Check it locally: `python3 scripts/build_data.py && node --check js/app.js`.
4. Open a pull request describing what changed and why.

## Guidelines
- No tracking or ads inside the core code without discussion.
- Keep the app dependency-light: plain HTML, CSS and JavaScript.
- Always cite an official source for visa information.
