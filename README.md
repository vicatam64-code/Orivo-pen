# Orivo — Shopify theme

A **complete, valid Shopify theme**. The homepage (`templates/index.json`) renders the
full Orivo Mullein Purifier landing page from `sections/orivo-purifier.liquid`.
Unlike a bare section file, this has the whole theme skeleton Shopify requires
(`layout/`, `config/`, `locales/`, the standard `templates/`), so Shopify will accept it.

## Structure
```
layout/theme.liquid          App shell (head + content_for_header/layout)
layout/password.liquid       Password-page shell
templates/index.json         Homepage → renders the Orivo landing page
templates/page.orivo-purifier.json   Same page, assignable to any Shopify Page
templates/*.liquid           Standard pages (product, collection, cart, search, blog, 404…)
sections/orivo-purifier.liquid       The Orivo landing page (markup, CSS, JS, real cart wiring)
config/settings_schema.json  Theme settings
config/settings_data.json
locales/en.default.json      Translations
```

## Option A — Upload the zip straight to Shopify (fastest)
Online Store → Themes → **Add theme → Upload zip file** → pick this zip → **Publish**.

## Option B — GitHub → Shopify
1. Create a GitHub repo and commit the **contents** of this folder at the repo root
   (so `layout/`, `templates/`, `sections/`, `config/`, `locales/` sit at the top level).
2. In Shopify: Online Store → Themes → **Add theme → Connect from GitHub** → pick the repo/branch.
3. Shopify syncs the theme automatically on every push.

## Set your real Variant IDs (required for checkout)
The bundle buttons add **real variants** to the Shopify cart. In the theme editor open the
**Orivo Purifier Page** section and paste each numeric **Variant ID**
(Shopify admin → Products → open a variant → number at the end of the URL):
Buy 1 · Buy 2 (Get 1 Free) · Buy 3 (Get 2 Free) · Shipping Protection (optional).
Until IDs are set, the buttons show a setup note instead of adding to cart.

## Notes
- Prices in the design (R749 / R1,499 / R1,999) are static text — keep them matching your variant prices.
- Gallery images are designed placeholders; swap in real product photos.
- Keep the footer disclaimer — this is a botanical aromatherapy product, **not** a medicine,
  medical device, or nicotine-replacement therapy.
