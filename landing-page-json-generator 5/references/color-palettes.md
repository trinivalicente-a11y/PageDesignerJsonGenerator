# Color Palettes — v2

Complete palette configs per event type. Substitute into `siteSettings.colorScheme` and section background styles.

---

## 1. Tech / AI / Startup
**Theme:** `night` | **Font:** `'Manrope'` | **Radius:** `0.375rem`
**Vibe:** Deep dark, sky blue + indigo + pink accent

```json
{
  "theme": "night",
  "primary": "#38BDF8",
  "secondary": "#818CF8",
  "accent": "#F471B5",
  "background": "#0F172A",
  "darkBg": "#0F172A",
  "midBg": "#1E293B",
  "bodyTextDark": "#C8CBD0",
  "titleGradientStart": "#38BDF8",
  "titleGradientMiddle": "#818CF8",
  "titleGradientEnd": "#54FFFF",
  "buttonGradientStart": "#38BDF8",
  "buttonGradientMiddle": "#818CF8",
  "buttonGradientEnd": "#54FFFF"
}
```

**Section rhythm:**
- Hero: background image + dark overlay 70% | `backgroundColor: "#0F172A"`
- About: `backgroundColor: "#0F172A"`, solid
- Info Cards: gradient `#0F172A` → `#1E293B`
- Caption/Quote: background image + overlay 70%
- Schedule: video background + overlay 70%
- Speakers: `backgroundColor: "#0F172A"`, solid
- Tickets: gradient `#0F172A` → `#1E293B`
- FAQs: gradient
- CTA: background image + overlay 70%
- Footer: transparent, background image + overlay 70%

---

## 2. Medical / Academic / Research
**Theme:** `nord` | **Font:** `'Poppins'` | **Radius:** `9999px` (pill buttons)
**Vibe:** Clean, light, cool Scandinavian blue

```json
{
  "theme": "nord",
  "primary": "#5E81AC",
  "secondary": "#81A1C1",
  "accent": "#88C0D0",
  "background": "#ECEFF4",
  "darkBg": "#2E3440",
  "midBg": "#3B4252",
  "bodyTextDark": "#4C566A",
  "titleGradientStart": "#5E81AC",
  "titleGradientMiddle": "#81A1C1",
  "titleGradientEnd": "#8DC1FF",
  "buttonGradientStart": "#5E81AC",
  "buttonGradientMiddle": "#81A1C1",
  "buttonGradientEnd": "#8DC1FF"
}
```

**Section rhythm:**
- Hero/Header: background image + overlay 70%, content directly in section
- About: background image + overlay 70%, two-column (67%/33%)
- Speakers: transparent, `backgroundColor: "#ECEFF4"`
- Info Cards: no background video (was listed as video but no URL) `backgroundColor: "#ECEFF4"`
- Schedule: transparent, `backgroundColor: "#ECEFF4"`
- Tickets: transparent, `backgroundColor: "#ECEFF4"`
- CTA: video background + overlay 70%
- Contact: background image + overlay 50%
- Footer: transparent

**Note for light themes:** Section labels use primary color (`#5E81AC`) NOT gradient. Body text uses `#4C566A`. Do NOT use gradient text on light themes — use solid colors.

---

## 3. Music Festival / Entertainment
**Theme:** `synthwave` | **Font:** `'Bebas Neue'` | **Radius:** `0` (sharp edges)
**Vibe:** High energy, crimson red, dramatic dark

```json
{
  "theme": "synthwave",
  "primary": "#8C0328",
  "secondary": "#D85252",
  "accent": "#D59B6B",
  "background": "#F1F1F1",
  "darkBg": "#141414",
  "midBg": "#1a1a1a",
  "bodyTextDark": "#f1f1f1",
  "titleGradientStart": "#8C0328",
  "titleGradientMiddle": "#AF0332",
  "titleGradientEnd": "#D2043C",
  "buttonGradientStart": "#8C0328",
  "buttonGradientMiddle": "#AF0332",
  "buttonGradientEnd": "#D2043C"
}
```

**Section rhythm:**
- Hero: video background + overlay 70%, `padding: {top:"0%", left:"14%", right:"14%", bottom:"6%"}`
- Sponsors: gradient `#8c0328` → `#33000e` (90deg)
- About: `backgroundColor: "#F1F1F1"`, solid light
- Schedule: `backgroundColor: "#f1f1f1"`, solid light
- Experience/Info Cards: `backgroundColor: "#F1F1F1"`, solid light
- Location title: gradient `#8c0328` → `#33000e`
- Location card: background image + overlay 65%
- Artists: `backgroundColor: "#f1f1f1"`, solid light
- FAQ: `backgroundColor: "#F1F1F1"`, solid light
- Countdown: gradient `#8c0328` → `#33000e`
- CTA: `backgroundColor: "#f1f1f1"`, solid light
- Footer: background image + overlay 70%

---

