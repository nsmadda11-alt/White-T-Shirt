# Brand Studio decisions

This is the durable agreement between the learner and agent. Keep it concise and update it only with agreed choices or actual evidence. `Not chosen yet` is a valid status. Persona cards are hypotheses unless supported by real research.

[LEARNING.md](LEARNING.md) holds the short, reviewable record of learner explanations and help received. Keep the brand decisions and implementation evidence here; link rather than duplicate them.

## Current stage

- Stage: Baseline ready to try; brand decisions pending.
- Current feature: `BRAND-001` — first branded storefront and live style guide.
- Status: Pending learner scope agreement.
- Next small decision: Confirm the first slice after trying the neutral storefront.

## Product boundary

The product is the same white T-shirt throughout the comparison. The baseline offers a size selector and temporary demo bag. No real orders, payment, accounts, or persistence. Keep product facts stable between directions; do not add unsupported claims about materials, manufacturing, sustainability, fit, delivery, scarcity, reviews, or sales.

## Audience hypotheses

The primary need guides the page. Give the secondary card one contrasting need to check that same page; keep both cards brief.

| Tiny card                             | Primary audience          | Secondary audience        |
| ------------------------------------- | ------------------------- | ------------------------- |
| Person in a concrete situation        | Not chosen yet            | Not chosen yet            |
| Goal or meaning they seek             | Not chosen yet            | Not chosen yet            |
| Concern before choosing               | Not chosen yet            | Not chosen yet            |
| What the page should help them decide | Not chosen yet            | Not chosen yet            |
| Evidence or assumption                | Assumption; not validated | Assumption; not validated |

## Early brand brief

| Decision                                 | Agreement      |
| ---------------------------------------- | -------------- |
| Brand name                               | Not chosen yet |
| One-sentence promise                     | Not chosen yet |
| Primary archetype: the brand's character | Not chosen yet |
| Three voice traits                       | Not chosen yet |
| One example line in this voice           | Not chosen yet |
| Learner's predicted audience effect      | Not chosen yet |

## Visual decision

Compare two small hero previews before building the whole page. Hold the product, headline, supporting copy, and action identical. Use specific real design references and annotate visual choices, intended effect, and risk.

A simple original SVG wordmark is enough. Show small-size and one-color presentations; they may use the same asset when it works.

| Item                                              | Agreement or evidence |
| ------------------------------------------------- | --------------------- |
| Shared headline / support / action                | Not chosen yet        |
| Modernist preview, reference, and annotations     | Not chosen yet        |
| Postmodernist preview, reference, and annotations | Not chosen yet        |
| Chosen direction and reason                       | Not chosen yet        |
| Original SVG logo                                 | Not chosen yet        |
| Monochrome and small-size variants                | Not chosen yet        |
| Logo review at actual use size                    | Not checked yet       |
| Shared palette, typography, spacing, and assets   | Not chosen yet        |

## Ethical persuasion

Choose two applications that help the visitor make a voluntary, informed decision. Record their real implementation and mechanism rather than a principle name alone. Required size selection or validation alone does not establish consistency. Do not invent social proof, scarcity, authority, or product facts.

| Principle      | Actual copy or interaction | Visitor benefit / factual support |
| -------------- | -------------------------- | --------------------------------- |
| Not chosen yet | Not chosen yet             | Not chosen yet                    |
| Not chosen yet | Not chosen yet             | Not chosen yet                    |

## BRAND-001 — first branded storefront and live style guide

**Scope:** turn the working neutral storefront into the chosen brand's first coherent page. Keep the existing size selector and demo bag usable. Do not add checkout or all future features.

Keep when:

