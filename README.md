# alebgl77.github.io

Source of [alebgl77.github.io](https://alebgl77.github.io/), the trilingual profile site of **Alexandre Beguel**, Agentic AI Architect and external Chief AI Officer (CAIO) based in Paris.

The site is an entity hub: one canonical page per language that search engines and AI answer engines can parse, with schema.org JSON-LD, hreflang alternates, a sitemap and an `llms.txt`. It is plain static HTML served by GitHub Pages: no build step, no JavaScript, no trackers, no external fonts.

## Structure

| Path | Purpose |
| --- | --- |
| `index.html` | English profile (`x-default`) |
| `fr/index.html` | French profile |
| `es/index.html` | Spanish profile |
| `sitemap.xml` | The three language pages with `xhtml:link` hreflang alternates, plus the project pages |
| `robots.txt` | Allows all crawlers, including AI search crawlers, and points to the sitemap |
| `llms.txt` | Plain-text summary for LLMs ([llmstxt.org](https://llmstxt.org/) format) |
| `404.html` | Not-found page linking back to the three languages |
| `.nojekyll` | Serves files as-is, without Jekyll processing |

Each page carries one JSON-LD `@graph` with `ProfilePage`, `WebSite`, `Person` (stable `@id` `https://alebgl77.github.io/#person` on all three pages), `Organization` (Digitalizor) and an `ItemList` of `SoftwareSourceCode` entries.

## Updating

Keep the three pages in sync: same facts, same `@id` values, same hreflang set on every page. When content changes, update `dateModified` in the JSON-LD, the visible "Last updated" date and `lastmod` in `sitemap.xml`.

## Profile

The full profile, with project details and upstream contributions, is on GitHub: [github.com/alebgl77](https://github.com/alebgl77).
