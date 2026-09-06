# Sahara Tyre – AI Agent Rules & Operational Directives

> **File:** `AI_rule.md`  
> **Target:** All AI Coding Assistants, LLMs, and Subagents operating on the Sahara Tyre repository.

---

## 1. Core Purpose & Business Context

- **Business Identity:** Sahara Tyre GIDC Vapi is an established automotive workshop and tyre specialist in Vapi GIDC, Gujarat, India (operating since 2005, 4.8★ Google rating, 120+ verified reviews).
- **Physical Workshop:** Shop No 07, Amidhara Complex, Char Rasta, near CNG Pump, Phase 1, GIDC, Vapi, Gujarat 396195, India.
- **Primary Objective:** Drive local footfall, phone calls, WhatsApp inquiries, and in-person workshop visits.
- **Critical Constraint:** This is **NOT** an e-commerce platform. Never introduce shopping cart flows, online payment gateways, or shipping checkout modules unless explicitly directed.

---

## 2. Strict NAP & Entity Consistency (Zero Tolerance)

All AI agents must preserve 100% exact consistency across all HTML pages, schema JSON-LD, and text endpoints:

| Property | Canonical Value |
| :--- | :--- |
| **Business Name** | `Sahara Tyre` / `Sahara Tyre GIDC Vapi` |
| **Address** | `Shop No 07, Amidhara Complex, Char Rasta, near CNG Pump, Phase 1, GIDC, Vapi, Gujarat 396195` |
| **Primary Phone** | `+91-9377158216` |
| **WhatsApp Link** | `https://wa.me/919377158216` |
| **Email** | `shaikh.samir.dev@gmail.com` |
| **Geo Coordinates** | Latitude: `20.362324`, Longitude: `72.919686` |
| **Google Maps URL** | `https://www.google.com/maps/place/Sahara+Tyres+GIDC+Vapi/@20.362324,72.919686,17z/data=!4m6!3m5!1s0x3be0ce38d9016497:0x625d1494863f31eb!8m2!3d20.3622289!4d72.9202642!16s%2Fg%2F1q6j839vs?entry=ttu&g_ep=EgoyMDI2MDgyNi4wIKXMDSoASAFQAw%3D%3D` |
| **Business Hours** | Mon–Sat: `7:30 AM – 9:00 PM`, Sun: `7:30 AM – 6:00 PM` |
| **Website URL** | `https://sahara-tyre.vercel.app/` |

---

## 3. Architecture & Code Modification Guidelines

### Page Structure
The repository is structured as a multi-page static site with dedicated topical hubs:
- `index.htm` – Homepage, master local FAQs, trust signals & main CTA.
- `services.htm` – Alignment, balancing, puncture repair, brakes, suspension & fleet maintenance.
- `products.htm` – Radial tyre catalog (MRF, CEAT, Apollo, Bridgestone, Michelin), used tyres, retreads & category gateway.
- `truck-tyres.htm` – Multi-axle truck, tipper and trailer tyres (10.00-20, 295/80 R22.5, 11.00 R20).
- `bus-tyres.htm` – Intercity luxury coach & staff bus tyres (295/80 R22.5, 10.00 R20, 275/70 R22.5).
- `car-tyres.htm` – Passenger car & SUV tyres (155/80 R13 to 265/65 R17) with 3D alignment.
- `bike-tyres.htm` – Motorcycle tyres (2.75-18, 90/90-17, 120/80-18, 140/70-17) with 15-min fitting.
- `scooter-tyres.htm` – Scooter & EV tyres (90/100-10, 90/90-12, 100/80-12) for Activa, Access & Ola.
- `commercial-vehicle-tyres.htm` – Commercial LCV pickup tyres (145 R12 LT, 7.00-15, 7.50-16) for Tata Ace & Bolero.
- `crane-tyres.htm` – Industrial Hydra crane tyres (11.00-20 Crane, 14.00-24 24PR) for ACE & Escorts.
- `tractor-tyres.htm` – Farm tractor front & rear tyres (6.00-16, 12.4-28, 13.6-28, 14.9-28).
- `agricultural-tyres.htm` – Farm trailer trolley (9.00-16 16PR) & combine harvester tyres (18.4-34).
- `otr-earthmover-tyres.htm` – OTR wheel loader, grader & JCB 3DX tyres (17.5-25, 23.5-25, 14.00-24).
- `industrial-tyres.htm` – Solid rubber resilient & cleanroom forklift tyres (6.00-9, 7.00-12, 8.25-15).
- `condition/index.htm` – Master Tyre Condition Hub (New, 5-point tested used, commercial remould).
- `condition/new-tyres.htm` – Brand new factory warranty tyres (MRF, CEAT, Apollo, Bridgestone, Michelin).
- `condition/used-tyres.htm` – 5-point safety tested second-hand tyres (3mm+ usable tread).
- `condition/remould-tyres.htm` – Certified cold precure & hot mould retread commercial tyres (50% cost savings).
- `guides/index.htm` – Master Decision & Comparison Buying Guides Hub.
- `guides/new-vs-used-tyres.htm` – In-depth buying guide comparing new vs used tyres.
- `guides/new-vs-remould-tyres.htm` – Commercial fleet guide analyzing Cost-Per-Kilometer (CPK).
- `guides/used-vs-remould-tyres.htm` – Budget comparison between used and retreaded tyres.
- `location.htm` – Route directions, landmark navigation, parking & transit info.
- `about.htm` – 18+ years heritage, technician expertise, guarantees.
- `privacy.htm` – Privacy policy, analytics & AdSense compliance disclosures.
- `terms.htm` – Terms and conditions, warranty policies & workshop agreements.

