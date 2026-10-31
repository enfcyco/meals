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

## Enable GitHub Pages

In the repository's **Settings → Pages**, set the build and deployment source
to **GitHub Actions**. The workflow in `.github/workflows/pages.yml` then
deploys the site when changes are pushed to `main` (or when run manually).
