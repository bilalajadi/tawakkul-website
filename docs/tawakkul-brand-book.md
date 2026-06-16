# Tawakkul Education — Brand Book

*Last updated: 16-06-2026 · Derived from the live website and stakeholder sessions*

---

## 1. Brand Essence

**Purposeful. Complete. Personal.**

Tawakkul Education presents as a premium British governess agency — not a school, not a tutoring service. Every visual and verbal choice should reinforce this: refined, warm, discreet, excellent.

---

## 2. Colour Palette

All colours are defined as CSS custom properties in the website. Use these exact values across all materials.

### Primary Palette

| Name | Hex | CSS Variable | Usage |
|---|---|---|---|
| Cream (background) | `#FAF7F2` | `--bg` | Page background, light sections |
| Sand | `#F0E8D8` | `--sand` | Section backgrounds, cards |
| Espresso (deep dark) | `#2A2118` | `--espresso` | Hero overlays, footer, dark sections |
| Dark | `#1C1814` | `--dark` | Headings, deep text |
| Body text | `#3D3028` | `--text` | Body copy |
| Mid brown | `#4A3A2C` | `--mid` | Subheadings, secondary text |
| Border | `#E0D5C5` | `--border` | Dividers, card borders |

### Accent Palette

| Name | Hex | CSS Variable | Usage |
|---|---|---|---|
| Gold | `#E2C08D` | `--gold` | Highlights, labels, accents, trust strip |
| Gold dark | `#C9A05A` | `--gold-dk` | Hover states, borders on gold elements |

### Colour Rules
- **Never** use pure black (`#000000`) — always use `--dark` or `--espresso`
- **Never** use pure white as text over a light background — use `--text` or `--mid`
- Dark sections (footer, hadith band) use `--espresso` or `--dark` as background with cream/gold text
- Gold is an accent only — not a background for large areas
- Photo overlays use `rgba(42, 33, 24, 0.XX)` — the espresso tone, not a generic black

---

## 3. Typography

### Font Families

| Role | Font | CSS Variable | Fallback |
|---|---|---|---|
| Display (headings, pull quotes) | Fraunces | `--display` | Georgia, serif |
| Serif (body headings, nav) | Cormorant Garamond | `--serif` | Georgia, serif |
| Sans-serif (body copy, UI) | Lato | `--sans` | sans-serif |

All fonts loaded via Google Fonts. Import order: Fraunces → Cormorant Garamond → Lato.

### Type Scale

| Element | Font | Size | Weight | Notes |
|---|---|---|---|---|
| Hero headline (h1) | Fraunces | `clamp(2.8rem, 6vw, 5.2rem)` | 300 | Fluid, light weight |
| Section headline (h2) | Fraunces | `clamp(2rem, 4vw, 3rem)` | 300–400 | |
| Subheading (h3) | Cormorant Garamond | `1.2–1.4rem` | 600 | Often in gold |
| Body copy | Lato | `1rem` (16px base) | 300–400 | Line height 1.7–1.9 |
| Small labels / captions | Lato | `0.75–0.85rem` | 400–700 | Uppercase tracking |
| Nav links | Lato | `0.85rem` | 400 | Letter spacing 0.05em |
| CTA buttons | Lato | `0.85rem` | 700 | Uppercase, tracking |
| Pull quotes / ethos | Fraunces or Cormorant Garamond | `1.5–2rem` | 300 | Italic, centred |

### Typography Rules
- Headings are always light weight (300) for elegance — avoid bold headings
- Body copy uses Lato 300 (light) for a refined feel, not 400 (regular)
- Gold accents (`--gold`) are used for labels above headings (e.g. "Our Foundation")
- Italics are used sparingly — for pull quotes and founder emphasis only
- Letter spacing (`0.1–0.15em`) is applied to uppercase labels and nav links

---

## 4. Logo

### Versions
| Version | File | Usage | Size |
|---|---|---|---|
| Tree icon only | `Logo/images.png` | Navigation bar, favicon | 38px height in nav |
| Full shield crest | `Logo/0x0.png` | Footer | 80px height in footer |

### Logo Rules
- Always display on a light background or with sufficient contrast
- Do not recolour or stretch the logo
- Minimum clear space: equal to the height of the "T" in the wordmark on all sides
- Favicon: use the tree icon PNG (`Logo/images.png`)

### Logo + Wordmark
The nav combines the tree icon with the text "Tawakkul **Education**" — the word "Education" is italicised or styled differently to the brand name.

---

## 5. Imagery

### Style
All photography follows the **governess/butler agency** principle: **no faces**. Leave the subject to the imagination. The story is told through hands, objects, environments, textures.

### The Story to Tell
*Elite governess education for Muslim teenagers* — conveyed through:
- Hands writing, turning pages, holding books
- Leather-bound notebooks, fountain pens, quality stationery
- Warm interior light — libraries, desks, window light
- Nature and calm outdoor scenes (farm, countryside, open skies)
- Textures: linen, wood grain, aged paper, leather