## 4. Conference / Summit (Professional)
**Theme:** `autumn` | **Font:** `'Cabin'` or `'Space Grotesk'` | **Radius:** `0.375rem`
**Vibe:** Warm, authoritative, crimson + navy

```json
{
  "theme": "autumn",
  "primary": "#8C0328",
  "secondary": "#D85252",
  "accent": "#D59B6B",
  "background": "#F1F1F1",
  "darkBg": "#0c2a3e",
  "midBg": "#0b273f",
  "bodyTextDark": "#141414",
  "titleGradientStart": "#8C0328",
  "titleGradientMiddle": "#AF0332",
  "titleGradientEnd": "#D85252",
  "buttonGradientStart": "#8C0328",
  "buttonGradientMiddle": "#AF0332",
  "buttonGradientEnd": "#D2043C"
}
```

**Section rhythm:**
- Hero: background image + overlay 65%
- About: `backgroundColor: "#F1F1F1"`, solid light
- Info Cards: `backgroundColor: "#F1F1F1"`, solid light
- Schedule: `backgroundColor: "#F1F1F1"`, solid light
- Tickets: gradient `#8c0328` → `#33000e`
- CTA: gradient animated
- Footer: background image + overlay 70%

---

## 5. Food & Wine / Lifestyle
**Theme:** `coffee` | **Font:** `'Cabin'` | **Radius:** `0.375rem`
**Vibe:** Warm amber, deep teal, cozy

```json
{
  "theme": "coffee",
  "primary": "#DB924C",
  "secondary": "#1a3a37",
  "accent": "#c8a97e",
  "background": "#f5ebe0",
  "darkBg": "#1a3a37",
  "midBg": "#2a4a47",
  "bodyTextDark": "#3d2b1f",
  "titleGradientStart": "#DB924C",
  "titleGradientMiddle": "#c8793a",
  "titleGradientEnd": "#f0a96a",
  "buttonGradientStart": "#DB924C",
  "buttonGradientMiddle": "#c8793a",
  "buttonGradientEnd": "#f0a96a"
}
```

---

## 6. Gala / Awards / Luxury
**Theme:** `luxury` | **Font:** `'Space Grotesk'` | **Radius:** `0.375rem`
**Vibe:** Deep gold + jet black, cinematic

```json
{
  "theme": "luxury",
  "primary": "#C9A84C",
  "secondary": "#1A1A2E",
  "accent": "#E8D5B7",
  "background": "#09090E",
  "darkBg": "#09090E",
  "midBg": "#1A1A2E",
  "bodyTextDark": "#E8D5B7",
  "titleGradientStart": "#FFD700",
  "titleGradientMiddle": "#C9A84C",
  "titleGradientEnd": "#FFD700",
  "buttonGradientStart": "#C9A84C",
  "buttonGradientMiddle": "#8B6914",
  "buttonGradientEnd": "#FFD700"
}
```

---

## 7. Watch Party / Sports
**Theme:** `synthwave` | **Font:** `'Bebas Neue'` | **Radius:** `0`
**Vibe:** Electric blue + orange, high voltage

```json
{
  "theme": "synthwave",
  "primary": "#004fff",
  "secondary": "#ffb84d",
  "accent": "#7360FF",
  "background": "#0b101f",
  "darkBg": "#0b101f",
  "midBg": "#192347",
  "bodyTextDark": "#f1f1f1",
  "titleGradientStart": "#ffb84d",
  "titleGradientMiddle": "#ff7c24",
  "titleGradientEnd": "#ffb84d",
  "buttonGradientStart": "#004fff",
  "buttonGradientMiddle": "#3a7fff",
  "buttonGradientEnd": "#ffb84d"
}
```

---

## Full siteSettings Template

Substitute values from chosen palette above. Use for ALL event types.

