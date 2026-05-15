# VedaDB Investor Pitch Deck - Visual Design Document

## 1. Profile Baseline Declaration

- **Profile selection**: `profiles/strategic.md`
- **Selection rationale**: This is a fundraising pitch deck for VedaDB (a pre-launch multi-model database startup) targeting investors and VCs. The strategic profile is designed for project proposals, business plans, fundraising pitch decks, and investment proposals.
- **Referenced dimensions**: Design philosophy (grand vision, data persuasiveness, premium feel, returns-oriented), information density (medium-high), color guidance (steady premium deep tones), font guidance (sans-serif bold titles), content page layouts (big numbers, left-right columns, timeline), narrative style (fundraising framework: Problem -> Solution -> Product -> Market -> Business Model -> Competitive Advantage -> Team -> Financials -> Ask), content expression techniques (TAM/SAM/SOM, competitive matrix, milestone roadmap, unit economics).
- **Deviation notes**: 
  - Slightly more tech-forward visual language than a typical consulting strategic report, to match the database/AI infrastructure domain
  - Using a darker palette for key data pages (market size, traction) to create dramatic visual impact
  - Information density kept at medium (65-80%) rather than high, since this is pre-launch and content is more visionary

## 2. Style Baseline Declaration

- **Style anchor selection**:
  1. **CockroachDB / MongoDB brand design**: Reference the dark, bold, geometric visual language of modern database startups — sharp corners, strong typography, high contrast between dark hero sections and clean white content sections
  2. **Stripe's brand aesthetic**: Reference Stripe's precision, restraint, and premium tech feel — generous whitespace, subtle grid systems, confident typography hierarchy, and restrained color palette
  3. **Sequoia Capital pitch deck style**: Reference the clarity and data-forward approach of classic VC pitch decks — one argument per slide, prominent numbers, clean charts
- **Referenced dimension explanation**:
  - From CockroachDB/MongoDB: Color palette (dark navy backgrounds with bright accent), geometric precision, tech authority
  - From Stripe: Whitespace usage, typographic hierarchy, premium restraint, layout grid discipline
  - From Sequoia: Content structure (Problem -> Solution -> Market -> Ask), data prominence, investor-friendly framing

## 3. Style Details

### Color Design Principles
- **Color tendency**: Striking & bold — this is a startup pitch deck that needs to stand out and convey energy and ambition, while maintaining professional credibility
- **Temperature**: Cool — database infrastructure is a cool-toned domain; deep blues convey trust, depth, and technical authority
- **Primary color**: Deep Navy `#0B1426` — dark, authoritative, technical. Used for dark page backgrounds, key section headers
- **Background**: Light `#F5F5F0` — warm paper-like off-white for content pages. Avoids sterile pure white, adds premium warmth
- **Dark background**: `#0B1426` — used for cover, chapter transitions, market size pages, final page
- **Text color (light bg)**: `#1A1A2E` — near-black with slight blue undertone for readability
- **Text color (dark bg)**: `#FFFFFF` — pure white on dark backgrounds
- **Secondary**: `#475569` — slate gray for annotations, secondary text, dividers
- **Accent**: `#C8A45C` — muted gold/amber for key numbers, CTAs, highlights. Premium feel without being flashy. Used sparingly
- **Muted accent**: `#1E3A5F` — lighter navy for subtle backgrounds, cards, table headers

### Font Usage Principles
- **Title font**: `Liter` — modern neo-grotesque, clean and rational. ALL CAPS with expanded letter-spacing for cover and chapter titles. Bold weight for page titles
- **Body font**: `QuattrocentoSans` — classic elegant sans-serif, highly readable, clear at small sizes
- **Font size hierarchy**:
  - Cover title: 48-52px
  - Page title: 30-34px
  - Body text: 20px (moderate density pages)
  - Big numbers: 52-60px
  - Annotations/source: 13-14px
  - Subtitle: 22-24px

### Text Box and Container Styles
- Content separation: Prioritize whitespace + font size hierarchy over structural cards
- When cards are used: Sharp corners (0px border-radius), thin 1px borders in `#E0E0E0` or filled with `#1E3A5F` (muted navy)
- Decorative elements: Thin horizontal accent lines in gold `#C8A45C` (2px) used as section dividers; small gold squares as bullet decorators
- No rounded rectangles unless absolutely necessary

### Image Style
- **Icons**: Solid icons, used sparingly for product feature cards and competitive matrix. Restrained usage — only when icons add clarity
- **Tables**: Minimal three-line style. Header row in `#0B1426` with white text, body rows alternating `#FFFFFF` and `#F5F5F0`. Thin borders in `#E0E0E0`
- **Charts**: Minimal style, monochrome with navy family. Single accent color (gold) for the VedaDB data series. Clean gridlines, no 3D effects
- **Illustrations**: Dark, abstract, tech-oriented imagery for cover/chapter pages — think data visualization art, network topologies, geometric abstractions. High contrast, limited color palette

## 4. Layout System

### Global Layout Characteristics
- **Canvas**: 1280 x 720px (16:9)
- **Page margins**: 60px left/right, 50px top/bottom
- **Unified elements across pages**:
  - Top-left: Small "VEDADB" logotype (12px, Liter, gold color) on content pages
  - Bottom-right: Page number (13px, QuattrocentoSans, secondary gray)
  - Bottom-left: Thin gold accent line (40px wide, 2px height) as brand mark
