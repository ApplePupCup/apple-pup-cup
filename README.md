# Apple Pup Cup

Marketing site for **Apple Pup Cup** — a wholesome, apple-based dog treat made for coffee shops. A product of Kyler Family Farm Rescue & Therapy.

Built as a static site with [Eleventy](https://www.11ty.dev/).

## Requirements

- [Node.js](https://nodejs.org/) 18 or newer

## Getting started

```bash
npm install     # install dependencies (first time only)
npm start       # start the dev server at http://localhost:8080
```

The dev server rebuilds and refreshes the browser automatically as you edit files.

To generate the production build:

```bash
npm run build   # outputs static HTML/CSS to _site/
```

`_site/` is generated output and is not tracked in git.

## Project structure

```
src/
  index.md              Home page content
  products.md           Products page content
  about.md              Our Mission page content
  partner.md            Become a Partner page content
  _data/site.js         Site-wide values: name, description, contact email, footer text
  _includes/layouts/    Page templates (base, home, page)
  css/style.css         All site styles
.eleventy.js            Eleventy configuration
```

## Making common changes

**Page text.** Each page is a Markdown file in `src/`. The block at the top between `---` lines is structured content (headlines, buttons, product details) that the layout renders; edit the values, keep the labels and indentation as they are.

**Contact email, footer, or site description.** Edit `src/_data/site.js`. These values appear across every page.

**Navigation links.** Edit the header and footer link lists in `src/_includes/layouts/base.njk`.

**Styles.** All CSS lives in `src/css/style.css`.

## Deployment

The site deploys to GitHub Pages automatically. Any push to `main` triggers the workflow in
`.github/workflows/deploy.yml`, which builds the site and publishes it — there is nothing to run by hand.

The live domain is set by `src/CNAME`, which is copied into the build output on every build. Changing the
domain means editing that file **and** updating the custom domain under Settings > Pages.

Because the site is served from the root of a custom domain, no `pathPrefix` is needed and links can be
written as normal absolute paths (`/products/`).
