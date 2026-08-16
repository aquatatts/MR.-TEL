# SEO Audit — TEL Collection & Squires Ink

**Date:** 2026-08-16
**Scope:** `telcollection.com.au` (Shopify Basic, AUD, AEST) + Squires Ink (Squarespace/Wix — *domain pending*)
**Priority:** Both properties, weighted toward local search
**Status:** Phase 1 complete (Shopify data layer). Phases 2–4 blocked on access — see [Blockers](#blockers).

---

## 1. Executive summary

TEL Collection is a **one-product store**: three products exist, two are archived, and a single
sealed set (`The Ritual Duo`) is sellable. Six collections exist; four contain zero products.

That shape dictates the strategy. There is no catalogue to optimise, so organic growth has to come
from **content depth** (The Healing Guide, the founder story, aftercare long-tail) and — for Squires
Ink — **local search**, where a Surfers Paradise studio can realistically win the map pack.

The product page itself is well optimised. The problems are everything *around* it.

---

## 2. Findings — TEL Collection

### 🔴 Critical (verify before anything else)

**F-1 — Active product may not be published to the Online Store channel.**

`onlineStoreUrl` returns `null` for all three products, including the ACTIVE one. That field is
normally populated for any product published to Online Store. If the product genuinely isn't
published, it is not crawlable, not indexable, and not purchasable — which would make every other
finding in this document irrelevant until fixed.

*Not confirmed.* The connected Shopify app lacks the `read_product_listings` scope, so
`publishedOnCurrentPublication` and `resourcePublications` could not be read.

> **Action:** Shopify admin → Products → The Ritual Duo → **Publishing** → confirm *Online Store*
> is ticked. Also confirm the storefront is not password-protected (Online Store → Preferences).

---

### 🟠 High

**F-2 — Every collection is missing its SEO title and meta description.**

All six collections return `seo.title: null` and `seo.description: null`. Google is generating
snippets unaided on every category page. Drafted replacements: [`fixes.md`](./fixes.md).

| Collection | Handle | Products | SEO title | Meta description |
|---|---|---:|---|---|
| Home page | `frontpage` | 1 | ❌ | ❌ |
| Ritual | `ritual` | 1 | ❌ | ❌ |
| Movement | `movement` | 0 | ❌ | ❌ |
| Threads | `threads` | 0 | ❌ | ❌ |
| Vision | `vision` | 0 | ❌ | ❌ |
| Collective | `collective` | 0 | ❌ | ❌ |

**F-3 — Three trust pages are unpublished.**

`Shipping and Returns`, `Privacy Policy`, and `FAQs` all have `isPublished: false`.

For a product applied to broken skin, policy and trust pages carry real E-E-A-T weight, and buyers
look for them before a first purchase. `FAQs` is also the cheapest long-tail content on the site —
"how long does a tattoo take to heal", "can I use moisturiser on a new tattoo", and similar queries
map directly onto FAQ entries and are eligible for rich results.

**F-4 — Four empty collections are live.**

`Movement`, `Threads`, `Vision`, and `Collective` each hold zero products and carry only a
"Coming soon" line. On a site with one sellable product, four thin pages meaningfully dilute
crawl signal and risk a thin-content assessment.

> **Recommendation:** `noindex` them (or remove from navigation and the sitemap) until each holds
> real stock. Do not write SEO metadata for pages that should not be indexed — that is why
> `fixes.md` deliberately omits them.

---

### 🟡 Medium

**F-5 — Archived products need redirects.**

`Restore Balm` (`/products/restore-balm`) and `Recovery Cream` (`/products/recovery-cream`) are
ARCHIVED. Archived Shopify products return 404. If either URL was ever indexed or linked, add
301 redirects to `/products/tattoo-aftercare-kit` to preserve equity and avoid soft-404s.

*Depends on:* Search Console coverage data to confirm whether these were ever indexed.

**F-6 — `/collections/frontpage` is a duplicate-content risk.**

The `frontpage` collection has no description and no SEO fields, and typically surfaces the same
product as the homepage. Canonicalise to `/` or `noindex`.

---

### 🟢 Working well — keep

- **Product SEO on The Ritual Duo is genuinely strong.** The SEO title
  (`Tattoo Aftercare Kit | The Ritual Duo — TEL Collection`) leads with the category term rather
  than the brand name, and the handle is `tattoo-aftercare-kit` rather than `the-ritual-duo`.
  That is the correct trade — search volume sits on the category, not the product name.
- **Descriptive image alt text** on the featured media.
- **The Healing Guide** (`/pages/healing-guide`) is a strong topical asset and the natural hub for
  an aftercare content cluster.
- **The Founder** (`/pages/founder`) — a named practitioner with fifteen years of first-hand
  experience and studio ownership is exactly the experience signal Google's guidelines reward.
  This is an under-exploited asset.

---

## 3. Squires Ink — pending

**Blocked: domain not yet supplied.** Platform confirmed as Squarespace/Wix.

A tattoo studio in Surfers Paradise competes in the local pack, not in classic organic. Planned
audit dimensions once the URL is available:

- **Google Business Profile** — category accuracy, service list, hours, booking link, photo
  cadence, Q&A, post frequency
- **Reviews** — volume, velocity, response rate, keyword content
- **NAP consistency** — name/address/phone identical across GBP, site, socials, and AU directories
  (True Local, Yellow Pages, Hotfrog, Localsearch)
- **On-site local signals** — `LocalBusiness` / `TattooParlor` schema, embedded map, address in
  footer, location-qualified titles
- **Service-page coverage** — cover-ups, full back, sleeves, laser removal, walk-ins, and
  Gold Coast / Surfers Paradise geo-modified variants
- **Artist pages** — individual artist profiles are a reliable long-tail and portfolio-search win
- **Cross-property link** — Squires Ink → TEL Collection is a natural, relevant internal link
  between two genuinely related properties

---

## 4. Blockers

| # | Blocker | Owner | Unblocks |
|---|---|---|---|
| B-1 | Squires Ink domain unknown | You | All of §3 |
| B-2 | Egress proxy blocks `telcollection.com.au` (403 at CONNECT) | You — allowlist in environment network policy | Rendered titles, canonicals, Product JSON-LD, OG tags, `robots.txt`, `sitemap.xml`, Core Web Vitals |
| B-3 | Google Search Console `NOT_AUTHENTICATED` | You — connect | Queries, impressions, CTR, index coverage, F-5 confirmation |
| B-4 | Google Analytics 4 `NOT_AUTHENTICATED` | You — connect | Organic landing pages, conversion paths |
| B-5 | Shopify app missing `read_product_listings` | You — re-auth with scope | Definitive answer on F-1 |
| B-6 | No backlink tool connected | — | Off-page analysis (out of scope unless Ahrefs/Semrush available) |

---

## 5. Plan

**Phase 1 — Shopify data layer** ✅ complete (this document)

**Phase 2 — Technical crawl** *(needs B-2)*
Rendered `<title>` / meta / canonical per template, Product + Organization + Breadcrumb JSON-LD,
Open Graph, `robots.txt`, `sitemap.xml` completeness, redirect chains, Core Web Vitals on mobile.

**Phase 3 — Search performance** *(needs B-3, B-4)*
Query and page-level performance, striking-distance terms, CTR outliers against drafted metadata,
index coverage, cannibalisation between the product page and The Healing Guide.

**Phase 4 — Local** *(needs B-1)*
Full Squires Ink local audit per §3, plus a Gold Coast keyword map.

**Phase 5 — Roadmap**
Prioritised 90-day plan across both properties, effort vs. impact.

---

## Appendix — method

All Phase 1 findings were read directly from the Shopify Admin GraphQL API against the connected
`TEL Collection` store on 2026-08-16. No live-site crawling was possible (B-2). No figure in this
document is estimated or inferred from outside that data; anything unverified is labelled as such.