- The learner has chosen the audience hypotheses, brief, visual direction, and logo; the page visibly expresses those choices.
- Two annotated hero directions compare modernist/postmodernist thinking with the same content and real source links.
- The selected SVG logo works at small size and in one color; the presentations may share one asset.
- The storefront and live style guide share CSS variables, typography, components, and assets; they do not drift into separate identities.
- Two ethical persuasion applications are visible and their claims are supportable.
- Prepared checks pass, the agent has reviewed the slice and discussed one actual check, and the learner has reported a browser impression plus keyboard/mobile observations.
- The issue, branch, commit, and PR explain this feature in the learner's repository; agreed decisions and actual evidence are saved here. The learner has approved keeping and merging the change, and the merge into `main` is verified. Publishing is a separate choice.

## Evidence

Write a short result and link only evidence that exists. A passing browser check is evidence for its assertions, not customer research or proof of full accessibility.

| Spec ID   | Files           | Issue / PR      | Actual checks and observations            |
| --------- | --------------- | --------------- | ----------------------------------------- |
| BRAND-001 | public/brand.json | feature/BRAND-001 | npm run check passed; Null Variable identity rendered on studio and storefront |

## Later

No follow-up is selected. After keeping `BRAND-001`, choose one next cycle: perhaps a brand story, a supported fit guide, or richer demo-bag behavior. Agree its scope and add one new spec ID at that time.

## Plan


### Audience and brand
- **Audience:** Developers and minimalists looking for clean, straightforward apparel without marketing fluff.
- **Need and promise:** Shoppers need clear fit information and a streamlined purchasing experience before ordering. We will help them compare sizes easily and understand what their demo order includes.
- **Archetype and voice:** Technical, Minimalist; precise, transparent, modern.
- **Visual direction:** [styleguide.html](https://github.com/nsmadda11-alt/White-T-Shirt/blob/feature/career-research/public/styleguide.html) — Monochrome UI elements and clean typography adapted from developer design systems to maintain a distraction-free aesthetic.
- **Honest persuasion:** Standard garment measurements and clear frontend architecture. Limits: No claims of miracle fabrics, proprietary cotton tech, or unverified comfort metrics.

### Two approaches to the fit question
Both approaches use the same white T-shirt, product facts, price, size choices, and simulated checkout.

- **A — Size guide first:** Show the product, price, size guide, and size choices together.
- **B — Fit explanation first:** Show a short fit explanation, then the same product and shopping controls.
- **Comparison:** Ask a peer to find the fit information, choose a size, review the order, and complete the demo checkout in each version. Record where they hesitate or ask questions. Keep the offer and wording steady; note that the order of information changes.

### User stories, features, and checks

Ask your classmate to choose one story from your plan and explain how they would check that it works.

1. **As a shopper unsure about fit, I want to find the size guide so I can make an informed size choice.**  
   Feature: Size guide linked to the product.  
   Check: A peer can find it, use its listed measurements, and select a size. The guide must describe only information we can support.

2. **As a shopper, I want to choose a size and quantity so I can build my demo order.**  
   Feature: Size selector and quantity control (`shop.js`).  
   Check: Changing either control updates the order summary correctly.

3. **As a shopper, I want to review the quantity and total so I know what the demo order includes.**  
   Feature: Order summary with item, size, quantity, and total.  
   Check: With a size selected and quantity 2, the summary shows that size and twice the unit price.

4. **As a shopper, I want to submit a simulated order so I can see what checkout would do.**  
   Feature: Demo checkout with required fields and clear errors.  
   Check: Missing required information shows an error. Valid information produces a confirmation. No real payment is taken.

5. **As a shopper, I want my demo order saved so I can confirm it was recorded.**  
   Feature: Working SQLite backend.  
   Check: Complete a valid simulated order, confirm it appears in SQLite, close and reopen the app, and confirm the record remains.

### Scope and status
- **Included:** One plain white T-shirt, Null Variable developer branding, the two fit-information approaches, size and quantity selection, order summary, simulated checkout, and SQLite order storage.
- **Not claimed:** Real payment, real order fulfillment, or unsupported claims about fit, materials, delivery, or popularity.
- **Status:** Planned; checks to be run during implementation.
