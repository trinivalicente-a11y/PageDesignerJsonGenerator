---
name: landing-page-json-generator
description: Generate a complete, beautiful event landing page JSON file for the Blackthorn Events page builder. Use this skill ANY TIME a user asks to generate, create, build, or fill in a landing page JSON, event layout JSON, or page builder JSON. Also trigger when they say things like "create a landing page for [event]", "generate the JSON for [event]", "build a page for this prospect", or paste event details and want a layout. The skill produces production-ready JSON that can be directly imported into the page builder. MANDATORY TRIGGERS: landing page JSON, event JSON, page builder JSON, generate layout, create event page, build landing page, prospect page, event layout.
---

# Landing Page JSON Generator — v2

## What this skill does

Given prospect/event information, generate a complete, production-ready JSON importable directly into the Blackthorn Events page builder. The JSON uses a `layout[]` → sections → columns → components hierarchy plus full `siteSettings`.

---

## Step 1 — Gather Input

**Required:**
- Event name
- Event date(s)
- Event location / venue name
- Short event description (2-4 sentences)
- Logo image URL (or `""`)

**Optional but improves quality significantly:**
- Brand primary color (hex)
- Brand secondary/accent color (hex)
- Background image or video URL (Cloudinary preferred)
- Event type — used to auto-select theme, font, palette
- Sections to include (speakers, schedule, FAQ, sponsors, countdown, etc.)
- CTA button label (default: "Register Now")
- Social media URLs
- Footer copyright text

---

## Step 2 — Select Theme, Font & Palette

Read `references/color-palettes.md` for full palette configs per event type.

### Theme Selection (32 available)

| Event Type | Best Theme | Runner-up |
|---|---|---|
| Tech / AI / Startup | `night` | `dim` |
| Medical / Academic / Research | `nord` | `corporate` |
| Music Festival / Entertainment | `synthwave` | `halloween` |
| Watch Party / Sports | `synthwave` | `retro` |
| Conference / Summit (professional) | `autumn` | `business` |
| University / Community / Alumni | `autumn` | `forest` |
| Gala / Awards / Luxury | `luxury` | `black` |
| Food & Wine / Lifestyle | `coffee` | `lemonade` |
| Kids / Family / Fun | `cupcake` | `pastel` |
| Creative / Design / Art | `cyberpunk` | `fantasy` |
| Wellness / Nature | `garden` | `emerald` |
| Finance / Corporate | `business` | `corporate` |

All available themes: `acid`, `aqua`, `autumn`, `black`, `bumblebee`, `business`, `cmyk`, `coffee`, `corporate`, `cupcake`, `cyberpunk`, `dark`, `dim`, `dracula`, `emerald`, `fantasy`, `forest`, `garden`, `halloween`, `lemonade`, `light`, `lofi`, `luxury`, `night`, `nord`, `pastel`, `retro`, `sunset`, `synthwave`, `valentine`, `winter`, `wireframe`

### Font Selection

| Event Type | Title Font | Body Font |
|---|---|---|
| Festival / Bold / Entertainment | `'Bebas Neue'` | `'Bebas Neue'` |
| Tech / Modern / Startup | `'Manrope'` | `'Manrope'` |
| Professional / Medical / Academic | `'Poppins'` | `'Poppins'` |
| Warm / Community / Alumni | `'Cabin'` | `'Cabin'` |
| Elegant / Gala / Luxury | `'Space Grotesk'` | `'Manrope'` |

Always include full font stack: e.g. `'Bebas Neue', system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif`

---

## Step 3 — Choose Sections

### Section order (standard full layout):
1. `header-section` — nav bar
2. `hero-section` — title, description, CTA (video or image background)
3. `sponsors-section` *(if sponsors available)*
4. `about-section` — event description with image
5. `info-cards-section` — "Why Attend" value props
6. `schedule-section` *(if sessions data available)*
7. `speakers-section` *(if speakers data available)*
8. `tickets-section` — ticket pricing
9. `faq-section` *(if FAQ data available)*
10. `countdown-cta-section` — countdown timer + register button
11. `footer-section`

### Minimum viable layout (no data):
Header → Hero → Info Cards → Tickets → CTA with Countdown → Footer

### Section layout patterns (from real examples):

- **Two-column about**: `67%` text column + `33%` image column
- **FAQ split**: `25%` title column + `75%` faq component column
- **Countdown split**: `25%` title+paragraph column + `75%` event-countdown column
- **Info cards with sidebar**: `25%` label+title column + `75%` info-cards column
- **Testimonials**: 3x `33%` columns, each with `image` + `info-cards`
- **Contact split**: `50%` contact-us + `50%` title/paragraph/icon-list

---

## Step 4 — Section Design Rules

### CRITICAL: Two-Title Heading Pattern
Every content section uses TWO title components, not one:
1. **Small label**: `fontSize: "1rem"`, ALL CAPS, primary/accent color, `enableGradientText: false`
2. **Large headline**: `fontSize: "2.5rem"`, sentence case, gradient text ON or body text color

