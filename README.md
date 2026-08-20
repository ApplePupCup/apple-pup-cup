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

Not yet configured. The site is fully static, so any static host will serve the contents of `_site/` after running `npm run build`.
