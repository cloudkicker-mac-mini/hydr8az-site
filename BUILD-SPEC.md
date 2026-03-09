# HYDR8AZ Website Build Spec

## Goal
Build a complete static website for HYDR8AZ IVs & MedSpa. We already have the homepage at index.html. Build ALL remaining pages.

## Source of Truth
ALL content must be scraped from https://www.hydr8az.net/ — do NOT make up any content. Every page, every service description, every detail must come from their existing site.

## Tech Stack
- HTML5 + Tailwind CSS (via CDN: https://cdn.tailwindcss.com)
- Vanilla JavaScript
- Same Tailwind config as index.html (copy the tailwind.config block)
- Same fonts: Open Sans + Playfair Display
- Same color scheme: primary purple #6565E5, dark #222222, surface #F7F7F7, coral #E67373

## File Structure
```
index.html (DONE - don't modify)
about.html
contact.html
help-me-choose.html
iv-therapy-options.html (listing page)
iv-therapy-options/
  acceler8-athletic-performance.html
  afterburn-sunburn.html
  allevi8-pms-menopause.html
  alpha-lipoic-acid-iv.html
  amino-acids.html
  boost-energy-detox.html
  concentr8-brain-fog.html
  dexamethasone-iv.html
  dicip8-anxiety.html
  eradic8-bundle.html
  everything-under-the-sun.html
  gr8-xpress-myers-iv.html
  glutathione.html
  hangover-relief.html
  high-dose-vitamin-c.html
  immunity-boost.html
  jet-lag.html
  libido-boost--his-hers.html
  lr-1-l.html
  magnesium-chloride-iv.html
  migraine-elimin8.html
  mommy-2-b.html
  myers-cocktail.html
  nad.html
  quench-rehydration.html
  rejuven8.html
  tummy-trouble.html
injections-iv-add-ins.html
services/
  alma-accent-prime-body-contouring-skin-tightening.html
  alma-lmnt.html
  alma-opus-plasma-skin-rejuvenation.html
  cbd-professional-skincare-line.html
  lmnt-electrolyte-packet.html
  opus-colibri-eye-lift-lesion-removal.html
  patchaid-vitamin-patches.html
  resurface-rf-skin-resurfacing.html
  sauna-detox-slimming-wrap.html
  targeted-led-light-therapy.html
  vacuum-therapy-booty-breast-enhancement.html
  vibration-plate-for-circulation-muscle-stimulation.html
  wood-therapy-body-shaping.html
  yeso-therapy-body-wraps.html
privacy-policy.html
terms-conditions.html
```

## Page Templates

### Individual IV Therapy Page Template
Each IV therapy page should have:
1. Same nav as index.html
2. Hero section with treatment name
3. Description from the source site
4. Bullet point benefits (from source)
5. Key ingredients (from source)
6. "Book Now" CTA
7. Same footer as index.html

### Individual Service/MedSpa Page Template  
Same structure as IV therapy pages but for medspa services.

### IV Therapy Options Listing Page
Grid of all IV therapy options with cards linking to individual pages.

### About Page
Content from https://www.hydr8az.net/about — mission, vision, team info.

### Contact Page
Form layout with business info: address, phone, email, hours, map embed placeholder.

### Help Me Choose
Interactive guide from the source site content.

## CRITICAL RULES
1. SCRAPE content from https://www.hydr8az.net/{page} for EVERY page - use curl
2. Do NOT invent any service descriptions, benefits, or ingredients
3. Do NOT add services that don't exist on their site
4. All internal links must use relative paths (e.g., href="/iv-therapy-options/nad.html")
5. Use the HYDR8AZ text logo (not an image): <span class="text-2xl font-bold tracking-tight"><span class="text-hydr8-400">HYDR8</span><span class="text-hydr8-900">AZ</span></span>
6. Every page needs the same nav and footer as index.html
7. Images are in assets/images/ — reuse the existing ones
8. Phone number: (928) 733-7776
9. Address: 205 English Village, 1440 McCulloch Blvd N, Lake Havasu City, AZ 86403
10. Email: Hydr8AZ@gmail.com

## After Building
Run a link checker to verify NO broken internal links exist.
