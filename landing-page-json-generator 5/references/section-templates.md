# Section Templates — v2

Copy-paste JSON templates for every section type. Fill `[PLACEHOLDERS]` with event data.
All IDs: `{type}-{13-digit-timestamp}` — use unique realistic numbers per component.

---

## STANDARD SECTION WRAPPER

Every section uses this outer structure:

```json
{
  "id": "[section-id]",
  "name": "[Section Name]",
  "cssClass": "section-[section-id]",
  "layoutType": "standard",
  "gridTemplate": "[1fr / repeat(2,1fr) / 1fr 3fr / etc]",
  "styles": {
    "gap": "1rem",
    "width": "100%",
    "height": "",
    "margin": {"top": "", "left": "", "right": "", "bottom": ""},
    "padding": {"top": "10%", "left": "10%", "right": "10%", "bottom": "10%"},
    "fontSize": "1rem",
    "minHeight": "",
    "textColor": "#141414",
    "alignItems": "stretch",
    "marginUnit": "px",
    "borderColor": "",
    "borderStyle": "solid",
    "borderWidth": "0px",
    "paddingUnit": "%",
    "borderRadius": "",
    "contentWidth": "full-width",
    "justifyItems": "space-between",
    "defaultShadow": "none",
    "backgroundSize": "cover",
    "borderWidthTop": "0px",
    "backgroundColor": "[BG_COLOR]",
    "backgroundImage": "[IMAGE_URL or empty]",
    "backgroundStyle": "[solid / image / video / gradient / transparent]",
    "backgroundVideo": "[VIDEO_URL or empty]",
    "borderWidthLeft": "0px",
    "backgroundRepeat": "default",
    "borderWidthRight": "0px",
    "gradientEndColor": "[DARK_BG]",
    "borderWidthBottom": "0px",
    "gradientAnimation": false,
    "gradientDirection": 90,
    "responsiveSpacing": {
      "mobile": {
        "margin": {"top": "", "left": "", "right": "", "bottom": ""},
        "padding": {"top": "8%", "left": "8%", "right": "8%", "bottom": "8%"}
      },
      "tablet": {
        "margin": {"top": "", "left": "", "right": "", "bottom": ""},
        "padding": {"top": "8%", "left": "8%", "right": "8%", "bottom": "8%"}
      }
    },
    "backgroundPosition": "center center",
    "gradientStartColor": "[LIGHT_BG]",
    "backgroundVideoLoop": true,
    "gradientMiddleColor": "[MID_BG]",
    "backgroundAttachment": "scroll",
    "backgroundVideoMuted": true,
    "enableGradientBorder": false,
    "responsiveBackground": {},
    "backgroundOverlayColor": "#000000",
    "backgroundVideoAutoplay": true,
    "backgroundOverlayEnabled": false,
    "backgroundOverlayOpacity": 70,
    "enableGradientBackground": false
  },
  "columns": [ ... ]
}
```

---

## HEADER SECTION

```json
{
  "id": "header-section",
  "name": "Header Section",
  "cssClass": "section-header-section",
  "layoutType": "standard",
  "gridTemplate": "1fr",
  "styles": {
    "gap": "1rem", "width": "100%",
    "margin": {"top": "", "left": "", "right": "", "bottom": ""},
    "padding": {"top": "0%", "left": "0%", "right": "0%", "bottom": "0%"},
    "paddingUnit": "%", "fontSize": "1rem", "minHeight": "",
    "alignItems": "stretch", "contentWidth": "full-width",
    "justifyItems": "space-between", "defaultShadow": "none",
    "backgroundSize": "cover", "borderWidthTop": "0px",
    "backgroundColor": "[HEADER_BG or transparent]",
    "backgroundImage": "[HEADER_BG_IMAGE or empty]",
    "backgroundStyle": "[gradient or image]",
    "backgroundVideo": "",
    "backgroundOverlayEnabled": true, "backgroundOverlayOpacity": 70,
    "backgroundOverlayColor": "#000000",
    "gradientAnimation": false, "gradientDirection": 90,
    "gradientStartColor": "[DARK_BG]", "gradientEndColor": "[DARK_BG]",
    "enableGradientBackground": false,
    "responsiveSpacing": {
      "mobile": {"margin": {"top":"","left":"","right":"","bottom":""}, "padding": {"top":"0%","left":"8%","right":"8%","bottom":"0%"}},
      "tablet": {"margin": {"top":"","left":"","right":"","bottom":""}, "padding": {"top":"0%","left":"8%","right":"8%","bottom":"6%"}}
    },
    "responsiveBackground": {}
  },
  "columns": [{
    "id": "column-1", "name": "Column 1", "cssClass": "column-column-1", "width": "100%",
    "styles": {"padding": {"top":"0px","left":"","right":"","bottom":"0px"}, "defaultShadow": "none", "responsiveSpacing": {}},
    "components": [
      {
        "id": "header-[TS1]",
        "type": "header",
        "data": {"id": "header", "icon": "fas fa-grip-vertical", "name": "Header", "description": "Modern navigation header with logo, menu, and register button", "componentType": "header"},
        "styles": {
          "width": "", "margin": {"top":"","left":"","right":"","bottom":""}, "padding": {"top":"","left":"","right":"","bottom":"0px"},
          "fontSize": "", "maxWidth": "100%", "maxWidthUnit": "%", "widthUnit": "%",
          "glassMode": false, "textAlign": "left", "textColor": "",
          "fontFamily": "[FONT_STACK]",
          "marginUnit": "px", "headerGlass": false, "paddingUnit": "px",
          "borderRadius": "", "borderRadiusUnit": "px",
          "navItemColor": "[LIGHT_TEXT or #f1f1f1]",
          "navItemHoverColor": "[PRIMARY]",
          "navItemActiveColor": "[SECONDARY]",
          "hamburgerIconColor": "[PRIMARY]",
          "textFontSize": "1rem", "fontSizeToken": "custom",
          "isTransparent": true,
          "enable3DEffect": false,
          "headerImageUrl": "",
          "backgroundColor": "transparent", "backgroundImage": "",
          "headingFontSize": "1rem",
          "navbarAlignment": "space-between",
          "enableHeaderGradient": true,
          "navbarBackgroundColor": "transparent",
          "backgroundColorUserUpdated": false,
          "mobileBottomNavBackgroundColor": "#141414",
          "responsiveSpacing": {
            "mobile": {"margin": {"top":"","left":"","right":"","bottom":""}, "padding": {"top":"","left":"","right":"","bottom":""}},
            "tablet": {"margin": {"top":"","left":"","right":"","bottom":""}, "padding": {"top":"","left":"","right":"","bottom":""}}
          }
        },
        "headerData": {
          "logoText": "", "logoImageUrl": "[LOGO_URL]", "logoUrl": "", "removeLogo": false, "hideEventName": true,
          "navItems": [
            {"id": "nav_[TS2]", "url": "#about-section", "icon": "fas fa-info", "label": "About"},
            {"id": "nav_[TS3]", "url": "#tickets-section", "icon": "fas fa-ticket-alt", "label": "Tickets"},
            {"id": "nav_[TS4]", "url": "#schedule-section", "icon": "far fa-rectangle-list", "label": "Schedule"},
            {"id": "nav_[TS5]", "url": "#location-section", "icon": "fas fa-location-dot", "label": "Location"}
          ],
          "registerButtonLabel": "Register Now",
          "registerButtonVariation": "gradient",
          "registerButtonIcon": "", "registerButtonIconPosition": "before",
          "registerButtonStyles": {}, "hideRegisterButton": false,
          "enableSecondaryButton": false, "secondaryButtonLabel": "", "secondaryButtonUrl": "#", "secondaryButtonVariation": "secondary",
          "hideNavMenu": false, "hideBackToEventGroup": false, "hideLanguageSelector": false,
          "enableMobileBottomBar": true, "onlyUseIconsInMobile": true, "mobileBottomBarRegisterVariation": ""
        }
      }
    ]
  }]
}
```