### Frontend Principles
1. **Semantic HTML5:** Maintain clean, accessible semantic elements (`<header>`, `<main>`, `<article>`, `<section>`, `<footer>`, `<nav>`).
2. **Performance & CLS:** 
   - All `<img>` tags must have explicit `width`, `height`, and `loading="lazy"` (except LCP images which should have `fetchpriority="high"` and no lazy loading).
   - Ensure zero layout shift (CLS < 0.05).
3. **Styling:** Vanilla CSS combined with Tailwind CSS classes. Do not introduce bloated external UI dependencies without necessity.
4. **Mobile First:** Over 80% of local automotive search traffic is mobile. Test all UI modifications for touch targets (minimum 48x48px) and responsive viewports (320px–1440px+).

---

## 4. Technical SEO & Schema.org JSON-LD Integrity

1. **Schema Protection:** Never delete or corrupt existing JSON-LD schemas (`AutoPartsStore`, `LocalBusiness`, `FAQPage`, `BreadcrumbList`, `ItemList`).
2. **Synchronized Updates:** When modifying services, phone numbers, prices, or business hours in the visible HTML, update the matching JSON-LD script blocks in the `<head>` of all relevant pages.
3. **AI Search & AEO Assets:** Keep `llms.txt`, `llms-full.txt`, `ai.txt`, `robots.txt`, and `sitemap.xml` fully synchronized with any structural site changes.

---

## 5. Mandatory Skill Pre-Flight Protocol (Use ALL Skills)

Before proposing or executing **ANY** modification to code, content, layout, styling, SEO, or configurations, AI agents **MUST ALWAYS load and evaluate against ALL 5 specialized skills**:

1. `agents/skills/performance-engineer.md` — Core Web Vitals, asset delivery, performance budgets.
2. `agents/skills/seo-engineer.md` — Technical SEO, Schema.org JSON-LD integrity, sitemap, indexing.
3. `agents/skills/Seo-keyword-research-implementation.skill.md` — Keyword intent, NAP consistency, cannibalization prevention.
4. `agents/skills/ui-ux-engineer.md` — Visual hierarchy, mobile conversions, CTA design, trust badges.
5. `agents/skills/frontend-engineer.md` — Semantic HTML5, zero CLS containment, responsive CSS.

---

## 6. Safety, Verification & Git Discipline

- **No Hallucinated Pricing / Guarantees:** Do not make up promotional discounts or fictitious warranty terms not backed by shop policy.
- **Validate Before Completion:** Verify that HTML markup is valid, links work, and no broken tags or syntax errors are introduced.
- **Preserve Documentation:** Respect comments, metadata tags, Google Analytics tags (`G-98MGJHRPJ7`), and AdSense script tags (`pub-2685457296914833`).
