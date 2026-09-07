# TEL Collection — Pre-launch audit (Chapter One: The Ritual Duo)

Prepared 4 September 2026, six days before doors open (Thursday 10 September).
Scope: the Shopify store at telcollection.com.au (theme "TEL v3 — LIVE (2 Sep)", password-gated),
the v4 work-in-progress theme, Klaviyo, Shopify analytics and both Meta ad accounts.

---

## 1. Where it stands — scorecard

Scores are out of 10 against what a premium DTC skincare launch needs on day one.

| Area | Score | Read |
|---|---|---|
| Brand identity (mark, palette, packaging) | 8 | The monogram, black glass and foil system is the most luxury-coded identity in tattoo aftercare. Nobody else in the category looks like this. |
| Voice and copy | 8 | Distinctive, confident, specific ("Earned. Not given.", "Sealed, not split"). Overwritten in places: the product page carries ~900 words and the founder quote appears three times across the site. |
| Visual system on the site | 6 | Theme (Prestige) is set up well: Cormorant + EB Garamond, #080808 / #F5F0E8 / gold. But custom pages break the system (see §3). |
| Imagery | 5 | Nine clean packshots, one hand-in-cream shot, one "settled ink" chest shot. No motion, no 3D, no editorial scene, no texture macro. This is the biggest gap between the ambition and the page. |
| Product page conversion | 5 | Price, reviews badge and sticky ATC are right. Quantity selector, variant picker and badges on a single-variant product add noise. Eight accordions below the fold, no "what's in the box" visual, no FAQ block, no shipping/returns reassurance near the button. |
| Trust and proof | 4 | 6 Judge.me reviews, 5.0 average, but only 1 is a verified buyer and several are reviews of the tattoo studio, not the product ("Alex, you're an artist bro", "friendly staff"). The gate page claims "10 verified reviews". A premium buyer notices. |
| Structure and navigation | 6 | Four-item main menu is clean. The Healing Guide (your best SEO and retention asset) is footer-only. Five empty "chapter" collections exist and must stay unlinked. Privacy Policy page unpublished. |
| Tracking and analytics | 3 | Meta pixel present with a hand-coded Lead event on the gate. No Conversions API confirmed, no GA4 confirmed, no UTMs on any of ~4,600 sessions (all arrive untagged). No purchase signal exists yet because nothing can be purchased. |
| Email / CRM (Klaviyo) | 4 | 3 live post-purchase flows, which is good. Zero sign-up forms, no welcome flow, no abandoned checkout, no browse abandonment, no launch sequence. Main list is double opt-in, which will cost you a share of every sign-up on launch day. |
| Paid media readiness | 3 | ~A$2,970 spent in 90 days, 84% of site traffic from Facebook, almost all of it to the password gate. Spend is spread evenly across ages 18 to 65+ and both genders. "New Sales" campaign is optimising for purchases on a store that cannot take them. |
| **Overall launch readiness** | **5.2** | **Brand is ready. The machine around it is not.** |