---

## HERO SECTION (video preferred)

```json
{
  "id": "hero-section",
  "name": "Hero Section",
  "cssClass": "section-hero-section",
  "layoutType": "standard",
  "gridTemplate": "1fr",
  "styles": {
    "gap": "1rem", "width": "100%",
    "margin": {"top": "", "left": "", "right": "", "bottom": ""},
    "padding": {"top": "0%", "left": "14%", "right": "14%", "bottom": "6%"},
    "paddingUnit": "%", "fontSize": "1rem", "minHeight": "",
    "alignItems": "stretch", "contentWidth": "full-width",
    "defaultShadow": "none", "backgroundSize": "cover",
    "backgroundColor": "[DARK_BG]",
    "backgroundImage": "",
    "backgroundStyle": "video",
    "backgroundVideo": "[VIDEO_URL]",
    "backgroundVideoLoop": true, "backgroundVideoMuted": true, "backgroundVideoAutoplay": true,
    "backgroundOverlayEnabled": true, "backgroundOverlayOpacity": 70, "backgroundOverlayColor": "#000000",
    "gradientAnimation": false, "gradientDirection": 90,
    "gradientStartColor": "[DARK_BG]", "gradientEndColor": "[DARK_BG]",
    "enableGradientBackground": false, "enableGradientBorder": false,
    "responsiveSpacing": {
      "mobile": {"margin": {"top":"","left":"","right":"","bottom":""}, "padding": {"top":"0%","left":"8%","right":"8%","bottom":"0%"}},
      "tablet": {"margin": {"top":"","left":"","right":"","bottom":""}, "padding": {"top":"0%","left":"8%","right":"8%","bottom":"0%"}}
    },
    "responsiveBackground": {}
  },
  "columns": [{
    "id": "column-1", "name": "Column 1", "cssClass": "column-column-1", "width": "100%",
    "styles": {"padding": {"top":"0px","left":"","right":"","bottom":"0px"}, "defaultShadow": "none", "responsiveSpacing": {}},
    "components": [
      {
        "id": "icon-list-[TS1]",
        "type": "icon-list",
        "data": {"id": "icon-list", "icon": "fas fa-list-ul", "name": "Icon List", "description": "List with an icon next to each text item", "componentType": "icon-list"},
        "styles": {
          "width": "", "margin": {"top": "2%", "left": "", "right": "", "bottom": ""},
          "padding": {"top": "", "left": "", "right": "", "bottom": ""},
          "fontSize": "", "itemGap": "12px", "glassMode": false,
          "iconColor": "[PRIMARY]", "textAlign": "center", "textColor": "[LIGHT_TEXT]",
          "fontFamily": "[FONT_STACK]",
          "marginUnit": "%", "paddingUnit": "px", "borderRadius": "",
          "textFontSize": "1rem", "fontSizeToken": "custom",
          "enable3DEffect": false, "backgroundColor": "transparent",
          "enableHeaderGradient": true, "responsiveSpacing": {}
        },
        "iconListData": {
          "items": [
            {"id": "icon-list-item-[TS2]", "icon": "fas fa-calendar", "text": "[EVENT_DATE]"},
            {"id": "icon-list-item-[TS3]", "icon": "fas fa-map-marker-alt", "text": "[EVENT_LOCATION]"}
          ],
          "layout": "inline"
        }
      },
      {
        "id": "title-[TS4]",
        "type": "title",
        "data": {"id": "title", "icon": "fas fa-heading", "name": "Title", "description": "Heading text component with customizable styling", "componentType": "title"},
        "styles": {
          "width": "", "margin": {"top": "0px", "left": "", "right": "", "bottom": "-25px"},
          "padding": {"top": "", "left": "", "right": "", "bottom": ""},
          "fontSize": "2.5rem", "maxWidth": "",
          "glassMode": false, "textAlign": "center", "textColor": "",
          "fontFamily": "[FONT_STACK]",
          "fontWeight": "700", "marginUnit": "px", "paddingUnit": "px",
          "borderRadius": "", "textFontSize": "1rem", "fontSizeToken": "custom",
          "isTransparent": true, "customFontSize": "2.5rem",
          "enable3DEffect": false, "backgroundColor": "", "backgroundImage": "",
          "headingFontSize": "2.5rem", "headingFontSizeToken": "h1",
          "enableGradientText": true,
          "enableHeaderGradient": true,
          "responsiveSpacing": {"mobile": {"margin": {"top":"0px","left":"","right":"","bottom":""}, "padding": {"top":"","left":"","right":"","bottom":""}}}
        },
        "textData": {"icon": "", "text": "[EVENT_NAME_PART_1]", "textColor": "[PRIMARY]"}
      },
      {
        "id": "title-[TS5]",
        "type": "title",
        "data": {"id": "title", "icon": "fas fa-heading", "name": "Title", "description": "Heading text component with customizable styling", "componentType": "title"},
        "styles": {
          "width": "", "margin": {"top": "-15px", "left": "", "right": "", "bottom": ""},
          "padding": {"top": "", "left": "", "right": "", "bottom": ""},
          "fontSize": "2.5rem", "glassMode": false, "textAlign": "center",
          "fontFamily": "[FONT_STACK]",
          "fontWeight": "700", "marginUnit": "px", "paddingUnit": "px",
          "textFontSize": "1rem", "fontSizeToken": "custom",
          "isTransparent": true, "customFontSize": "2.5rem",
          "enable3DEffect": false, "backgroundColor": "", "backgroundImage": "",
          "headingFontSize": "2.5rem", "headingFontSizeToken": "h1",
          "enableGradientText": false,
          "enableHeaderGradient": true,
          "responsiveSpacing": {}
        },
        "textData": {"icon": "", "text": "[EVENT_NAME_PART_2]", "textColor": "[LIGHT_TEXT]"}
      },
      {
        "id": "paragraph-[TS6]",
        "type": "paragraph",
        "data": {"id": "paragraph", "icon": "fas fa-paragraph", "name": "Paragraph", "description": "Paragraph text component with customizable styling", "componentType": "paragraph"},
        "styles": {
          "width": "", "margin": {"top": "", "left": "", "right": "", "bottom": ""},
          "padding": {"top": "", "left": "", "right": "", "bottom": ""},
          "fontSize": "1.15rem", "glassMode": false, "textAlign": "center",
          "fontFamily": "[FONT_STACK]",
          "marginUnit": "px", "paddingUnit": "px", "borderRadius": "",
          "textFontSize": "1.15rem", "fontSizeToken": "custom",
          "isTransparent": true, "enable3DEffect": false,
          "headingFontSize": "1rem", "enableHeaderGradient": true,
          "textFontSizeToken": "bodyLarge", "responsiveSpacing": {}
        },
        "paragraphData": {"text": "[EVENT_DESCRIPTION]", "textColor": "[LIGHT_TEXT]"}
      },
      {
        "id": "ticket-pricing-[TS7]",
        "type": "ticket-pricing",
        "data": {"id": "ticket-pricing", "icon": "fas fa-ticket-alt", "name": "Ticket Pricing", "description": "Display event ticket pricing cards with registration", "componentType": "ticket-pricing"},
        "styles": {
          "width": "", "margin": {"top": "", "left": "", "right": "", "bottom": ""},
          "padding": {"top": "", "left": "", "right": "", "bottom": ""},
          "fontSize": "", "glassMode": false, "textAlign": "left", "textColor": "[LIGHT_TEXT]",
          "fontFamily": "[FONT_STACK]",
          "marginUnit": "px", "paddingUnit": "px",
          "borderRadius": "0px",
          "textFontSize": "1rem", "fontSizeToken": "custom",
          "isTransparent": true, "readMoreColor": "[PRIMARY]",
          "enable3DEffect": true,
          "buttonVariation": "gradient",
          "hideGuestTickets": true, "hideTicketImages": true,
          "hideProductTickets": false, "hideDonationTickets": true,
          "enableGradientBorder": true,
          "hideQuantityRemaining": true, "hideTicketDescription": true,
          "cardContentBackgroundColor": "[PRIMARY]",
          "responsiveSpacing": {}
        }
      }
    ]
  }]
}
```