```
[title]     "WHY ATTEND"           ← 1rem, primary color, no gradient
[title]     "Join the Future"      ← 2.5rem, gradient ON
[paragraph] body text...
[component]
```

### Background Rules
- **Hero/Header**: ALWAYS use background image or video. No URL = animated gradient (`gradientAnimation: true`)
- **Overlay**: `backgroundOverlayEnabled: true`, opacity `65-75` on ALL image/video backgrounds
- **Dark themes**: keep backgrounds consistently dark, vary with subtle gradients
- **Light themes** (`nord`, `autumn`): alternate transparent + image-backed sections
- **Never plain solid color on hero**

### Padding — always use `%` units on sections
- Hero/Header: `{top: "8%", left: "10%", right: "10%", bottom: "8%"}`
- Content sections: `{top: "10%", left: "10%", right: "10%", bottom: "10%"}`
- Compact sections (sponsors, countdown): `{top: "6%", left: "6%", right: "6%", bottom: "6%"}`
- Footer: `{top: "0px", left: "64px", right: "64px", bottom: "0px"}`
- Set `"paddingUnit": "%"` on every section

### Mobile Responsive Spacing
Every section MUST include:
```json
"responsiveSpacing": {
  "mobile": {
    "margin": {"top": "", "left": "", "right": "", "bottom": ""},
    "padding": {"top": "8%", "left": "8%", "right": "8%", "bottom": "8%"}
  },
  "tablet": {
    "margin": {"top": "", "left": "", "right": "", "bottom": ""},
    "padding": {"top": "8%", "left": "8%", "right": "8%", "bottom": "8%"}
  }
}
```

---

## Step 5 — All Component Types & Rules

### Complete Component Inventory

**BASIC tab:** `button`, `hero`, `icon`, `icon-list`, `icon-text-group`, `image`, `paragraph`, `rich-text`, `social-share-button`, `tabs`, `title`, `video`

**EVENT DETAILS tab:** `about-event`, `contact-us`, `date-time`, `event-banner`, `event-countdown`, `event-title`, `faq`, `info-cards`, `sessions-schedule`, `simple-location-card`, `simple-pricing`, `speakers`, `sponsors`, `ticket-pricing`

**REGISTRATION tab:** `checkout-form`, `register-button`


### `header`
- `isTransparent: true`, `navbarBackgroundColor: "transparent"`
- `enableMobileBottomBar: true`, `onlyUseIconsInMobile: true`
- Nav items include `"icon"` field (Font Awesome class)
- `mobileBottomNavBackgroundColor`: dark variant of primary or `"#141414"`

### `hero` (dedicated hero component)
- Place in 50-100% width column
- Section background: image with 65% overlay OR video

### `icon-list`
- Use for date + location in hero/header area
- `"layout": "inline"` for side-by-side display
- Each item: `{"id": "...", "icon": "fas fa-calendar", "text": "..."}`
- `iconColor`: primary or accent color

### `title`
- Two-title pattern on every section (see above)
- Label title: `fontSizeToken: "custom"`, `headingFontSizeToken: "h3"`, `fontSize: "1.5rem"`
- Headline title: `fontSizeToken: "custom"`, `headingFontSizeToken: "h2"`, `fontSize: "2.5rem"`
- `enableGradientText: true` on headlines for dark themes

### `paragraph`
- Body text color: `"#C8CBD0"` on very dark (`night`) backgrounds, `"#4C566A"` on light (`nord`), `"#141414"` on warm light (`autumn`)
- `textFontSizeToken: "bodyLarge"` for main descriptions

### `image`
- Standalone image block for About sections, testimonials, contact
- `imageData.src`: URL of image

### `icon`
- Standalone decorative icon before section headings (light themes especially)
- `iconData.icon`: relevant Font Awesome class

### `info-cards`
- `enableIconAnimation: true` for entertainment/energy events
- `enableGradientBorder: true` on dark themes
- `hideCount: true` unless showing real stats with numbers
- Layout: `"3-column"`, `"2-column"`, `"4-column"`, or `"1-column"` (for testimonials)
- Choose relevant Font Awesome icons per card
- `cardBackgroundColor`: slightly lighter than section background for dark themes

### `ticket-pricing`
- Dark themes: `glassMode: true`, `enableGradientBorder: true`, `enable3DEffect: true`
- Light themes: `glassMode: false`
- Always: `hideTicketImages: true`, `hideQuantityRemaining: true`, `buttonVariation: "gradient"`
- `borderRadius: "0px"` for bold/festival events

### `register-button` ← USE THIS instead of `button` for all primary CTAs
- `registerButtonData.variation: "gradient"`
- `registerButtonData.icon`: Font Awesome class
- `registerButtonData.iconPosition: "after"`

### `button` ← only for non-checkout links
- `buttonData.variation: "gradient"` or `"secondary"`

### `event-countdown`
- `countdownData.format: "labels"`
- `showDays: true`, `showHours: true`, `showMinutes: true`, `showSeconds: true`
- `hideOnStart: false`
- `labelColor`: primary or accent color
- `textColor`: white or light