### What to Avoid
- Faces (any age, any ethnicity)
- Generic stock photos of classrooms or computers
- AI-generated images
- Anything cold, clinical, or corporate
- Bright saturated colours inconsistent with the warm palette

### Photo Overlay Treatment
All hero/feature photos use a layered CSS gradient overlay in the espresso tone:
```css
background:
  linear-gradient(160deg, rgba(42,33,24,.68) 0%, rgba(42,33,24,.38) 50%, rgba(42,33,24,.62) 100%),
  url('images/photo.jpg') center center / cover no-repeat;
```
Adjust opacity values to suit readability of overlaid text. Text over photos must always have `text-shadow: 0 1px 12px rgba(0,0,0,.55)`.

### Current Photo Library (in `/images/`)
| File | Used in | Subject |
|---|---|---|
| `tushar-ranjan-seth-GqpGd6NtUoI-unsplash.jpg` | Homepage hero | Warm atmospheric scene |
| `evgeni-tcherkasski-ksu_65duslc-unsplash.jpg` | About intro / Referral tier 1 | Calm, natural |
| `jan-kahanek-g3O5ZtRk2E4-unsplash.jpg` | Programme section | Writing/desk |
| `allen-y-Y5hiuHgRTus-unsplash.jpg` | About page founder | Leather bag (placeholder) |
| `arnel-hasanovic-MNd-Rka1o0Q-unsplash.jpg` | About journey section | Natural scene |
| `tushar-ranjan-seth-eIhFwKh20zY-unsplash.jpg` | Services intro | Warm tone |
| `fabian-centeno-7osiV1AFIF8-unsplash.jpg` | Services hadith section | Dark, atmospheric |
| `alexander-zezegov-gMSx6QvKIlc-unsplash.jpg` | Referral tier 2 | Turkey farm retreat |

---

## 6. Spacing & Layout

### Container
- Max width: `1200px` (`--max`)
- Horizontal padding: `clamp(1.5rem, 5vw, 4rem)` (`--pad`)

### Section Rhythm
- Section padding: `5rem 0` (desktop), `3.5rem 0` (mobile)
- Between sections: consistent breathing room — no cramming
- Grid gaps: `3–4rem` (two-column layouts)

### Grid Patterns
- Two-column (text + photo): `1fr 1fr` on desktop, stacked on mobile
- Feature cards: `repeat(auto-fit, minmax(260px, 1fr))`
- Trust strip / stats: `repeat(4, 1fr)` on desktop

---

## 7. Components

### CTA Buttons
```css
Primary: background --gold-dk, text --espresso, uppercase, 0.1em tracking, 0.85rem Lato 700
Hover: background --gold, slight lift (translateY -2px)
Secondary (outline): border --gold-dk, text --espresso
```

### Cards (Pillars, Services)
- Background: `--bg` or `--sand`
- Left border accent: `3px solid --gold`
- Subtle shadow on hover
- Heading in `--serif` or `--display`

### Dark Bands (Hadith, Footer)
- Background: `--espresso` or `--dark`
- Text: `rgba(255,255,255,0.9)` for body, `--gold` for accents
- Used sparingly — maximum 2 dark sections per page

### Testimonials
- Light section background (`--bg`)
- Quote text: `--text` (dark enough to read comfortably)
- Quote marks: large, in `--gold`, decorative
- Attribution: small, `--mid`, light weight

---

## 8. Tone of Voice

### Personality
Warm but authoritative. Like a trusted, highly educated family friend — not a salesperson, not a corporation.

### Voice Characteristics
| Characteristic | Example |
|---|---|
| Confident, not boastful | "Built around your child" not "The best education available" |
| Personal, not corporate | "Your family" not "Our clients" |
| Elevated, not stuffy | "Purposeful and complete" not "Optimised outcomes" |
| Islamic, not performative | Natural reference to values, not performative signalling |

### Sentence Style
- Short, declarative sentences for impact
- Rhetorical questions to draw the reader in ("Are you ready to build an education your child will thrive in?")
- Em dashes for elegant asides — like this
- Avoid exclamation marks
- Avoid buzzwords: "innovative", "world-class", "game-changing"

---

## 9. Navigation Structure

| Link | Status |
|---|---|
| Services | Active |
| About | Active |
| Referral | Hidden (not in nav — page saved but not linked) |
| FAQ | Anchor link on homepage |
| Book a Free Call | Primary CTA — links to Calendly |

**Calendly link:** `https://calendly.com/tawakkuleducation/free-call?month=2026-05`

---

## 10. Versioning

Website versions are saved in `/versions/` before each round of significant edits.

| Version | Folder | Date | Notes |
|---|---|---|---|
| v1 | `versions/v1-pre-june16/` | 16-06-2026 | Pre-feedback state — all 4 pages |

---

*This brand book should be treated as a living document. Update it when design decisions are made, confirmed, or changed.*