---

## SPONSORS SECTION

```json
{
  "id": "sponsors-section",
  "name": "Sponsors Section",
  "cssClass": "section-sponsors-section",
  "layoutType": "standard",
  "gridTemplate": "repeat(1, 1fr)",
  "styles": {
    "gap": "1rem", "width": "100%",
    "margin": {"top": "", "left": "", "right": "", "bottom": ""},
    "padding": {"top": "0px", "left": "0px", "right": "0px", "bottom": "0px"},
    "paddingUnit": "px", "fontSize": "1rem", "minHeight": "",
    "alignItems": "stretch", "contentWidth": "full-width", "defaultShadow": "none",
    "backgroundSize": "cover",
    "backgroundColor": "",
    "backgroundStyle": "gradient",
    "backgroundVideo": "", "backgroundImage": "",
    "gradientStartColor": "[PRIMARY]", "gradientMiddleColor": "[PRIMARY]", "gradientEndColor": "[DARK_VARIANT]",
    "gradientDirection": 90, "gradientAnimation": false,
    "enableGradientBackground": true,
    "backgroundOverlayEnabled": false, "backgroundOverlayOpacity": 50, "backgroundOverlayColor": "#000000",
    "responsiveSpacing": {}, "responsiveBackground": {}
  },
  "columns": [{
    "id": "column-1", "name": "Column 1", "cssClass": "column-column-1", "width": "100%",
    "styles": {"padding": {"top":"","left":"","right":"","bottom":""}, "defaultShadow": "none", "responsiveSpacing": {}},
    "components": [{
      "id": "sponsors-[TS1]",
      "type": "sponsors",
      "data": {"id": "sponsors", "icon": "fas fa-handshake", "name": "Sponsors", "description": "Display event sponsors in an infinite scroll or by tier", "componentType": "sponsors"},
      "styles": {
        "width": "", "margin": {"top": "0%", "left": "0%", "right": "0%", "bottom": "0%"},
        "padding": {"top": "2%", "left": "", "right": "", "bottom": "0%"},
        "fontSize": "", "glassMode": false, "textAlign": "left", "textColor": "",
        "fontFamily": "[FONT_STACK]",
        "marginUnit": "%", "paddingUnit": "%", "borderRadius": "",
        "textFontSize": "1rem", "fontSizeToken": "custom",
        "isTransparent": true, "enable3DEffect": false,
        "backgroundColor": "transparent", "headingFontSize": "1rem",
        "enableHeaderGradient": true,
        "responsiveSpacing": {
          "mobile": {"margin": {"top":"0%","left":"0%","right":"0%","bottom":"0%"}, "padding": {"top":"4%","left":"","right":"","bottom":"0%"}}
        }
      },
      "sponsorsData": {"variation": "carousel"}
    }]
  }]
}
```