```json
"siteSettings": {
  "colorScheme": {
    "uiPrimaryColor": "[primary]",
    "uiPrimaryColorHover": "[primary -10% brightness]",
    "uiPrimaryColorActive": "[primary -20% brightness]",
    "colorOnPrimary": "#EDD0D0",
    "uiSecondaryColor": "[secondary]",
    "colorOnSecondary": "#110202",
    "colorOnAccent": "#100904",
    "uiBackgroundColor": "[background]",
    "colorSurface": "[midBg]",
    "colorSlate": "[midBg slightly lighter]",
    "colorSilver": "[midBg lighter still]",
    "colorLavender": "[accent]",
    "buttonBackgroundColor": "[primary]",
    "buttonColor": "#EDD0D0",
    "buttonHoverBackgroundColor": "[accent]",
    "buttonHoverColor": "#100904",
    "daisyPrimary": "[primary]",
    "daisyPrimaryContent": "#EDD0D0",
    "daisySecondary": "[secondary]",
    "daisySecondaryContent": "#110202",
    "daisyAccent": "[accent]",
    "daisyAccentContent": "#100904",
    "daisyNeutral": "[midBg]",
    "daisyNeutralContent": "#E5E0DC",
    "daisyBase100": "[background]",
    "daisyBase200": "[midBg slightly lighter]",
    "daisyBase300": "[midBg]",
    "daisyBaseContent": "[bodyText — #141414 light themes, #f1f1f1 dark themes]",
    "hyperlinkColor": "[accent]",
    "hyperlinkHoverColor": "[accent lighter]",
    "ulColor": "[accent]",
    "ulActiveColor": "[primary]",
    "primaryButtonColor": "[primary]",
    "primaryButtonContent": "#EDD0D0",
    "primaryButtonHoverColor": "[accent]",
    "primaryButtonHoverContent": "#100904",
    "secondaryButtonColor": "[secondary]",
    "secondaryButtonContent": "#110202",
    "secondaryButtonHoverColor": "[accent]",
    "secondaryButtonHoverContent": "#100904",
    "accentButtonColor": "[accent]",
    "accentButtonContent": "#100904",
    "accentButtonHoverColor": "[primary]",
    "accentButtonHoverContent": "#EDD0D0",
    "gradientStart": "[background or darkBg]",
    "gradientMiddle": "[midBg]",
    "gradientEnd": "[darkBg]",
    "gradientPreset": "linear-90",
    "enableBodyGradient": false,
    "titleGradientStart": "[titleGradientStart]",
    "titleGradientMiddle": "[titleGradientMiddle]",
    "titleGradientEnd": "[titleGradientEnd]",
    "buttonGradientStart": "[buttonGradientStart]",
    "buttonGradientMiddle": "[buttonGradientMiddle]",
    "buttonGradientEnd": "[buttonGradientEnd]"
  },
  "typography": {
    "uiFontColorPrimary": "[#141414 light / #f1f1f1 dark]",
    "uiFontColorSecondary": "[#E5E0DC or secondary]",
    "colorMuted": "[#E5E0DC or muted variant]",
    "uiFontFamily": "[chosen font stack]",
    "uiFontSize": "1rem",
    "uiFontWeight": "400",
    "headingFontWeight": "700",
    "textFontWeight": "400",
    "colorSuccess": "#499380",
    "colorOnSuccess": "#020806",
    "colorWarning": "#E97F19",
    "colorOnWarning": "#130600",
    "colorDanger": "#D40017",
    "colorOnDanger": "#FFD4D1",
    "elevation1": "none",
    "elevation2": "none",
    "daisyInfo": "#42ADBB",
    "daisyInfoContent": "#010B0D",
    "daisySuccess": "#499380",
    "daisySuccessContent": "#020806",
    "daisyWarning": "#E97F19",
    "daisyWarningContent": "#130600",
    "daisyError": "#D40017",
    "daisyErrorContent": "#FFD4D1",
    "fontSizingTokens": [
      {"key": "h1", "label": "H1", "sizeEm": 3.75, "weight": "800"},
      {"key": "h2", "label": "H2", "sizeEm": 2, "weight": "800"},
      {"key": "h3", "label": "H3", "sizeEm": 1.875, "weight": "800"},
      {"key": "bodyLarge", "label": "Body Large", "sizeEm": 1.15, "weight": "600"},
      {"key": "bodySmall", "label": "Body Small", "sizeEm": 1, "weight": "600"},
      {"key": "caption", "label": "Caption", "sizeEm": 0.875, "weight": "600"}
    ],
    "titleFontFamily": "[chosen font stack]",
    "paragraphFontFamily": "[chosen font stack]"
  },
  "stylings": {
    "uiBorderStyle": "0 solid rgba(39,39,39,0.06)",
    "uiBorderWidth": "0",
    "uiBorderRadius": "[0px bold events / 0.5rem standard]",
    "uiBorderColor": "rgba(39,39,39,0.06)",
    "radiusButton": "[0 bold/festival / 9999px pill / 0.375rem standard]",
    "radiusSection": "0px",
    "spaceXxs": "0.25rem",
    "spaceXs": "0.5rem",
    "spaceSm": "0.75rem",
    "spaceMd": "1rem",
    "spaceLg": "1.5rem",
    "uiInnerPadding": "1rem",
    "defaultSectionPaddingTop": "0px",
    "defaultSectionPaddingBottom": "0px",
    "defaultSectionPaddingLeft": "0px",
    "defaultSectionPaddingRight": "0px",
    "defaultSectionPaddingLinked": false,
    "defaultColumnGap": "16px",
    "contentMaxWidth": "",
    "componentsBorderWidth": "0",
    "componentsBorderStyle": "none",
    "componentsBorderColor": "rgba(39,39,39,0.06)",
    "tabsBorderWidth": "0",
    "tabsBorderStyle": "none",
    "tabsBorderColor": "rgba(39,39,39,0.06)",
    "sectionsColumnsBorderWidth": "0",
    "sectionsColumnsBorderStyle": "none",
    "sectionsColumnsBorderColor": "rgba(39,39,39,0.06)"
  },
  "customCSS": ""
}
```
