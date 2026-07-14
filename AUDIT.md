# Offline Mirror Audit — mc4dtp.ma

**Date:** 2026-07-13
**Source site:** https://mc4dtp.ma (WordPress)
**Deliverable:** `offline_mirror/mc4dtp.ma/` — complete, self-contained, offline-browsable copy
**Entry point:** open `offline_mirror/mc4dtp.ma/index.html` in any browser

---

## 1. Objective

Compare the previously scraped copy against the live site, identify everything
missing, and produce a mirror that is byte-for-byte browsable offline with all
pages and assets present and internal links rewritten to local paths.

## 2. Authoritative page list

The live site is WordPress, which publishes a machine-readable sitemap index at
`https://mc4dtp.ma/sitemap.xml`. This is the ground truth for "every published URL".

| Sitemap section | URLs |
|-----------------|------|
| Posts (`wp-sitemap-posts-post-1.xml`) | 11 |
| Pages (`wp-sitemap-posts-page-1.xml`) | 37 |
| Categories (`wp-sitemap-taxonomies-category-1.xml`) | 5 |
| Tags (`wp-sitemap-taxonomies-post_tag-1.xml`) | 13 |
| **Total real published URLs** | **65** (66 incl. home `/`) |

Every one of these was confirmed live (HTTP 200) — no stale sitemap entries.

## 3. Findings — the earlier captures were incomplete

| Capture | Tool | Real pages captured | Verdict |
|---------|------|--------------------|---------|
| `scraped_site/` | Playwright (`web_scraper.py`) | 26 / 65 | Incomplete |
| `mirror_mc4dtp/` | wget (earlier run) | recovered 8 more, still partial | Incomplete |
| **`offline_mirror/`** | **wget (this run, sitemap-seeded)** | **66 / 66** | **Complete** |

### Root cause of the gaps
`web_scraper.py` only follows links it finds *rendered in the page HTML*
(see lines 121–127). It never reads `sitemap.xml`. Any page not linked from the
visible navigation was therefore never discovered — this skipped 36 pages,
including 2 real blog posts and a set of WordPress/theme demo pages.

### Pages missing from *both* earlier captures (36), now included
- **Real blog posts:** `functional-and-stylish-wall-to-wall-shelves-2`,
  `how-to-make-a-huge-impact-with-multiples`
- **Section pages:** `blog`, `our-services`, `projets`
- **Theme demo/boilerplate pages:** `shop`, `shop-2`, `cart`, `cart-2`,
  `checkout`, `checkout-2`, `my-account`, `my-account-2`, `sample-page`,
  `team`, `history`, `home-dark`, `home-onepage`,
  `projects-2-columns`, `projects-3-columns`,
  `projects-grid-2-columns`, `projects-grid-3-columns`, `projects-grid-4-columns`,
  `gallery-2-columns`, `gallery-3-columns`, `gallery-4-columns`
- **Taxonomies:** `category/uncategorized`, `category/slider`, and tags
  `application`, `art`, `html5`, `internet`, `music`, `printf`, `responsive`, `website`

## 4. How the mirror was built

```
wget --mirror --page-requisites --convert-links --adjust-extension \
     --no-parent --span-hosts --domains=mc4dtp.ma -e robots=off \
     --no-check-certificate --tries=3 --timeout=30 \
     -U "Mozilla/5.0 ..." -i seed_urls.txt -P offline_mirror
```

- `-i seed_urls.txt` seeded all 66 sitemap URLs so unlinked pages are fetched.
- `--page-requisites` pulled every CSS/JS/image/font each page needs.
- `--convert-links` rewrote internal references to local relative paths.
- `--adjust-extension` saved pages as `.html`.

## 5. Completeness verification

| Check | Result |
|-------|--------|
| Sitemap pages present locally | **66 / 66, 0 missing** |
| Total files | 448 |
| HTML pages | 136 |
| Images (jpg/png/gif/svg/webp) | 138 |
| CSS files | 19 |
| JavaScript files | 26 |
| Fonts (woff/ttf/eot) | 17 |
| Total size | ~19 MB |
| Internal links rewritten to local | Yes |

## 6. Known limitations (inherent, not scrape gaps)

Two third-party scripts call live Google servers on every page load and can
**never** function offline — they are left as absolute URLs by design:

- **Google Maps embed** (`maps.google.com/maps/api/js`) — map on contact/about pages
- **reCAPTCHA** (`google.com/recaptcha/api.js`) — contact form

The `xmlrpc.php` link left absolute is a WordPress backend endpoint, not a
viewable page. Some theme icon images returned 404 *on the live server itself*
(they don't exist upstream) — not a download failure.

## 7. Files in this project

| Path | Status |
|------|--------|
| `offline_mirror/` | **KEEP** — the complete offline copy (deliverable) |
| `offline_mirror_wget.log` | download log (safe to delete) |
| `scraped_site/` | superseded — incomplete Playwright scrape |
| `mirror_mc4dtp/` + `mirror_mc4dtp_wget.log` | superseded — earlier partial wget |
| `web_scraper.py` | original scraper script |

**Bottom line:** `offline_mirror/` is the authoritative, verified-complete,
fully offline-browsable copy of mc4dtp.ma. The older captures can be deleted.