---

## ABOUT SECTION (two-column: text + image)

```json
{
  "id": "about-section",
  "name": "About Section",
  "cssClass": "section-about-section",
  "layoutType": "standard",
  "gridTemplate": "2fr 1fr",
  "styles": {
    "gap": "1rem", "width": "100%",
    "margin": {"top": "", "left": "", "right": "", "bottom": ""},
    "padding": {"top": "10%", "left": "10%", "right": "10%", "bottom": "10%"},
    "paddingUnit": "%", "fontSize": "1rem", "minHeight": "",
    "alignItems": "stretch", "contentWidth": "full-width", "defaultShadow": "none",
    "backgroundSize": "cover", "backgroundColor": "[SECTION_BG]",
    "backgroundStyle": "solid", "backgroundVideo": "", "backgroundImage": "",
    "gradientAnimation": false,
    "enableGradientBackground": false,
    "backgroundOverlayEnabled": false, "backgroundOverlayOpacity": 50, "backgroundOverlayColor": "#000000",
    "responsiveSpacing": {
      "mobile": {"margin": {"top":"","left":"","right":"","bottom":""}, "padding": {"top":"8%","left":"8%","right":"8%","bottom":"8%"}},
      "tablet": {"margin": {"top":"","left":"","right":"","bottom":""}, "padding": {"top":"8%","left":"8%","right":"8%","bottom":"8%"}}
    },
    "responsiveBackground": {}
  },
  "columns": [
    {
      "id": "column-1", "name": "Column 1", "cssClass": "column-column-1", "width": "67%",
      "styles": {"padding": {"top":"0px","left":"","right":"","bottom":"0px"}, "defaultShadow": "none", "responsiveSpacing": {}},
      "components": [
        {
          "id": "title-[TS1]", "type": "title",
          "data": {"id": "title", "icon": "fas fa-heading", "name": "Title", "description": "Heading text component with customizable styling", "componentType": "title"},
          "styles": {
            "fontSize": "1.5rem", "textAlign": "left", "isTransparent": true,
            "enable3DEffect": false, "backgroundColor": "",
            "headingFontSize": "1.5rem", "headingFontSizeToken": "h3",
            "enableGradientText": true,
            "fontFamily": "[FONT_STACK]",
            "margin": {"top": "", "left": "", "right": "", "bottom": "2%"},
            "padding": {"top": "", "left": "", "right": "", "bottom": ""},
            "marginUnit": "%", "paddingUnit": "px",
            "enableHeaderGradient": true, "responsiveSpacing": {}
          },
          "textData": {"icon": "fas fa-compact-disc", "text": "ABOUT THE EVENT", "textColor": "[PRIMARY]"}
        },
        {
          "id": "title-[TS2]", "type": "title",
          "data": {"id": "title", "icon": "fas fa-heading", "name": "Title", "description": "Heading text component with customizable styling", "componentType": "title"},
          "styles": {
            "fontSize": "2.5rem", "textAlign": "left", "isTransparent": true,
            "enable3DEffect": false, "backgroundColor": "",
            "headingFontSize": "2.5rem", "headingFontSizeToken": "h2",
            "enableGradientText": false,
            "fontFamily": "[FONT_STACK]",
            "margin": {"top": "", "left": "", "right": "", "bottom": ""},
            "padding": {"top": "", "left": "", "right": "", "bottom": ""},
            "enableHeaderGradient": true, "responsiveSpacing": {}
          },
          "textData": {"icon": "", "text": "[ABOUT_HEADLINE]", "textColor": "[BODY_TEXT_COLOR]"}
        },
        {
          "id": "paragraph-[TS3]", "type": "paragraph",
          "data": {"id": "paragraph", "icon": "fas fa-paragraph", "name": "Paragraph", "description": "Paragraph text component with customizable styling", "componentType": "paragraph"},
          "styles": {
            "fontSize": "1.15rem", "textAlign": "left", "isTransparent": true,
            "enable3DEffect": false, "backgroundColor": "",
            "headingFontSize": "1rem",
            "fontFamily": "[FONT_STACK]",
            "textFontSizeToken": "bodyLarge",
            "margin": {"top": "", "left": "", "right": "", "bottom": ""},
            "padding": {"top": "", "left": "", "right": "", "bottom": ""},
            "enableHeaderGradient": true, "responsiveSpacing": {}
          },
          "paragraphData": {"text": "[EVENT_DESCRIPTION_LONG]", "textColor": "[BODY_TEXT_COLOR]"}
        }
      ]
    },
    {
      "id": "column-2", "name": "Column 2", "cssClass": "column-column-2", "width": "33%",
      "styles": {"padding": {"top":"0px","left":"","right":"","bottom":"0px"}, "defaultShadow": "none", "responsiveSpacing": {}},
      "components": [{
        "id": "image-[TS4]", "type": "image",
        "data": {"id": "image", "icon": "fas fa-image", "name": "Image", "description": "Standalone image component", "componentType": "image"},
        "styles": {
          "width": "100%", "margin": {"top": "", "left": "", "right": "", "bottom": ""},
          "padding": {"top": "", "left": "", "right": "", "bottom": ""},
          "fontSize": "", "glassMode": false, "textAlign": "center",
          "marginUnit": "px", "paddingUnit": "px", "borderRadius": "",
          "enable3DEffect": false, "backgroundColor": "transparent",
          "responsiveSpacing": {}
        },
        "imageData": {"src": "[ABOUT_IMAGE_URL]", "alt": "[EVENT_NAME]"}
      }]
    }
  ]
}
```

