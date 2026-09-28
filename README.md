# ETHLETE Mockups

Design mockups for the ETHLETE storefront redesign, by MHT Media.
Deployed to Vercel at every push to `main`. Not the live store.

## Adding a mockup

1. Export the screen from Claude Design.
2. Save it as `_exports/<slug>.html` — lowercase-with-dashes. The slug becomes the URL:
   `_exports/homepage.html` is served at `/homepage/`.
3. Optionally add a title and description in `mockups.json`. Without one, the title comes
   from the export's own screen label and the slug is title-cased.
4. Commit and push. Vercel runs `node tools/build.mjs` and publishes `public/`.

Hand-built pages that are not Claude Design exports go in `pages/<slug>/index.html`
instead, and are copied through as-is.

## Local preview

```
node tools/build.mjs
npx serve public
```

`public/` is generated and never committed.

## Notes

- Every page is served `X-Robots-Tag: noindex, nofollow`, and `robots.txt` disallows all.
  The site is public to anyone with the link, but stays out of search.
- Fonts, JS and small images are content-hashed into `_shared/` and de-duplicated across
  pages, so each page is a few KB rather than a few MB.
- Each export links the exact design-system CSS it shipped with, so republishing one page
  never shifts the others.
- `index.html`, `assets/`, `_ds/` and `support.js` at the repo root are an earlier
  pre-unpacked export. They are not part of the build and are not served.
