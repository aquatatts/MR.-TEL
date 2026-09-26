# Privacy policy additions — TEL Collection + Squires Ink

**Status:** draft for review, not applied. Nothing on the store has changed.
**Applies to:** the existing Shopify store policy at **Settings → Policies → Privacy policy**,
served at `https://telcollection.com.au/policies/privacy-policy`.

TEL Collection and Squires Ink are the same legal entity (ABN 62 679 571 021), so one policy
covers both. These sections are **additions** to the current Shopify template, not a rewrite.
Each block says where it goes.

Placeholders are in `[square brackets]` — fill them before publishing.

This is a practical draft, not legal advice. Have your accountant or lawyer read it once before
it goes live, particularly §3.

---

## 1. Replace the opening paragraph

> **Last updated: [date you publish]**
>
> This Privacy Policy is issued by **[legal entity name]** (ABN 62 679 571 021), which trades as
> **TEL Collection** and **Squires Ink**, at Shop 7, 26 Orchid Avenue, Surfers Paradise QLD 4217.
> "We", "us" and "our" mean that business under either name.
>
> It covers the TEL Collection online store at telcollection.com.au, the Squires Ink tattoo studio
> and its website at squiresink.com, and any other way you deal with us, including signing a
> waiver in the studio.

*Why:* the current opening only covers "this store and website". It also shows a "Last updated"
date of 28 July, but the record was last edited on 21 June. Set a real date when you publish.

---

## 2. Add under "Personal Information We Collect or Process"

> - **Studio and waiver information.** When you get tattooed at Squires Ink we collect the details
>   on our client waiver: your name, date of birth, contact details, identification to confirm you
>   are over 18, and the design, placement and artist for your tattoo.
> - **Health information.** The waiver asks about health matters relevant to your safety during and
>   after a tattoo, such as medical conditions, medications, allergies and pregnancy. See §3 for how
>   we handle this.

---

## 3. New section — Health information

> **Health information**
>
> We collect health information on our waiver only to decide whether it is safe to tattoo you and
> to give you the right aftercare advice. We collect it with your consent when you complete the
> waiver.
>
> We do **not** use your health information for marketing, and we do not add it to our email or
> customer lists. It is stored with your signed waiver and seen only by studio staff who need it.

*Why this matters most:* health information is sensitive information under the Privacy Act. It's
also the one thing that can bring a small business under the Act even if its turnover is below
$3M. This section has to stay true in practice as well as on paper — see the build note at the
end.

---

## 4. Add under "How We Use Your Personal Information", after "Marketing and Advertising"

> **Marketing when you opt in at the studio.** If you tick the marketing box on your Squires Ink
> waiver, we will use your name and email address to send you news, aftercare guidance and offers
> from both Squires Ink and TEL Collection. Ticking the box is optional. It is never a condition of
> getting tattooed, and you can unsubscribe at any time using the link in any email.

---

## 5. Add under "Personal Information Sources"

> - **From the Squires Ink studio**, when you complete a client waiver.

---

## 6. Add under "How We Disclose Personal Information"

> We use service providers to run the business, including **Shopify** (online store),
> **Smartwaiver** (studio waivers), **Square** (studio payments), **Klaviyo** and **Mailchimp**
> (email). Some of these providers store information outside Australia, including in the
> **United States**. They handle your information on our behalf and only for the services they
> provide to us.

*Why:* the template only says "vendors". Naming the providers and the likely country is what the
overseas-disclosure principle (APP 8) expects where it's practicable. Check this list against what
you actually use before publishing.

---

## 7. Replace "Complaints"

> **Complaints**
>
> If you have a concern about how we have handled your personal information, contact us using the
> details below and we will respond within 30 days. If you are not satisfied with our response, you
> can complain to the **Office of the Australian Information Commissioner** at
> [www.oaic.gov.au](https://www.oaic.gov.au).

*Why:* the template points to an unspecified "local data protection authority". For an Australian
business that should be the OAIC.

---

## 8. Add to "Security and Retention of Your Information"

> We keep signed studio waivers for [period — confirm with your insurer], as they are part of our
> records of each tattoo. We keep marketing contact details until you unsubscribe or ask us to
> delete them.

---

## 9. Contact

The current policy lists **0407 772 614** and **info@telcollection.com.au**. The Squires Ink
Business Profile lists **0415 747 474**. Decide which contact handles privacy requests for both
brands and use it in the Contact section. One contact is simpler.

---

## Build note for the Smartwaiver opt-in — this is what keeps §3 true

When Smartwaiver sends a waiver to Mailchimp or Klaviyo (by webhook, Zapier or Make), it can send
**every field on the form, health answers included**. If the connection is set to "send
everything", your email platforms end up holding medical information. That breaks the promise in
§3, and it creates exactly the kind of data you least want stored in an email tool.

Map only these fields:

| Send | Don't send |
|---|---|
| First name, last name | Date of birth |
| Email | ID details |
| Marketing opt-in (true only if ticked) | Any health or medical answer |
| Consent timestamp | Design, placement, artist notes |
| `source: waiver` | Signature |

And only send a contact if the opt-in box was ticked. Everyone else stays in Smartwaiver only.

---

## Waiver checkbox wording (final)

> ☐ Yes — send me aftercare tips, studio news and offers from **Squires Ink** and
> **TEL Collection**. Optional, and you can unsubscribe any time.
> [Privacy Policy](https://telcollection.com.au/policies/privacy-policy)

Use the full URL. The waiver is hosted on Smartwaiver's domain, so a relative link would break.
Also link the footer of squiresink.com to the same policy, so both brands point at one document.