---

## INFO CARDS SECTION ("Why Attend")

```json
{
  "id": "info-cards-section",
  "name": "Why Attend Section",
  "cssClass": "section-info-cards-section",
  "layoutType": "standard",
  "gridTemplate": "1fr",
  "styles": {
    "gap": "1rem", "width": "100%",
    "margin": {"top": "", "left": "", "right": "", "bottom": ""},
    "padding": {"top": "10%", "left": "10%", "right": "10%", "bottom": "10%"},
    "paddingUnit": "%", "fontSize": "1rem", "minHeight": "",
    "alignItems": "stretch", "contentWidth": "full-width", "defaultShadow": "none",
    "backgroundSize": "cover", "backgroundColor": "[SECTION_BG]",
    "backgroundStyle": "solid", "backgroundVideo": "", "backgroundImage": "",
    "gradientAnimation": false, "enableGradientBackground": false,
    "backgroundOverlayEnabled": false, "backgroundOverlayOpacity": 50, "backgroundOverlayColor": "#000000",
    "responsiveSpacing": {
      "mobile": {"margin": {"top":"","left":"","right":"","bottom":""}, "padding": {"top":"8%","left":"8%","right":"8%","bottom":"8%"}},
      "tablet": {"margin": {"top":"","left":"","right":"","bottom":""}, "padding": {"top":"8%","left":"8%","right":"8%","bottom":"8%"}}
    },
    "responsiveBackground": {}
  },
  "columns": [{
    "id": "column-1", "name": "Column 1", "cssClass": "column-column-1", "width": "100%",
    "styles": {"padding": {"top":"0px","left":"","right":"","bottom":"0px"}, "defaultShadow": "none", "responsiveSpacing": {}},
    "components": [
      {
        "id": "title-[TS1]", "type": "title",
        "data": {"id": "title", "icon": "fas fa-heading", "name": "Title", "description": "Heading text component with customizable styling", "componentType": "title"},
        "styles": {
          "fontSize": "1.5rem", "textAlign": "left", "isTransparent": true,
          "enable3DEffect": false, "backgroundColor": "",
          "headingFontSize": "1.5rem", "headingFontSizeToken": "h3",
          "enableGradientText": true,
          "fontFamily": "[FONT_STACK]",
          "margin": {"top": "", "left": "", "right": "", "bottom": ""},
          "padding": {"top": "", "left": "", "right": "", "bottom": ""},
          "marginUnit": "%", "paddingUnit": "px",
          "enableHeaderGradient": true, "responsiveSpacing": {}
        },
        "textData": {"icon": "fas fa-compact-disc", "text": "WHY ATTEND", "textColor": "[PRIMARY]"}
      },
      {
        "id": "title-[TS2]", "type": "title",
        "data": {"id": "title", "icon": "fas fa-heading", "name": "Title", "description": "Heading text component with customizable styling", "componentType": "title"},
        "styles": {
          "fontSize": "2.5rem", "textAlign": "left", "isTransparent": true,
          "enable3DEffect": false, "backgroundColor": "",
          "headingFontSize": "2.5rem", "headingFontSizeToken": "h2",
          "enableGradientText": true,
          "fontFamily": "[FONT_STACK]",
          "margin": {"top": "", "left": "", "right": "", "bottom": ""},
          "padding": {"top": "", "left": "", "right": "", "bottom": ""},
          "enableHeaderGradient": true, "responsiveSpacing": {}
        },
        "textData": {"icon": "", "text": "[WHY_ATTEND_HEADLINE]", "textColor": "[BODY_TEXT_COLOR]"}
      },
      {
        "id": "paragraph-[TS3]", "type": "paragraph",
        "data": {"id": "paragraph", "icon": "fas fa-paragraph", "name": "Paragraph", "description": "Paragraph text component with customizable styling", "componentType": "paragraph"},
        "styles": {
          "fontSize": "1.15rem", "textAlign": "left", "isTransparent": true,
          "enable3DEffect": false, "fontFamily": "[FONT_STACK]",
          "textFontSizeToken": "bodyLarge",
          "margin": {"top": "", "left": "", "right": "", "bottom": ""},
          "padding": {"top": "", "left": "", "right": "", "bottom": ""},
          "enableHeaderGradient": true, "responsiveSpacing": {}
        },
        "paragraphData": {"text": "[WHY_ATTEND_DESCRIPTION]", "textColor": "[BODY_TEXT_COLOR]"}
      },
      {
        "id": "info-cards-[TS4]", "type": "info-cards",
        "data": {"id": "info-cards", "icon": "fas fa-chart-bar", "name": "Info Cards", "description": "Display event statistics in card format", "componentType": "info-cards"},
        "styles": {
          "margin": {"top": "", "left": "", "right": "", "bottom": ""},
          "padding": {"top": "", "left": "", "right": "", "bottom": ""},
          "fontSize": "", "glassMode": false, "iconColor": "",
          "textAlign": "left", "textColor": "", "countColor": "",
          "fontFamily": "", "marginUnit": "px", "paddingUnit": "px",
          "borderRadius": "", "iconFontSize": "1.5rem",
          "textFontSize": "", "fontSizeToken": "custom",
          "isTransparent": true, "enable3DEffect": false,
          "backgroundColor": "transparent", "backgroundImage": "",
          "headingFontSize": "1.5rem",
          "iconFontSizeToken": "custom", "customIconFontSize": "1.5rem",
          "textFontSizeToken": "custom", "tierFontSizeToken": "custom",
          "titleFontSizeToken": "custom", "headingFontSizeToken": "custom",
          "customHeadingFontSize": "1.5rem",
          "cardBackgroundColor": "",
          "enableIconAnimation": true,
          "enableGradientBorder": true,
          "responsiveSpacing": {}
        },
        "infoCardsData": {
          "cards": [
            {"id": "card-[TS4]-1", "icon": "fas fa-graduation-cap", "type": "custom", "count": 0, "title": "[BENEFIT_1_TITLE]", "description": "[BENEFIT_1_DESC]"},
            {"id": "card-[TS4]-2", "icon": "fas fa-users", "type": "custom", "count": 0, "title": "[BENEFIT_2_TITLE]", "description": "[BENEFIT_2_DESC]"},
            {"id": "card-[TS4]-3", "icon": "fas fa-lightbulb", "type": "custom", "count": 0, "title": "[BENEFIT_3_TITLE]", "description": "[BENEFIT_3_DESC]"}
          ],
          "layout": "3-column",
          "hideCount": true
        }
      }
    ]
  }]
}
```

