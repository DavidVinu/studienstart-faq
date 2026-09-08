# studienstart-faq

Static FAQ page for first-year medical students at Heidelberg University, written by two
buddies of the Fachschaft Medizin for their buddy group. The page is in German.

Live at <https://studienstart-faq.pages.dev>

## Layout

    site/index.html   the whole page: content, styles, search and filters in one file
    site/_headers     response headers for Cloudflare Pages

No build step, no dependencies. Open `site/index.html` in a browser to preview.

## Editing the content

Each question is a `<details class="q">` block inside the `<section class="group">` of its
category. To add one, copy an existing block; search, filters and the question counter pick
it up on their own.

`LINKS` at the top of the script fills the link boxes marked with `data-link`. An empty
`url` removes the box, so a link can be dropped without touching the markup.

## Deploy

    npx wrangler pages deploy site --project-name studienstart-faq --branch main

Needs a Cloudflare account with access to the Pages project.

## Note

The answers are the personal experience of the authors, not official information from the
university or the Fachschaft.
