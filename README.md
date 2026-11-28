# Meals

A simple collection of meal ideas and family recipes. The plain-text lists
(`meals.txt`, `sides.txt`, and `suggestions.txt`) are still here, and the static
recipe site lives alongside them.

## View the recipe site

After GitHub Pages is enabled for this repository, the site will be available at
<https://enfcyco.github.io/meals/>.

## Add a recipe

1. Copy one of the HTML files in `recipes/` and give the copy a short filename,
   such as `chili.html`.
2. Edit its title, description, ingredients, and directions.
3. Add a link to the new page in the recipe cards in `index.html`.
4. Commit the changes to `main`; the Pages workflow publishes the site.

The site uses only HTML and CSS—no build tools or dependencies.

## Add a recipe photo

1. Add the original `.jpg` or `.jpeg` photo(s) to the repository root on the branch that contains the recipe.
2. In **Actions → Optimize Recipe Images → Run workflow**, select that branch, enter the recipe filename (for example, `butter-chicken.html`), and list the image filenames separated by commas.
3. The workflow saves auto-oriented JPEGs, resized to at most 1920 × 1920 pixels at quality 85, in `images/<recipe-filename-without-extension>/`. It removes the root-level originals and commits the optimized images to the selected branch.
4. Reference the result from the recipe page with a relative path, such as `../images/butter-chicken/IMG_1234.jpeg`, and add descriptive alt text.

Review the generated images before publishing. The workflow does not overwrite existing output files; rename or move a conflicting output before running it again.

## Enable GitHub Pages

In the repository's **Settings → Pages**, set the build and deployment source
to **GitHub Actions**. The workflow in `.github/workflows/pages.yml` then
deploys the site when changes are pushed to `main` (or when run manually).
