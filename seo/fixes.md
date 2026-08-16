# Ready-to-apply fixes — TEL Collection

Drafted from live Shopify data on 2026-08-16. **Nothing here has been applied.** These are
proposals for your store; say the word and I'll write them via the Shopify Admin API, or you can
paste them in manually.

Character counts are given because Google truncates around ~60 (title) and ~155 (description).

---

## 1. Collection metadata (fixes F-2)

Only collections that *should* be indexed are drafted. `Movement`, `Threads`, `Vision`, and
`Collective` are deliberately omitted — they hold zero products and should be `noindex`ed until
stocked, not optimised. Writing metadata for them would be optimising pages you don't want ranked.

### `ritual` — Ritual

**SEO title** (50)
```
Premium Tattoo Aftercare | Ritual — TEL Collection
```

**Meta description** (144)
```
Premium tattoo aftercare from TEL Collection. Restore Balm seals and protects fresh ink; Recovery Cream keeps healed work sharp. Sold as one set.
```

*Rationale:* leads with the category term ("tattoo aftercare"), which carries the search volume;
"Ritual" alone has none. Mirrors the convention already used correctly on the product page.

### `frontpage` — Home page

**Preferred fix:** `noindex` this collection, or canonicalise it to `/`. It duplicates the homepage
and has no independent purpose (F-6).

If you'd rather keep it indexed, use:

**SEO title** (55)
```
Tattoo Aftercare, Built by a Collector | TEL Collection
```

**Meta description** (149)
```
TEL Collection makes premium tattoo aftercare in Australia. The Ritual Duo — Restore Balm and Recovery Cream, formulated as one sealed two-step system.
```

---

## 2. Homepage metadata

Set in **Online Store → Preferences**, not on a collection. Worth checking — it wasn't readable
from the API and is the highest-traffic template on the site.

**SEO title** (58)
```
Premium Tattoo Aftercare Australia | TEL Collection
```

**Meta description** (152)
```
A sealed two-step tattoo aftercare system, never sold apart. Restore Balm for fresh ink, Recovery Cream for the years after. Built by a collector of 15 years.
```

---

## 3. Publish the trust pages (fixes F-3)

Set `isPublished: true` on:

- `shipping-and-returns`
- `privacy-policy`
- `faqs`

Shopify also expects refund, privacy, and terms policies to be populated under
**Settings → Policies** — these generate their own indexable `/policies/*` URLs.

### FAQ topics worth covering

Each maps to real aftercare search demand and is eligible for FAQ rich results via `FAQPage`
schema. Drawn from the ground your own product copy already covers:

1. How long does a new tattoo take to heal?
2. When can I start using moisturiser on a new tattoo?
3. Balm or cream — which do I use, and when?
4. How do I care for a cover-up or heavy black work? *(the layered protocol — genuinely
   differentiated content, and almost nobody covers it)*
5. Why is the Duo sold as a set and not separately?
6. Can I use this on healed tattoos?
7. Is it safe for sensitive skin?
8. How long does one 60 ml jar last?

Answer each in 40–60 words on `/pages/faqs`, then internally link to `/pages/healing-guide` and
the product page.

---

## 4. Redirects (fixes F-5)

Add under **Online Store → Navigation → URL Redirects**, once Search Console confirms these were
indexed:

| From | To |
|---|---|
| `/products/restore-balm` | `/products/tattoo-aftercare-kit` |
| `/products/recovery-cream` | `/products/tattoo-aftercare-kit` |

---

## 5. Noindex the empty collections (fixes F-4)

For `movement`, `threads`, `vision`, `collective` — either remove them from navigation and the
sitemap until stocked, or add to `theme.liquid` within `<head>`:

```liquid
{%- if template contains 'collection' and collection.products_count == 0 -%}
  <meta name="robots" content="noindex, follow">
{%- endif -%}
```

This is self-clearing: each collection becomes indexable automatically the moment it has stock,
so there's nothing to remember to undo later.

---

## Suggested order

1. **F-1** — confirm the product is published *(nothing else matters until this is settled)*
2. **F-3** — publish the trust pages
3. **F-2** — apply collection metadata
4. **F-4** — noindex the empty collections
5. **F-5** — redirects, after Search Console confirms
