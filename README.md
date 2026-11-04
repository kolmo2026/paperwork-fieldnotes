# Paperwork Fieldnotes

[日本語](README.ja.md) · [Educational site](https://blog.optmodel.com/)

An English/Japanese static blog with three original cross-tool practices: a reproducible research pack, a portable handoff, and source-page/financial-period labeling.

## Install and run

Requires Node 24+ and npm. Dependency installation needs a network connection.

```sh
git clone https://github.com/kolmo2026/paperwork-fieldnotes.git
cd paperwork-fieldnotes
npm ci
npm run build
npm run serve -- --port 4173
```

Open http://127.0.0.1:4173 after starting the local server. Stop it with Ctrl+C.

## Reproducible example

**Input:** site/content.mjs and site/style.css are the maintained editorial sources.

**Output:** 10 static HTML pages: English/Japanese home, About and three original articles; sitemap.xml, robots.txt and CNAME.

Fixtures: Articles contain synthetic folder structures, page recipes and share scenarios.. All supplied documents and numbers are synthetic.

## Tests and build sources

```sh
npm test
npm run build
```

Build and static page checks; no financial or PDF calculation engine in this repository.

Source: `site/` and `scripts/`. The static site is built to `docs/`, with English/Japanese equivalents, canonical/hreflang links, sitemap, robots, CNAME and .nojekyll. Its hostname is https://blog.optmodel.com. Each repository is self-contained; no sibling directory is needed to build.


## Limits

Educational workflows using synthetic examples. The blog contains no upload endpoint, backend, analytics or login. Product-site tutorials are linked, not copied.

## Privacy and tools

No account, analytics, backend or document-upload endpoint. Calculations/file operations run locally. Public site assets still load over the network; browser dependencies are bundled rather than fetched from a runtime CDN. JSON exports are plain text; review filenames and assumptions before sharing.

[Eqvero](https://eqvero.com/), [KolmoPDF](https://www.kolmopdf.com/) and [KomoPDF](https://komopdf.com/) are related products.


## License

MIT; see [LICENSE](LICENSE). Third-party dependencies retain their own licenses; when dependencies are installed, the build collects their license texts in THIRD-PARTY-NOTICES.txt.