---

## COUNTDOWN + CTA SECTION (two-column)

```json
{
  "id": "event-countdown-section",
  "name": "Event Countdown Section",
  "cssClass": "section-event-countdown-section",
  "layoutType": "standard",
  "gridTemplate": "1fr 3fr",
  "styles": {
    "gap": "1rem", "width": "100%",
    "margin": {"top": "", "left": "", "right": "", "bottom": ""},
    "padding": {"top": "6%", "left": "6%", "right": "6%", "bottom": "6%"},
    "paddingUnit": "%", "fontSize": "1rem", "minHeight": "",
    "alignItems": "stretch", "contentWidth": "full-width", "defaultShadow": "none",
    "backgroundSize": "cover", "backgroundColor": "",
    "backgroundStyle": "gradient",
    "backgroundVideo": "", "backgroundImage": "",
    "gradientStartColor": "[PRIMARY]", "gradientMiddleColor": "[PRIMARY]", "gradientEndColor": "[DARK_VARIANT]",
    "gradientDirection": 90, "gradientAnimation": false,
    "enableGradientBackground": true,
    "backgroundOverlayEnabled": false, "backgroundOverlayOpacity": 50, "backgroundOverlayColor": "#000000",
    "responsiveSpacing": {}, "responsiveBackground": {}
  },
  "columns": [
    {
      "id": "event-countdown-section-column-1", "name": "Column 1", "cssClass": "column-event-countdown-section-column-1", "width": "25%",
      "styles": {"padding": {"top":"","left":"","right":"","bottom":""}, "defaultShadow": "none", "responsiveSpacing": {}},
      "components": [
        {
          "id": "title-[TS1]", "type": "title",
          "data": {"id": "title", "icon": "fas fa-heading", "name": "Title", "description": "Heading text component with customizable styling", "componentType": "title"},
          "styles": {
            "fontSize": "1.5rem", "textAlign": "left", "isTransparent": true,
            "enable3DEffect": false, "headingFontSize": "1.5rem", "headingFontSizeToken": "h3",
            "fontFamily": "[FONT_STACK]",
            "margin": {"top": "", "left": "", "right": "", "bottom": ""},
            "padding": {"top": "", "left": "", "right": "", "bottom": ""},
            "enableHeaderGradient": true, "responsiveSpacing": {}
          },
          "textData": {"icon": "", "text": "Upcoming Event", "textColor": "[LIGHT_TEXT]"}
        },
        {
          "id": "paragraph-[TS2]", "type": "paragraph",
          "data": {"id": "paragraph", "icon": "fas fa-paragraph", "name": "Paragraph", "description": "Paragraph text component with customizable styling", "componentType": "paragraph"},
          "styles": {
            "fontSize": "1.15rem", "textAlign": "left", "isTransparent": true,
            "enable3DEffect": false, "fontFamily": "[FONT_STACK]",
            "textFontSizeToken": "bodyLarge",
            "margin": {"top": "", "left": "", "right": "", "bottom": ""},
            "padding": {"top": "", "left": "", "right": "", "bottom": ""},
            "enableHeaderGradient": true,
            "responsiveSpacing": {"mobile": {"margin": {"top":"","left":"","right":"","bottom":""}, "padding": {"top":"","left":"","right":"","bottom":""}}}
          },
          "paragraphData": {"text": "Save The Date & Book Your Ticket", "textColor": "#ffffff"}
        }
      ]
    },
    {
      "id": "event-countdown-section-column-2", "name": "Column 2", "cssClass": "column-event-countdown-section-column-2", "width": "75%",
      "styles": {"padding": {"top":"","left":"","right":"","bottom":""}, "defaultShadow": "none", "responsiveSpacing": {}},
      "components": [{
        "id": "event-countdown-[TS3]", "type": "event-countdown",
        "data": {"id": "event-countdown", "icon": "fas fa-clock", "name": "Event Countdown", "description": "Countdown timer to event start date", "componentType": "event-countdown"},
        "styles": {
          "width": "", "margin": {"top": "", "right": "", "bottom": "", "left": ""},
          "padding": {"top": "", "right": "", "bottom": "", "left": ""},
          "fontSize": "2em", "glassMode": false, "textAlign": "left",
          "textColor": "[LIGHT_TEXT]",
          "fontFamily": "[FONT_STACK]",
          "labelColor": "[SECONDARY or accent]",
          "marginUnit": "px", "paddingUnit": "px", "borderRadius": "",
          "textFontSize": "1rem", "fontSizeToken": "custom",
          "customFontSize": "2em",
          "enable3DEffect": false, "backgroundColor": "transparent",
          "responsiveSpacing": {"mobile": {"margin": {"top":"","left":"","right":"","bottom":""}, "padding": {"top":"","left":"","right":"","bottom":""}}}
        },
        "countdownData": {
          "format": "labels",
          "showDays": true, "showHours": true,
          "hideOnStart": false, "showMinutes": true, "showSeconds": true
        }
      }]
    }
  ]
}
```

---

## CTA SECTION (full-width, image/video background)

