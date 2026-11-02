# Little Yard — static landing

Standalone HTML/CSS/JavaScript edition of Little Yard, published at:

**https://punktirok.github.io/l-yard/**

This repository contains only the generated static website, local images/fonts and bundled dependency notices. It has no application server, database, admin interface, request form, availability service or Telegram integration. The full application is maintained separately and is not deployed by this repository.

## Publishing

GitHub Pages serves the root directory of `main`. `.nojekyll` disables Jekyll processing. Pushing updated static files to `main` triggers publication automatically. No custom domain or paid hosting is configured. `404.html` is the custom error document for unknown URLs, including nested paths. It uses `/l-yard/`-rooted assets and a home link, without JavaScript or redirecting to the home page.

The editable source is maintained separately in the project's isolated `static-landing/` folder. Run its build, content check, TypeScript check and static verifier, then update this repository with the contents of its generated `site/` directory. Do not upload environment files, databases, uploads, source tooling or `node_modules`.

## Preview

```sh
python3 -m http.server 4173 --bind 127.0.0.1
```

Open http://127.0.0.1:4173/. Any ordinary static HTTP server can serve these files. Python’s generic preview server does not emulate Pages error routing; the 404 document’s asset/home paths expect the `/l-yard/` publishing prefix.

## Content and notices

This is the owner-authorized shareable presentation copy, published on 2026-11-02. Content is frozen from the public snapshot dated 2026-10-29, with request-related instructions adapted for this edition. House images/details remain illustrative, some external links remain service-homepage placeholders, and legal dialogs retain their preparation notices. The draft keeps `noindex, nofollow`; publication does not verify these provisional facts or enable bookings.

Dependency notices are in `app.js.LEGAL.txt` and `licenses/`. The build-time typography engine is not included in this repository or in the browser bundle.