### `sponsors`
- `sponsorsData.variation: "carousel"` — always
- Place right after hero

### `sessions-schedule`
- Minimal styles — the component handles its own rendering
- Place inside a well-padded section with two-title header above it

### `speakers`
- Minimal styles — component handles rendering
- Two-title header above it

### `faq`
- `faqData.questionsDefaultState: "collapsed"`
- `faqData.categoriesDefaultState: "firstExpanded"`
- Use 25%/75% column split

### `tabs`
- Use for multi-topic content (program tracks, topic categories)
- Minimal styles needed

### `icon-text-group`
- Combines an icon + heading + body text in one card-like block
- Good alternative to info-cards when you want a more editorial layout
- Use for feature highlights, step-by-step guides, or benefit breakdowns

### `rich-text`
- Full WYSIWYG-style text block supporting bold, italic, lists, links
- Use when you need formatted text with mixed styles in a single block
- Prefer over `paragraph` when content has structure (bullet lists, headings within text)

### `video`
- Standalone embedded video component (YouTube, Vimeo, etc.)
- Different from `backgroundVideo` (section background) — this is an inline content component
- Use in about sections, speaker intro sections, or recap/promo sections

### `social-share-button`
- Adds social sharing buttons (share to X, LinkedIn, Facebook, etc.)
- Place near CTA sections or at the bottom of content sections
- Minimal configuration needed

### `about-event`
- Dedicated "About Event" component that auto-pulls event description from Salesforce/BT data
- Use instead of manual title+paragraph when event data is connected
- Minimal styles needed — component handles its own rendering

### `date-time`
- Dedicated date & time display component — auto-reads from event data
- Use in header area or about section as an alternative to `icon-list` for date/location
- Minimal styles needed

### `event-banner`
- Full-width banner image component — different from background image
- Use for announcements, speaker reveals, or promotional banners within the page
- `eventBannerData` holds image URL and link

### `simple-pricing`
- Simplified ticket pricing display (no checkout flow)
- Use when you want to show pricing info without triggering registration
- Alternative to `ticket-pricing` for informational pages

### `checkout-form`
- Embeds the full checkout/registration form directly inline on the page
- Use when you want the registration form embedded rather than triggered by a button
- Minimal styles — component handles its own rendering

### `contact-us`
- Use in a 50% column alongside title/paragraph/icon-list
- Minimal styles

### `simple-location-card`
- `showTitle: false`
- `buttonData.icon: "fas fa-map"`, `buttonData.label: "View Map"`

### `footer`
- `isTransparent: true`
- Section background: image with 70% overlay preferred
- Always include: `copyright`, `description`, `linkColumns` (2), `socialLinks` (3)

---

## Step 6 — ID Generation

Pattern: `{type}-{13-digit-timestamp}` or with suffixes for duplicates

Real examples:
- `"header-1776463832139-1776717878247-mjpv7bd2m"`
- `"title-1776468780217"`
- `"info-cards-1776724657151"`

Use realistic 13-digit numbers. Every component must have a globally unique ID.
Column IDs: `"column-1"`, `"column-2"` or descriptive like `"event-countdown-section-column-1"`

---

## Step 7 — siteSettings

Read `references/color-palettes.md` for full siteSettings JSON per event type.

Key rules:
- `"radiusButton": "0"` — bold/festival; `"9999px"` — modern pill; `"0.375rem"` — standard
- `"uiBorderRadius": "0px"` for bold events, `"0.5rem"` for standard
- `"defaultSectionPaddingLinked": false`
- `"defaultColumnGap": "16px"`
- `fontSizingTokens` H1 `sizeEm`: `3.75` for bold (Bebas Neue), `2.5` for standard
- Light theme body text: `"uiFontColorPrimary": "#141414"` not white

---

## Step 8 — Output

Output ONLY raw JSON. No markdown fences. No explanation before or after.
Save as `layout-export-[event-name-slug].json` when asked.

---

## Quality Checklist

- [ ] `"theme"` field at root level
- [ ] Every section: unique `id`, `cssClass`, `gridTemplate`, `layoutType`
- [ ] Every component: unique `id`
- [ ] Two-title pattern (label + headline) in every content section
- [ ] Hero: image/video background OR `gradientAnimation: true` — never plain solid
- [ ] All image/video backgrounds: `backgroundOverlayEnabled: true`
- [ ] Section padding uses `%` units, not `px`
- [ ] `responsiveSpacing` with mobile+tablet on every section
- [ ] `siteSettings.colorScheme`: all 40+ tokens populated
- [ ] `siteSettings.typography`: `titleFontFamily`, `paragraphFontFamily`, `fontSizingTokens`
- [ ] Header: `enableMobileBottomBar: true`, nav items have `icon` field
- [ ] Primary CTAs use `register-button` type, not `button`
- [ ] Footer: `copyright`, `description`, `linkColumns`, `socialLinks`, `logoImageUrl`
- [ ] Zero placeholder text — all fields filled with real event content
- [ ] Nav items anchor links match actual section IDs (e.g. `#tickets-section`)