Ranking against the field on *premium feel*: top 3 in the category (with Stories & Ink and Mad Rabbit's premium line).
Ranking on *execution polish*: bottom half, purely because it is pre-launch and the imagery and trust layers are thin.

---

## 2. What is actually live (site anatomy)

**Store:** Shopify Basic, AUD, Australia, password-protected. Theme: Prestige (Maestrooo). Nine theme copies exist; "TEL v3 — LIVE (2 Sep)" is the published one, "TEL v4 — WIP (rose copper + shoot)" is in progress.

**Catalogue:** one active product, The Ritual Duo, A$59.95, SKU TEL-RD-60, 450 in stock of the first run of 500. Restore Balm and Recovery Cream exist as archived singles (correctly hidden). Collections: Home page, Ritual (1 product), Movement, Threads, Vision, Collective (empty, the future chapters).

**Home page (v3) section order:** hero ("Earned. Not given.") → founder band → featured product → three columns (Restore / Recovery / Sealed) → proof strip (heavy metals, micro, pH, shelf life, ISO/GMP) → "Our Aim" overlay → newsletter.

**Home page (v4 WIP) section order:** hero → product header → product band → "Why two" → studio band → proof strip → founder band → "Chapter One: Five hundred sets, doors open Thursday 10 September" → newsletter. v4 is the better sequence: product before founder, one idea per band, and it fixes the four identical footer icons.

**Product page:** vendor, title, Judge.me badge, price, payment terms, lead copy, mono spec line, variant picker, quantity, buy buttons, then eight accordions (Ritual, Routine, Why it can't be split, Heavy work protocol, Founder, Standard, Shipping). Judge.me full widget below.

**Pages:** Contact, Our Aim, Shipping & Returns (free AU shipping, 1–2 day dispatch), FAQs, Trusted By, The Founder, The Healing Guide. Privacy Policy page exists but is unpublished (footer points at the Shopify policy URL instead, which is fine if that policy is filled in).

**Gate page:** custom-built. Email capture is the primary action, storefront password demoted to a toggle. Fires Meta PageView and a Lead event on sign-up. Offer: 24 hours early access and "the founding price, which will not run twice".

---

## 3. Style review — where you stand and what breaks

**What is right.** Black ground, cream type, one metallic accent, a serif pairing with wide letter-spacing on headings, one italic gold word per heading as a brand device. That device ("Earned. Not *given*.") is genuinely yours and worth protecting. Packaging and site speak the same language, which most small brands never achieve.

**What breaks the premium read.**

1. **Two metallics.** The theme (v3) is gold #C9A24B. The Founder page and v4 are rose copper #DCA47B. Trusted By, FAQs and the gate are gold. The physical jars and box are gold foil; the Chapter One card is copper. Pick one for the site and match it to the foil on the product. If the jars are gold, the site is gold. Copper can live on the card and on limited-edition touches only.
2. **Three typographic systems.** Theme pages: Cormorant + EB Garamond. Founder page: Cormorant + EB Garamond + IBM Plex Mono (good, matches). Trusted By, FAQs, Healing Guide and the gate: system sans-serif (-apple-system / Segoe UI). On an iPhone that means Helvetica-style headings on your proof pages and Garamond everywhere else. Rebuild those pages on the theme's rich-text / page sections so they inherit the fonts, or set the page CSS to the same stack as the Founder page.
3. **Density.** Long serif paragraphs on a black ground at 17px are hard to read on mobile, which is 78% of your traffic. The founder story deserves its page; on the product page it should be one pull-quote and a link.
4. **Single-product clutter.** Remove the variant picker and quantity selector blocks on the product page and home featured product. One product, one price, one button. That is the "elevated essentials" promise made visible.
5. **Hero asset.** v3 hero is a PNG (TC_EE_Image_2.png), heavy and static. v4 swaps in the packshot, which is cleaner but still a still. The hero is where a 3D turntable or a 6-second loop belongs (see §5).
6. **Announcement bar copy** is right ("CHAPTER ONE · FIVE HUNDRED SETS · THURSDAY 10 SEPTEMBER"). After launch it should count down the remaining sets, honestly.

**Verdict:** the identity is a 9, the site is a 6 wearing the identity. The fix is consistency and imagery, not a redesign.

---

## 4. Trust layer — fix before Thursday

- Keep only reviews about the product. Move the studio reviews (Chriso, Eli, Ejrule) to the "From the chair" section of Trusted By, labelled as Squires Ink Google reviews. Product reviews with a "verified buyer" badge are worth ten unverified ones on a premium page.
- Gate page says "5.0 · 10 verified reviews". Judge.me shows 6 reviews, 1 verified. Change the line to what is true or remove the number.
- Turn on Judge.me's post-fulfilment review request (14 days for a balm, 45 days for the cream stage) so every online order becomes a verified review with a photo.
- Add the batch test results as a downloadable "Certificate of Analysis" page. The proof strip claims are strong; letting people see the document is stronger.
- Claims hygiene: the copy is already careful (moisturise, condition, protect). Keep "heal" out of product copy; "Healing Guide" as a page name is fine.

---

## 5. Imagery and 3D — how to get "direct, clean, insane"

**Shopify supports 3D natively.** Upload a .glb (web) and a .usdz (iOS) to the product's media and Prestige renders an interactive model in the gallery with a "View in your space" AR button on phones. No app needed.

**Recommended path (in order):**

1. **Commission one photoreal 3D model** of the box and both jars. A Blender or Cinema 4D artist builds it from the packaging dieline and label artwork. Cost A$600–1,800, one to two weeks. This single asset produces everything below.
2. **From the model:** a 6–8 second hero turntable loop (MP4/WebM, under 3 MB) for the home hero; the GLB/USDZ for the product gallery and AR; 4–6 CGI "scene" renders (obsidian, wet stone, gold ring light, mist) in the style of the Firefly concept in this repo, but with labels that are pixel-accurate; and clean ad stills at 1:1, 4:5 and 9:16.
3. **Why CGI over AI image generation for hero assets:** AI renders garble label text and jar proportions. For a brand whose entire pitch is "built to a standard", the label on the hero must be the real label. Use AI for mood boards and background plates, not for the product.
4. **Real photography still matters.** The founder's chest and back, the hand in cream, the studio counter: these are the proof that CGI cannot fake. Shoot a half-day with a photographer who does skincare texture work: macro of balm being scooped, the cream's surface, the two textures side by side, ink under studio light at day 1 / day 14 / day 90.
5. **Phase two (post-launch):** a scroll-driven 3D product story (Apple-style) built with Spline or Three.js in a custom section. Budget A$3–8k. Only worth it once traffic is real.

**Image spec for the product page:** 1 packshot, 1 open-jar texture, 1 in-use, 1 box/unboxing, 1 3D model, 1 founder proof shot, 1 ingredient panel. Seven, not nine, in that order.

---

## 6. The numbers (last 90 days)

**Traffic:** 4,601 sessions, 3,778 visitors. Facebook 3,867 (84%), direct 667, Instagram 46, Google 14. 93% of sessions landed on the password gate. Mobile Australia 3,520; desktop United States 512 (almost certainly Meta ad-review and bot traffic, ignore).

**Sign-ups:** 60 subscribed customers in Shopify from roughly 4,200 gate sessions, about 1.4%. A dedicated pre-launch gate with a real offer should convert 5–12%. The gate is well designed; the traffic being sent to it is not qualified (see Meta below).

**Sales:** 41 orders, A$2,188 total in 12 months. 34 are POS at the studio counter (A$1,978, AOV A$52.92, so some are discounted). Effectively zero online revenue, which is expected pre-launch but means there is no conversion baseline.

**Meta Ads (both accounts, 90 days, ~A$2,970 spend):**

| Campaign | Account | Objective | Spend | Clicks | CPC | CTR |
|---|---|---|---|---|---|---|
| New Sales ad set | Benny personal | Sales | 1,400 | 844 | 0.61 | 3.2% |
| Walk-Ins — Gold Coast | Benny personal | Engagement | 415 | 227 | 0.76 | 1.6% |
| Post: "Years in the making" | Benny personal | Traffic | 351 | 3,044 | 0.10 | 8.1% |
| Artists Wanted — AU | Benny personal | Engagement | 260 | 203 | 0.44 | 3.0% |
| Warm Entry v2 — AU | TEL Collection Ads | Traffic | 195 | 1,548 | 0.11 | 10.2% |
| Gold Coast 18–55 Reach | Benny personal | Awareness | 161 | 2 | 2.64 | 0.07% |
| Bookings — Mandala reel | Benny personal | Engagement | 158 | 61 | 1.05 | 1.5% |

Reads:
- The "Years in the making" creative is your winner: 10% CTR at A$0.10 a click across two runs. That story angle (founder, fifteen years, the rework) is what the market responds to. Build the launch creative from it.
- "New Sales ad set" has spent A$1,400 on a Sales objective with no purchase event possible. Meta has been optimising toward nothing. Pause it until Thursday, then relaunch with Purchase as the event.
- Studio campaigns (Walk-Ins, Bookings, Artists Wanted) are running from the same personal account as TEL. Separate them: TEL spend, pixel and audiences in the TEL Collection Ads account only, so lookalikes are built from TEL buyers, not walk-in enquiries.
- Age/gender spend is flat across 18 to 65+. CTR is highest in 55+ (a common accidental-click pattern) and lowest in 18–24. Nothing in the targeting says "heavily tattooed 22–40". That is the audience problem, and it is why the gate converts at 1.4%.

---

## 7. Launch stage — the next six days, then 30/60/90

**Before Thursday (in this order):**

1. Switch the Klaviyo "Email List" to single opt-in for the launch window. Confirm the Shopify gate sign-ups (tag "newsletter") are syncing into Klaviyo; if they are not, export and import the 60 now.
2. Build four Klaviyo flows: Welcome (3 emails: the standard / the ritual / the founder), Abandoned checkout (3 touches over 24h), Browse abandonment (1 touch), Back in stock (for when the 500 close). The Healing Guide and reorder flows already exist and are live.
3. Launch email sequence to the list: T-2 "Doors open Thursday, you go first", T-1 "The founding price, once", Launch morning (early access link + password for 24h), T+1 public open, T+3 "sets remaining" update.
4. Tracking: install the Shopify Facebook & Instagram app with Conversions API (server-side purchase events), remove the hand-rolled fallback pixel from the gate once confirmed, add GA4 through Google & YouTube app, and set a UTM convention (utm_source=meta / utm_medium=paid / utm_campaign=ch1-launch / utm_content=creative-name) on every ad and email link.
5. Site fixes: one metallic, one type system, product page de-cluttered, studio reviews moved, gate review line corrected, Healing Guide into the main menu, Privacy Policy page published or deleted.
6. Pause the "New Sales" campaign and the studio campaigns' spillover into TEL. Keep "Warm Entry / Years in the making" live to the gate until Wednesday night.
7. Studio: every client tattooed this week gets the Ritual Duo and a card with a QR to the Healing Guide and the review link. They are your first verified reviews.

**Launch day to day 30:** Meta Purchase campaign, ABO with three ad sets (founder story video, product CGI turntable, artist testimonial), Gold Coast + Brisbane first, then Sydney/Melbourne. Daily budget A$100–150. Target: first 100 online orders, 30 verified reviews, cost per purchase under A$35. Post-purchase review ask at day 14.

**Day 30–60:** lookalikes from purchasers, retarget engaged non-buyers, Google Shopping + brand search, first studio wholesale pilot (5 studios, 12 sets each, counter display). Second content shoot from real customer healed work.

**Day 60–90:** decide Chapter Two from the data (reorder rate on cream vs balm, studio sell-through), open the "Sets remaining" counter honestly, start SMS.

---

## 8. Targeted audiences — who actually buys a A$60 aftercare set

Ranked by expected conversion:

1. **Squires Ink clients (past 24 months).** Highest intent, already trust the founder. POS customers + studio booking list. Email + SMS + counter.
2. **Fresh-ink buyers, Gold Coast/Brisbane, 22–40.** Meta interests: tattoo artists, tattoo conventions (Australian Tattoo Expo), Inked, Tattoo Life, specific AU artists with large followings; layered with "engaged shoppers". This is the cold core.
3. **Heavily tattooed collectors, AU-wide.** The "fifteen years, full back rework" story is for them. Lookalike from purchasers once you have 100+.
4. **Gift buyers.** Partners/friends of someone booked in. The sealed black box is a gift already. Angle: "for the day after the session".
5. **Tattoo artists and studios (B2B).** The real moat. An artist who hands the Ritual Duo to every client is a channel. Build a wholesale/partner page, a counter display, and an artist referral code.
6. **Laser-removal and rework clients.** Underserved, higher pain, higher spend. The founder's own story is this exact customer.

Audiences to avoid: broad AU 18–65+, interest-free "advantage+" until the pixel has 50+ purchases.

---

## 9. Building the marketing team for stage two

Lean, mostly freelance, founder stays the face.

| Role | Who / how | Cost (A$/month) | First 30-day output |
|---|---|---|---|
| Brand + founder content | Benny | — | 3 Reels/week from the studio, every session a story |
| Performance media buyer | Freelance (Upwork / local), Meta + Google | 1,500–3,000 + ad spend | Account restructure, launch campaigns, weekly report |
| Content creator / videographer | Local, one half-day/week in studio | 1,200–2,000 | Product textures, client healed work, founder pieces |
| 3D / CGI artist | Project | 600–1,800 once | Model, turntable, 6 scene renders, AR files |
| Email / CRM | Claude + Klaviyo (this workflow) | — | Flows, launch sequence, weekly numbers |
| Customer care | Studio front desk | — | Same-day replies, review requests |

Weekly scorecard (already scaffolded in this workspace as "weekly numbers"): sessions, sign-ups, orders, conversion rate, cost per purchase, review count, sets remaining.

---

## 10. The gap you can own — "elevated essentials"

The category splits into three: pharmacy (Bepanthen, clinical, cheap), streetwear DTC (Mad Rabbit, Hustle Butter, Sorry Mom: loud, bundles, discounts) and natural/vegan (Ora's, Stories & Ink: soft, editorial). Nobody sits at "luxury ritual": black glass, one sealed system, one price, no sales, built by a collector in a working studio. That position is open in Australia and thin globally. The price (A$59.95 for 120 ml, A$0.50/ml) is premium but defensible against per-ml pricing of the DTC leaders.

Protect it by refusing three things competitors all do: discount codes on the product, single-jar sizes, and bundling with merch. The "no sales, no starter sizes" line is already on the page. Hold it.

(Competitor detail and positioning map in the companion artifact.)

---

## 11. Competitor field (summary; full tables in `tel-launch-audit.html`)

Twenty-eight brands checked. The Australian market splits four ways: pharmacy clinical (Bepanthen ~A$12/50g, ARTG-registered), supermarket natural (Dr Pickles A$22.50 at Coles/Woolworths; Ink Nurse A$34.99 across 600+ Chemist Warehouse stores), studio workhorse (Hustle Butter A$32.50/150ml, ProTat A$10/50g) and organic apothecary (Aftercare Collective, For Another Self, Penguin Tattoo Co, all Melbourne, all already using "ritual" language).

**Price per ml (A$):** Mad Rabbit 0.57 · **TEL 0.50** · Papatui 0.51 · Stories & Ink 0.49 · Sorry Mom 0.43 · Ink Nurse 0.40 · Aussie Inked 0.36 · Dr Pickles 0.30 · Bepanthen 0.26 · Hustle Butter 0.22 · Harry's Tattoo Frost 0.13.

**Finding:** no brand selling into Australia occupies premium price and luxury codes at the same time. The top-right quadrant is empty. Stories & Ink is the only scaled brand near it globally and is retail-coded, not black glass.

**Kits:** every competitor kit pairs a cleanser with a moisturiser (Stories & Ink Duo ~A$52, Ink Nurse Essentials A$84.99, Mad Rabbit Starter ~A$90). Nobody sells a seal-then-condition two-stage set. That structure is the argument for the price.

**Market:** 25% of Australians have a tattoo (McCrindle 2025; women 31%, men 19%; 61% have more than one). 1,860 studios, growing 4.5% a year (IBISWorld). Australian dedicated-aftercare retail estimated at A$10–15M a year. The premium tier above A$40 is effectively unserved.

**Watch:** Harry's Tattoo Frost (2026) at A$0.13/ml; Stories & Ink's 800 Target + 600 Superdrug footprint could enter AU via Amazon or Adore; Ink Nurse owns "Australia's #1" volume language, so own "the considered choice" instead. Run a class 3 trademark search on "The Ritual Duo" given Aftercare Collective ("Conscious Tattoo Ritual Care") and Penguin ("The Ritual Kit").

## 12. Their playbooks, TEL's counter-moves

| Pattern | Who | TEL's move |
|---|---|---|
| Pharmacy/grocery shelf | Bepanthen, Ink Nurse, Dr Pickles | Refuse the shelf. "Five hundred sets. Not in pharmacies." Number the cards 001–500. |
| Discount-led DTC | Ink Nurse bundles/codes, Mad Rabbit subs | Access replaces discount: first look, healing notes, priority on the next run. "Second Ritual" reorder at 6–8 weeks. Live sets-remaining counter. |
| Studio wholesale | Ink Nurse kit/Faire/Guild, Dr Pickles A$7 tubes | You own a studio: Squires Ink as flagship, "Healed at Squires" monthly gallery, then 10–20 hand-picked "TEL Studios" with a 12-set black-glass cabinet, exclusive by suburb, no open wholesale. |
| Ambassadors at scale | Mad Rabbit 7,000, Stories & Ink Artist Series | Artist Edition slip-case, 100 sets per artist, one per quarter. Proof is the artist's own client's healed piece. |
| Convention sponsorship | Ink Nurse, Dr Pickles | Don't sponsor; tattoo. A working Squires Ink booth, Duo sold only to people tattooed there, healing documented. |
| Short-form/UGC | Ink Nurse sale reels, Stories & Ink before/after | "One piece, four weeks" silent time-lapses with the founder's voice. One a week. Your own data: 10% CTR on the founder story. |
| Natural/vegan/organic | Aussie Inked, Tattman, Aftercare Collective, etc. | Don't compete on "natural". Compete on function (occlusive then humectant) and object (black glass, gold foil). |
| Attack SEO | Ink Nurse "truth about Bepanthen" | Don't attack. Healing notes by style that rank for "how to heal a [style] tattoo". Pitch GLOW/Tatt Lab as the premium pick (no luxury tier is listed). |
| Reviews | Ink Nurse ~4★ Trustpilot | Photo-required reviews at week four. 100 photo reviews from the first 500. |

## 13. Claims in Australia

Cosmetic (AICIS/ACCC) as long as copy stays at cleanse, moisturise, protect, appearance. Therapeutic (ARTG) the moment it claims to prevent, treat, cure or change physiology. **Never:** heals, healing, speeds healing, treats, repairs, regenerates, antibacterial, antiseptic, prevents infection, reduces scarring, prevents scabbing, anti-inflammatory, medical grade, clinically proven, SPF/UV, wound, first aid. **Safe:** soothes, hydrates, nourishes, maintains the moisture barrier, protects, supports skin through the settling weeks, keeps fresh ink comfortable, helps ink look vivid. Beeswax rules out "vegan" for Restore Balm; petrolatum rules out "natural". Don't claim either.

## 14. v4 mobile render

`docs/tel-v4-mobile-render.html` is a mobile-first render of v4's section order with the same fonts, black and gold, pushed to maximum premium. Twelve changes, all achievable in Prestige before Thursday: one metal (gold, matched to the jar foil), scene hero with slow push-in, mono spec strip, product before founder, one light product plate, hairline price ledger with no variant picker or quantity stepper, numbered two-step ledger, sideways proof strip, founder as pull quote, a "500" sets-remaining meter wired to inventory, 56px full-width mono buttons, monogram-only blurred header.

## 15. v5 against v4

v5 is built and unpublished in Shopify as "TEL v5 — premium draft (review vs v4)" (theme id 142920974399), duplicated from v4. Source in `theme/v5/`. Eight custom sections (`tel-hero`, `tel-spec-strip`, `tel-product`, `tel-steps`, `tel-band`, `tel-proof`, `tel-chapter`, `tel-newsletter`), one stylesheet (`assets/tel-v5.css`), rebuilt `templates/index.json`, de-cluttered `templates/product.json`, gold restored in `config/settings_data.json` and `layout/theme.liquid`, quieter header and announcement, sets-remaining meter wired to live inventory.

| Dimension | v4 | v5 |
|---|---|---|
| Look | 6.5 | 8.5 |
| Feel | 6.0 | 8.5 |
| Style consistency | 5.5 | 8.0 |
| Conversion mechanics | 5.0 | 7.5 |
| Vision and retention after Chapter One | 5.0 | 8.0 |
| **Overall** | **5.6** | **8.1** |

To nine: CGI turntable in the hero, the CW Media film and studio photography in the bands, verified photo reviews, and the four custom pages restyled to the theme. A leftover test section "TEL probe" sits in the section list (not on any page); delete it from Edit code if wanted. Publishing stays with the owner.

## 16. Klaviyo build (draft) and connectors

Before: 3 live post-purchase flows, no form, no welcome, no abandoned checkout, no browse abandonment, no launch sequence, double opt-in, no UTMs.

After, all draft: 12 branded templates; Welcome (3 emails, days 0/2/5); Abandoned checkout (1h, 24h, day 3, no discount, exits on purchase); Browse abandonment (4h, viewed but no checkout); Back in stock; four launch campaigns to the list, dated but unscheduled (Tue 7am, Wed 7am, Thu 6am with early-access password slot, Mon 7am) with full UTMs; first-access popup form.

Decisions left to the owner: single opt-in for launch week, the early-access password, the day-four sets count, and confirming the dedicated sending domain.

Connectors: Shopify, Klaviyo, Meta Ads and Facebook/Instagram Insights (Supermetrics), Xero (Squires Ink org; add a TEL tracking category), Google Drive (shoot assets present), Gmail, Calendar, Square, Mailchimp, GitHub connected. Not connected: GA4 (biggest gap; not installed on the store either), Google Ads, TikTok. Notion connected but empty.

---

## 7 September — v6 reviewed, the hero swapped, v6.1 built

**Context.** Ben built **TEL v6 — LAUNCH CANDIDATE (Thu 10 Sep)** (`142936834111`) on top of the v5 sections: real shoot photography in every slot, a reviews section wired to Judge.me, the credential box on the founder band, a live "sets remaining" line under the buy button, the Healing Guide linked from the steps band, and "seventeen years" made consistent. He likes where it is heading and asked for (a) the v5 hero photo, writing and placement on top, (b) the Aim part sorted, (c) an overall premium tune-up.

**What was done.** v6 is untouched. It was duplicated to **TEL v6.1 — v5 hero + premium tune-up (DRAFT)** (`gid://shopify/OnlineStoreTheme/142983823423`, unpublished) and the changes below were written there. Files changed vs v6: `templates/index.json`, `templates/page.json`, `templates/page.page.json` (new), `sections/header-group.json`, `sections/tel-hero.liquid` — mirrored in `theme/v6.1/`.

Compare render (three phones, v5 · v6 · v6.1, rendered from source with the shoot images): `docs/tel-v5-v6-compare.html`.

### The hero swap
- The scene render (`docs/assets/tel-scene-hero.jpg`, 1200×1797) was uploaded to Shopify **Files** as `tel-chapter-one-scene-hero.jpg` (MediaImage `29840071426111`, alt text set) so the section serves responsive 800–1200 px copies with `fetchpriority=high`, instead of the raw 220 KB theme asset.
- Hero settings: image = scene, no separate mobile image, mobile focal **top (50% 0%)**, desktop focal **centre (50% 50%)**, height 700 / 860, veil 86, push-in on. Eyebrow, heading ("Earned. Not *given*.") and "Shop the Ritual" are v5's and were already identical in v6; placement (low-left, 32 px / 72 px) unchanged.
- `tel-hero.liquid` gained a **Desktop focal point** select (upper third / upper-centre = v6's hard-coded value / centre / lower-centre). Note: Shopify validates JSON templates against the section schema at write time — the new setting had to be sent *after* the section file, or it is silently stripped.

### Tune-up applied in v6.1 (no copy changed)
1. Announcement bar: one 73-character message wrapped to two rows on phones → two messages, rotating every 5 s: "CHAPTER ONE · NOW OPEN · FIVE HUNDRED SETS" / "FREE SHIPPING AUSTRALIA-WIDE · SHIPS FROM SURFERS PARADISE".
2. Spec strip: back to three facts. "Free shipping" appeared four times on one page (bar, strip, price ledger, footer icons).
3. Background rhythm: strict alternation product · *steps* · proof · *reviews* · chair · *founder* · aim · *chapter* · newsletter (steps now lifted). v6 had founder and chapter both lifted, back to back.
4. **Our aim band** (`tel_aim`, type `tel-band`, no image) after the founder: eyebrow "Our aim", heading "Built on discipline. Driven by *purpose*.", pull quote "TEL isn't a brand you buy once. It's a standard you choose.", two lines from the page, outline button → `/pages/about`.
5. **Page template**: Our Aim, The Founder, Trusted By and The Healing Guide all carry their own `<h1>` inside custom HTML; the default `page.json` was printing the page title above them as a second centred heading inside an extra-small column. `show_title: false`, `page_width: lg`. Plain-text pages that use the "page" template suffix (Shipping & Returns; Privacy Policy when published) keep their title through a new `templates/page.page.json` (`show_title: true`, `page_width: sm`). FAQs carries its own h1 and was moved from the "page" suffix to the default template — neither the live v3 theme nor v6 has a `page.page.json`, so both pages already resolved to `page.json` there and nothing visible changed on the live site. Page bodies untouched.
6. Desktop focal control on the hero (above).
7. Live numbers verified: variant inventory 450 of 500; Judge.me metafields `reviews.rating_count` = 6, `reviews.rating` = 5.0 (the ledger hides itself at zero).
9. **Proof heading** (approved 7 Sep): "Tested. Not *claimed*." — the former heading leads the sub: "We live and breathe tattoos — we know chemistry. Both ingredient lists published in full, in order, exactly as they read on the jar. Nothing in there we can't explain."
10. **Chair band button** (approved 7 Sep): "Trusted by" → "The artists" (same link; the band's eyebrow is already "From the chair").
8. `sections/tel-spec-strip-probe.liquid` is already neutralised in v6 (no preset, never listed in the section picker); deletion in the code editor is the only remaining step.

### Ben's call (not changed)
- Founder band body is three paragraphs on a phone; the middle one is the one to cut.
- Klaviyo list is still double opt-in (carried from the last audit).
- Desktop hero: portrait scene crops to box + plinth on 16:9. If the landscape shoot is preferred on desktop, set Image = sealed-set r1 and Mobile image = scene (both pickers exist).

### Ranking, out of ten

| Axis | v5 | v6 | v6.1 |
|---|---|---|---|
| Look | 8.5 | 8.0 | **9.0** |
| Feel | 8.5 | 8.5 | **9.0** |
| Style | 8.5 | 8.5 | **9.0** |
| Vision & retention | 8.0 | 8.5 | **9.0** |
| Launch readiness | 6.5 | 8.5 | **9.0** |
| **Overall** | 8.0 | 8.4 | **9.0** |

Publish v6.1 as the Thursday theme.

### Housekeeping
- Seven `assets/zz-render-tmp-*.jpg` (600–900 px copies of the shoot images) were parked in the superseded **v5** draft theme (`142920974399`) purely to pull the images into the compare render, because the sandbox cannot reach the Shopify CDN and the API cannot delete theme files. Delete the v5 theme once v6.1 is approved.
- Links: editor `https://admin.shopify.com/store/iw0xvm-v5/themes/142983823423/editor` · preview `https://telcollection.com.au/?preview_theme_id=142983823423` · Our Aim on v6.1 `https://telcollection.com.au/pages/about?preview_theme_id=142983823423`.
