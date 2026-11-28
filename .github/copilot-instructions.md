# GitHub Copilot Instructions for Meals

## Repository conventions
- Keep `meals.txt`, `sides.txt`, and `suggestions.txt` as simple, readable plain-text lists. Preserve their existing format and backward compatibility.
- The recipe site is static HTML and CSS. Follow the existing patterns in `index.html`, `recipes/`, and `styles.css`; do not add build tools or dependencies.

## Pull requests
- Create every pull request for work in this repository as a Draft PR by default, including when the user asks to create or open a PR. Only create a ready-for-review PR when the user explicitly requests one, and do not mark a draft ready or otherwise convert it out of draft unless the user explicitly asks.
- Draft status lets the user review changes in the GitHub browser UI before approval; the user does not review code locally.

## Adding recipes from scans
- Create one individual page under `recipes/` for each distinct recipe the user provides, using the existing recipe-page structure, and add a recipe card linking to each page in `index.html`.
- Preserve original source links when provided, and transcribe visible ingredient amounts and timings accurately. Preserve each legible handwritten note as a meaningful family preference at the relevant ingredient or step, clearly marked as a note, asterisk, or modification; keep it separate from the original recipe text. Label unclear handwriting as uncertain instead of guessing, and clearly identify other unreadable or absent information. Never invent missing directions.
- Write directions in concise original phrasing rather than reproducing long source text verbatim.
- Do not make unrelated list changes, such as adding a meal that is already listed. Do not add a scanner app or OCR tooling unless explicitly requested.

## Recipe photos
- Keep optimized recipe photos in `images/<recipe-filename-without-extension>/`, for example `images/butter-chicken/` for `recipes/butter-chicken.html`. Preserve each source filename and use the `.jpeg` extension for the optimized output.
- The `Optimize Recipe Images` GitHub Actions workflow accepts a recipe filename and comma-separated root-level `.jpg`/`.jpeg` filenames. It auto-orients each image, resizes it without upscaling so neither dimension exceeds 1920 pixels, saves it as JPEG at quality 85, removes the specified root-level originals, and commits the results to the branch selected when dispatching the workflow.
- Check the selected branch and recipe filename before running the workflow. Do not dispatch it on `main` for work intended for another branch. Review generated images and their file sizes before using them.
- In a recipe page under `recipes/`, reference an image using a relative path such as `../images/butter-chicken/IMG_1234.jpeg` and provide meaningful alt text. Do not add unoptimized source uploads as website images.

## Validation
- Check that local links resolve and run `git diff --check` before completing changes.