- **Grid**: 12-column grid, consistent alignment

### Special Page Layouts
- **Cover**: Hero design — full dark navy background (`#0B1426`), large gold title centered, subtitle in white below, thin gold horizontal line separating title and subtitle. No image — typography-focused
- **Table of Contents**: Grid layout — 6 chapters arranged in 2 rows x 3 columns on off-white background. Each chapter: large number in gold + chapter title in navy
- **Chapter transitions**: Dark navy background, large semi-transparent chapter number (120px, 10% opacity white), chapter title in gold, one-line subtitle in white. Minimal, dramatic
- **Closing page**: Dark navy background, centered "THANK YOU" in gold, contact info below in white, thin gold line separator

### Content Page Layout Patterns
- **Pattern A - Big Numbers**: Dark background, 3 big numbers in gold across the page, supporting text below each. For market size, traction pages
- **Pattern B - Left-Right Split**: Left 50% text content, Right 50% chart/image. For product, architecture pages
- **Pattern C - Three Cards**: Three equal-width vertical cards with icons, titles, and descriptions. For features, competitive advantages
- **Pattern D - Timeline**: Horizontal timeline with milestones. For roadmap, financial projections
- **Pattern E - Full Table/Chart**: Page dominated by a table or chart with title above. For competitive matrix, financial data

## 5. Style Usage Rules

- `title`: Used for page titles on content pages (30px, navy, Liter)
- `subtitle`: Used for subtitles and secondary headings (22px, slate gray, QuattrocentoSans)
- `body`: Used for all body text on content pages (20px, near-black, QuattrocentoSans, 1.6 line height)
- `bigNumber`: Used for prominent statistics and KPIs (56px, gold, Liter)
- `caption`: Used for annotations, sources, page numbers (13px, slate gray, QuattrocentoSans)
- `coverTitle`: Used for cover page title (52px, gold, Liter, ALL CAPS)
- `coverSubtitle`: Used for cover page subtitle (24px, white, QuattrocentoSans)
- `chapterTitle`: Used for chapter transition titles (40px, gold, Liter)
- `chapterNumber`: Used for large chapter numbers (120px, 10% opacity white, Liter)
- Colors: `$primary` (navy) for dark backgrounds, titles on light pages; `$accent` (gold) for key numbers, highlights, CTAs; `$background` (off-white) for content page backgrounds; `$text` (near-black) for body text; `$secondary` (slate) for annotations
- Table style: `default` table style with navy header, alternating light rows

## 6. Risk Prohibitions

- [ ] **NO purple/gradient/purple-blue combinations** — AI-typical color schemes destroy the premium tech feel
- [ ] **NO rounded rectangles** — Sharp corners only, to convey precision and technical authority
- [ ] **NO generic stock photos** — Use abstract tech imagery or skip images entirely; quality over decoration
- [ ] **NO unsupported claims without data** — Every market claim must have a source annotation
- [ ] **NO long text paragraphs** — Bullet points only, max 3-4 lines per point
- [ ] **NO overly flashy visual decoration** — Clean, steady, static display
- [ ] **NO body text below 18px** — Minimum 20px for body, 13px for annotations only
- [ ] **NO more than 3 colors** on any single page — Navy, gold, white/gray only
- [ ] **NO vague competitive analysis** — Specific metric comparison required
- [ ] **NO returns described only qualitatively** — Quantified figures (ROI, growth rate, market size)

## 7. Theme Definition

```yaml
theme:
  colors:
    primary: "#0B1426"
    secondary: "#475569"
    accent: "#C8A45C"
    background: "#F5F5F0"
    text: "#1A1A2E"
    light: "#FFFFFF"
    muted: "#1E3A5F"
    border: "#E0E0E0"
  textStyles:
    title:
      fontSize: 32
      color: "$primary"
      fontFamily: "Liter"
    subtitle:
      fontSize: 22
      color: "$secondary"
      fontFamily: "QuattrocentoSans"
    body:
      fontSize: 20
      color: "$text"
      fontFamily: "QuattrocentoSans"
      lineHeight: 1.6
    bigNumber:
      fontSize: 56
      color: "$accent"
      fontFamily: "Liter"
    caption:
      fontSize: 13
      color: "$secondary"
      fontFamily: "QuattrocentoSans"
    coverTitle:
      fontSize: 52
      color: "$accent"
      fontFamily: "Liter"
    coverSubtitle:
      fontSize: 24
      color: "$light"
      fontFamily: "QuattrocentoSans"
    chapterTitle:
      fontSize: 40
      color: "$accent"
      fontFamily: "Liter"
    chapterNumber:
      fontSize: 120
      color: "#FFFFFF1A"
      fontFamily: "Liter"
  tableStyles:
    default:
      fontSize: 16
      fontFamily: "QuattrocentoSans"
      headerFill: "$primary"
      headerColor: "$light"
      headerBold: true
      bodyFill: ["$light", "$background"]
      bodyColor: "$text"
      border:
        style: solid
        width: 1
        color: "$border"
```