```json
{
  "id": "cta-section",
  "name": "CTA Section",
  "cssClass": "section-cta-section",
  "layoutType": "standard",
  "gridTemplate": "repeat(1, 1fr)",
  "styles": {
    "gap": "1rem", "width": "100%",
    "margin": {"top": "", "left": "", "right": "", "bottom": ""},
    "padding": {"top": "12%", "left": "12%", "right": "12%", "bottom": "12%"},
    "paddingUnit": "%", "fontSize": "1rem", "minHeight": "",
    "alignItems": "stretch", "contentWidth": "full-width", "defaultShadow": "none",
    "backgroundSize": "cover", "backgroundColor": "[DARK_BG]",
    "backgroundStyle": "solid",
    "backgroundVideo": "", "backgroundImage": "",
    "gradientAnimation": false, "enableGradientBackground": false,
    "backgroundOverlayEnabled": false, "backgroundOverlayOpacity": 50, "backgroundOverlayColor": "#000000",
    "responsiveSpacing": {
      "mobile": {"margin": {"top":"","left":"","right":"","bottom":""}, "padding": {"top":"8%","left":"8%","right":"8%","bottom":"8%"}},
      "tablet": {"margin": {"top":"","left":"","right":"","bottom":""}, "padding": {"top":"8%","left":"8%","right":"8%","bottom":"8%"}}
    },
    "responsiveBackground": {}
  },
  "columns": [{
    "id": "column-1", "name": "Column 1", "cssClass": "column-column-1", "width": "100%",
    "styles": {"padding": {"top":"0px","left":"","right":"","bottom":"0px"}, "defaultShadow": "none", "responsiveSpacing": {}},
    "components": [
      {
        "id": "title-[TS1]", "type": "title",
        "data": {"id": "title", "icon": "fas fa-heading", "name": "Title", "description": "Heading text component with customizable styling", "componentType": "title"},
        "styles": {
          "fontSize": "2.5rem", "textAlign": "center", "isTransparent": true,
          "enable3DEffect": false, "headingFontSize": "2.5rem", "headingFontSizeToken": "h1",
          "enableGradientText": true, "fontFamily": "[FONT_STACK]",
          "margin": {"top": "", "left": "", "right": "", "bottom": ""},
          "padding": {"top": "", "left": "", "right": "", "bottom": ""},
          "enableHeaderGradient": true, "responsiveSpacing": {}
        },
        "textData": {"icon": "", "text": "[CTA_HEADLINE]", "textColor": ""}
      },
      {
        "id": "paragraph-[TS2]", "type": "paragraph",
        "data": {"id": "paragraph", "icon": "fas fa-paragraph", "name": "Paragraph", "description": "Paragraph text component with customizable styling", "componentType": "paragraph"},
        "styles": {
          "fontSize": "1.15rem", "textAlign": "center", "isTransparent": true,
          "enable3DEffect": false, "fontFamily": "[FONT_STACK]",
          "textFontSizeToken": "bodyLarge",
          "margin": {"top": "", "left": "", "right": "", "bottom": ""},
          "padding": {"top": "", "left": "", "right": "", "bottom": ""},
          "enableHeaderGradient": true, "responsiveSpacing": {}
        },
        "paragraphData": {"text": "[CTA_SUBTEXT]", "textColor": "[LIGHT_TEXT]"}
      },
      {
        "id": "register-button-[TS3]", "type": "register-button",
        "data": {"id": "register-button", "icon": "fas fa-user-plus", "name": "Register Button", "description": "Button to start checkout flow", "componentType": "register-button"},
        "styles": {
          "width": "", "margin": {"top": "", "left": "", "right": "", "bottom": ""},
          "padding": {"top": "", "left": "", "right": "", "bottom": ""},
          "fontSize": "", "glassMode": false, "textAlign": "center",
          "fontFamily": "[FONT_STACK]",
          "marginUnit": "px", "paddingUnit": "px", "borderRadius": "",
          "textFontSize": "1rem", "fontSizeToken": "custom",
          "enable3DEffect": false, "backgroundColor": "",
          "responsiveSpacing": {}
        },
        "registerButtonData": {
          "icon": "fas fa-play", "label": "[CTA_BUTTON_LABEL]",
          "variation": "gradient", "borderRadius": "", "iconPosition": "after"
        }
      }
    ]
  }]
}
```

---

## FAQ SECTION (two-column split)

```json
{
  "id": "faq-section",
  "name": "FAQ Section",
  "cssClass": "section-faq-section",
  "layoutType": "standard",
  "gridTemplate": "1fr 3fr",
  "styles": {
    "gap": "1rem", "width": "100%",
    "margin": {"top": "", "left": "", "right": "", "bottom": ""},
    "padding": {"top": "10%", "left": "10%", "right": "10%", "bottom": "10%"},
    "paddingUnit": "%", "fontSize": "1rem", "minHeight": "",
    "alignItems": "stretch", "contentWidth": "full-width", "defaultShadow": "none",
    "backgroundSize": "cover", "backgroundColor": "[SECTION_BG]",
    "backgroundStyle": "gradient",
    "gradientStartColor": "[DARK_BG]", "gradientMiddleColor": "[DARK_BG]", "gradientEndColor": "[DARKER_BG]",
    "gradientDirection": 90, "gradientAnimation": false, "enableGradientBackground": true,
    "backgroundOverlayEnabled": false, "backgroundOverlayOpacity": 50, "backgroundOverlayColor": "#000000",
    "responsiveSpacing": {
      "mobile": {"margin": {"top":"","left":"","right":"","bottom":""}, "padding": {"top":"8%","left":"8%","right":"8%","bottom":"8%"}},
      "tablet": {"margin": {"top":"","left":"","right":"","bottom":""}, "padding": {"top":"8%","left":"8%","right":"8%","bottom":"8%"}}
    },
    "responsiveBackground": {}
  },
  "columns": [
    {
      "id": "column-1", "name": "Column 1", "cssClass": "column-column-1", "width": "25%",
      "styles": {"padding": {"top":"","left":"","right":"","bottom":""}, "defaultShadow": "none", "responsiveSpacing": {}},
      "components": [
        {
          "id": "title-[TS1]", "type": "title",
          "data": {"id": "title", "icon": "fas fa-heading", "name": "Title", "description": "Heading text component with customizable styling", "componentType": "title"},
          "styles": {
            "fontSize": "1rem", "textAlign": "left", "isTransparent": true,
            "enable3DEffect": false, "headingFontSize": "1rem", "headingFontSizeToken": "h3",
            "enableGradientText": false, "fontFamily": "[FONT_STACK]",
            "margin": {"top": "", "left": "", "right": "", "bottom": ""},
            "padding": {"top": "", "left": "", "right": "", "bottom": ""},
            "enableHeaderGradient": true, "responsiveSpacing": {}
          },
          "textData": {"icon": "", "text": "NEED HELP?", "textColor": "[LIGHT_TEXT]"}
        },
        {
          "id": "title-[TS2]", "type": "title",
          "data": {"id": "title", "icon": "fas fa-heading", "name": "Title", "description": "Heading text component with customizable styling", "componentType": "title"},
          "styles": {
            "fontSize": "2.5rem", "textAlign": "left", "isTransparent": true,
            "enable3DEffect": false, "headingFontSize": "2.5rem", "headingFontSizeToken": "h2",
            "enableGradientText": true, "fontFamily": "[FONT_STACK]",
            "margin": {"top": "", "left": "", "right": "", "bottom": ""},
            "padding": {"top": "", "left": "", "right": "", "bottom": ""},
            "enableHeaderGradient": true, "responsiveSpacing": {}
          },
          "textData": {"icon": "", "text": "FAQs", "textColor": "[BODY_TEXT_COLOR]"}
        }
      ]
    },
    {
      "id": "column-2", "name": "Column 2", "cssClass": "column-column-2", "width": "75%",
      "styles": {"padding": {"top":"","left":"","right":"","bottom":""}, "defaultShadow": "none", "responsiveSpacing": {}},
      "components": [{
        "id": "faq-[TS3]", "type": "faq",
        "data": {"id": "faq", "icon": "fas fa-question-circle", "name": "FAQ", "description": "Display frequently asked questions grouped by category", "componentType": "faq"},
        "styles": {
          "margin": {"top": "", "left": "", "right": "", "bottom": ""},
          "padding": {"top": "", "left": "", "right": "", "bottom": ""},
          "fontSize": "", "glassMode": false, "textAlign": "left", "textColor": "",
          "fontFamily": "", "marginUnit": "px", "paddingUnit": "px", "borderRadius": "",
          "textFontSize": "", "fontSizeToken": "custom",
          "isTransparent": true, "enable3DEffect": false,
          "backgroundColor": "transparent",
          "headingFontSize": "1.5rem", "customHeadingFontSize": "1.5rem",
          "responsiveSpacing": {}
        },
        "faqData": {"questionsDefaultState": "collapsed", "categoriesDefaultState": "firstExpanded"}
      }]
    }
  ]
}
```

