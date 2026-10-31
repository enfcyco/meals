# GitHub Copilot Instructions for Meals

## Repository conventions
- Keep `meals.txt`, `sides.txt`, and `suggestions.txt` as simple, readable plain-text lists. Preserve their existing format and backward compatibility.
- The recipe site is static HTML and CSS. Follow the existing patterns in `index.html`, `recipes/`, and `styles.css`; do not add build tools or dependencies.

## Adding recipes from scans
- Create one individual page under `recipes/` for each distinct recipe the user provides, using the existing recipe-page structure, and add a recipe card linking to each page in `index.html`.
- Preserve original source links when provided, and transcribe visible ingredient amounts and timings accurately. Preserve each legible handwritten note as a meaningful family preference at the relevant ingredient or step, clearly marked as a note, asterisk, or modification; keep it separate from the original recipe text. Label unclear handwriting as uncertain instead of guessing, and clearly identify other unreadable or absent information. Never invent missing directions.
- Write directions in concise original phrasing rather than reproducing long source text verbatim.
- Do not make unrelated list changes, such as adding a meal that is already listed. Do not add a scanner app or OCR tooling unless explicitly requested.

## Validation
- Check that local links resolve and run `git diff --check` before completing changes.
