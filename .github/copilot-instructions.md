# GitHub Copilot Instructions for Meals

## Repository conventions
- Keep `meals.txt`, `sides.txt`, and `suggestions.txt` as simple, readable plain-text lists. Preserve their existing format and backward compatibility.
- The recipe site is static HTML and CSS. Follow the existing patterns in `index.html`, `recipes/`, and `styles.css`; do not add build tools or dependencies.

## Adding recipes from scans
- Create one individual page under `recipes/` for each distinct recipe the user provides, using the existing recipe-page structure, and add a recipe card linking to each page in `index.html`.
- Preserve original source links when provided. Transcribe visible ingredient amounts, timings, and handwritten notes accurately. Clearly identify information that is unreadable or absent; never invent missing directions.
- Write directions in concise original phrasing rather than reproducing long source text verbatim.
- Do not make unrelated list changes, such as adding a meal that is already listed. Do not add a scanner app or OCR tooling unless explicitly requested.

## Validation
- Check that local links resolve and run `git diff --check` before completing changes.
