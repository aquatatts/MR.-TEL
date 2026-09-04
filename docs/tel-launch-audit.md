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
