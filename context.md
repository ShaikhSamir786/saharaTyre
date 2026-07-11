# Context – Sahara Tyre Website

## Purpose

This website exists to **drive local, in-person visits** to Sahara Tyre GIDC Vapi — a tyre shop and automotive workshop in Vapi GIDC, Gujarat, India (operating since 2005).

## Primary Goal

**Enhance local footfall** to the physical shop located at:
Shop No 07, Amidhara Complex, Char Rasta, near CNG Pump, Phase 1, GIDC, Vapi, Gujarat 396195, India

The website is NOT an e-commerce store. It does NOT sell tyres online. Its sole purpose is to:
- Make Sahara Tyre discoverable in **local search results** (Google, Bing, AI search)
- Provide essential business information (services, pricing, hours, location)
- Encourage visitors to **call, WhatsApp, or visit the shop directly**
- Establish trust through reviews, years of experience, and service quality

## Google Business Profile (GBP) Integration

This website is linked and used within the **Google Business Profile** account for Sahara Tyre. The GBP listing helps the shop appear in:

- **Google Maps** searches (e.g., "tyre shop near me", "puncture repair Vapi")
- **Local Pack** results (the top 3 map results in Google Search)
- **Google Business Profile** side panel with business details
- **"Directions" button** — users tap and navigate directly to the shop

### GBP–Website Synergy

| GBP Element | Website Connection |
|-------------|-------------------|
| Website URL | `https://sahara-tyre.vercel.app/` |
| Phone number | `+91-9377158216` (matches GBP listing) |
| Address | Exact match with GBP address |
| Business hours | Mon–Sat 7:30 AM – 9 PM, Sun 7:30 AM – 6 PM |
| Services | Full service list on website for deep-dive |
| Reviews | 4.8/5 rating (120+ reviews) displayed on website |
| Photos | Unsplash hero images (GBP should use real shop photos) |

### Key GBP Actions to Optimize

1. **Website link** → Points to `https://sahara-tyre.vercel.app/`
2. **"Call" button** → Triggers `tel:+919377158216`
3. **"Directions" button** → Opens Google Maps to coordinates `20.362324, 72.919686`
4. **"Message" / WhatsApp** → Opens `wa.me/919377158216`

## Target Audience

- **Local vehicle owners** in Vapi GIDC and surrounding areas (Gunjan, Chala, Daman, Silvassa)
- **Truck fleet owners** and logistics companies in the GIDC industrial zone
- **Daily commuters** needing emergency puncture repair or quick tyre services
- **Car, SUV, and commercial vehicle** owners in the Vapi region

## How the Website Achieves Local Visit Goals

### 1. Local SEO (Search Engine Optimization)
- **Geo-targeted meta tags**: `geo.region=IN-GJ`, coordinates embedded
- **Keywords**: Hundreds of "near me" and Vapi-specific keywords in meta tags
- **Structured data (JSON-LD)**: LocalBusiness schema with full address, geo coordinates, opening hours, aggregate rating
- **Sitemap + robots.txt**: Ensures search engines index the site
- **Open Graph / Twitter Cards**: Optimized for social sharing

### 2. AI Search Visibility (Forward-Thinking)
- `llms.txt` — Business profile formatted for AI/LLM consumption
- `.well-known/ai-plugin.json` — OpenAI-compatible plugin manifest
- `ai.txt` — Crawl policy and content restrictions for AI crawlers
- Custom AI meta tags for AI search engines

### 3. Conversion-Optimized Design
- **Sticky "Call Now" button** in navigation bar
- **Floating action buttons** (Call + WhatsApp) always visible on screen
- **Mobile bottom nav** with Call, WhatsApp, and Directions buttons
- **Contact form** that sends inquiries directly via WhatsApp (no backend needed)
- **Hero section** with clear CTA: "Call Now" + "WhatsApp"
- **Location section** with embedded Google Maps

### 4. Trust Building
- 18+ years of experience highlighted prominently
- 4.8/5 Google rating (120+ reviews) in structured data
- Customer testimonials displayed
- "Why Choose Us" section (Expertise, Transparent Pricing, Industrial Focus, 24/7 Emergency)
- Quality-tested used tyres guarantee

## Website Architecture

Single-file static site (`index.htm`, 1,254 lines) — no build steps, no backend, no JavaScript framework. Deployed on Vercel.

- **Styling**: Tailwind CSS via CDN
- **JavaScript**: Minimal inline script for WhatsApp form submission only
- **Images**: External (Unsplash hero backgrounds, SVG favicon)
- **Analytics**: Google Analytics 4 (`G-98MGJHRPJ7`)
- **Monetization**: Google AdSense (publisher `pub-2685457296914833`)

## Services Offered

| Service | Key Details |
|---------|-------------|
| New Tyre Sales | MRF, CEAT, Apollo, Bridgestone, etc. |
| Used Tyres | Quality-tested, satisfaction warranty |
| Remolded Tyres | Eco-friendly, safety inspected |
| Puncture Repair | 15–20 min typical repair |
| Wheel Alignment | Precision laser alignment |
| Tyre Balancing | Computerised balancing |
| Brake Inspection | Disc & drum brake pads/rotors |
| Suspension Check | Struts, shocks, steering |
| Truck Tyre Fitting | Heavy-duty commercial tyres |
| Tyre Exchange | Fair value for old tyres |
| Fleet Maintenance | Scheduled for GIDC companies |
| Vehicle Inspection | Complete wheel/steering check |
| Roadside Assistance | Emergency support near GIDC |
| Tread Inspection | Free safety check |

## Service Areas

Vapi GIDC (primary), Gunjan, Imran Nagar, Chala, Daman Road, Daman, Silvassa, and surrounding Gujarat regions.

## Business Hours

- **Monday – Saturday**: 7:30 AM – 9:00 PM
- **Sunday**: 7:30 AM – 6:00 PM

## Contact

- **Phone**: +91-9377158216
- **WhatsApp**: https://wa.me/919377158216
- **Email**: shaikh.samir.dev@gmail.com
- **Website**: https://sahara-tyre.vercel.app/

## Deployment

- **Platform**: Vercel (zero-config static hosting)
- **Build**: None (static files served as-is)
- **Domain**: `sahara-tyre.vercel.app`
- **Cache**: `no-cache` on `index.htm` (forces revalidation)

## Git History Focus

Recent commits show iterative improvements in:
1. SEO optimization (structured data, keywords, metadata)
2. Deployment configuration (Vercel rewrites, headers)
3. Content updates (FAQs, services, branding)
4. Ad integration (Google AdSense)
5. AI discovery files (llms.txt, ai.txt, ai-plugin.json)