---

## FOOTER SECTION

```json
{
  "id": "footer-section",
  "name": "Footer Section",
  "cssClass": "section-footer-section",
  "layoutType": "standard",
  "gridTemplate": "repeat(1, 1fr)",
  "styles": {
    "gap": "1rem", "width": "100%",
    "margin": {"top": "", "left": "", "right": "", "bottom": ""},
    "padding": {"top": "0px", "left": "64px", "right": "64px", "bottom": "0px"},
    "paddingUnit": "px", "fontSize": "1rem", "minHeight": "",
    "alignItems": "stretch", "contentWidth": "full-width", "defaultShadow": "none",
    "backgroundSize": "cover", "backgroundColor": "[DARK_BG]",
    "backgroundImage": "[FOOTER_IMAGE_URL or empty]",
    "backgroundStyle": "image",
    "backgroundVideo": "",
    "backgroundOverlayEnabled": true, "backgroundOverlayOpacity": 70, "backgroundOverlayColor": "#000000",
    "gradientAnimation": false, "gradientDirection": 90,
    "gradientStartColor": "[DARK_BG]", "gradientEndColor": "[DARK_BG]",
    "enableGradientBackground": false, "enableGradientBorder": false,
    "responsiveSpacing": {}, "responsiveBackground": {}
  },
  "columns": [{
    "id": "column-1", "name": "Column 1", "cssClass": "column-column-1", "width": "100%",
    "styles": {"padding": {"top":"","left":"","right":"","bottom":""}, "defaultShadow": "none", "responsiveSpacing": {}},
    "components": [{
      "id": "footer-[TS1]", "type": "footer",
      "data": {"id": "footer", "icon": "fas fa-window-minimize", "name": "Footer", "description": "Footer with logo, links, social media, and copyright", "componentType": "footer"},
      "styles": {
        "width": "", "margin": {"top": "", "left": "", "right": "", "bottom": ""},
        "padding": {"top": "", "left": "", "right": "", "bottom": ""},
        "fontSize": "", "glassMode": false, "textAlign": "left", "textColor": "[LIGHT_TEXT]",
        "fontFamily": "", "marginUnit": "px", "paddingUnit": "%",
        "textFontSize": "", "fontSizeToken": "custom",
        "isTransparent": true, "enable3DEffect": false,
        "backgroundColor": "transparent", "headingFontSize": "",
        "responsiveSpacing": {}
      },
      "footerData": {
        "logoUrl": "", "logoText": "", "logoImageUrl": "[LOGO_URL]",
        "copyright": "© [YEAR] [ORG_NAME]. All rights reserved.",
        "description": "[FOOTER_TAGLINE]",
        "linkColumns": [
          {
            "id": "link-col-[TS2]",
            "title": "Event",
            "links": [
              {"id": "link-[TS3]", "url": "#tickets-section", "label": "Tickets"},
              {"id": "link-[TS4]", "url": "#schedule-section", "label": "Schedule"},
              {"id": "link-[TS5]", "url": "#about-section", "label": "About"}
            ]
          },
          {
            "id": "link-col-[TS6]",
            "title": "Information",
            "links": [
              {"id": "link-[TS7]", "url": "#info-cards-section", "label": "Why Attend"},
              {"id": "link-[TS8]", "url": "#faq-section", "label": "FAQ"},
              {"id": "link-[TS9]", "url": "#location-section", "label": "Location"}
            ]
          }
        ],
        "socialLinks": [
          {"id": "social-[TS10]", "url": "#", "icon": "fab fa-x", "platform": "X"},
          {"id": "social-[TS11]", "url": "#", "icon": "fab fa-linkedin", "platform": "LinkedIn"},
          {"id": "social-[TS12]", "url": "#", "icon": "fab fa-instagram", "platform": "Instagram"}
        ]
      }
    }]
  }]
}
```
