# DESIGN.md

# Gemini-inspired Minimal AI Interface

## 1. Design Philosophy

Create an extremely minimal, spacious and sophisticated AI interface inspired by the visual language of the Google
Gemini web application.

The design must communicate:

- Calm
- Intelligence
- Simplicity
- Approachability
- Premium technology
- Generous whitespace
- Soft depth
- Subtle spatial lighting

The interface must NEVER feel like a traditional dashboard.

Avoid:

- Dense layouts
- Excessive cards
- Strong borders
- Heavy shadows
- Large navigation systems
- Excessive decorative elements
- Strong gradients covering the entire page
- Excessive use of brand colors

The visual hierarchy must be created primarily through:

1. Typography
2. Whitespace
3. Scale
4. Soft radial lighting
5. Rounded geometry
6. Extremely subtle elevation

The overall impression should be:

"An intelligent interface floating inside a quiet digital space."

---

# 2. Theme System

The interface supports two complete visual themes:

- LIGHT MODE
- DARK MODE

Both themes MUST preserve exactly the same:

- Layout
- Component dimensions
- Typography
- Border radii
- Spacing
- Alignment
- Interaction model

Only colors, contrast and atmospheric lighting change.

The dark theme is NOT a simple inversion of the light theme.

---

# 3. Color System

## 3.1 Light Mode

### Global background

```css
--color-background: #FAF9F9

;
```

The screenshot uses an extremely soft warm-neutral off-white rather than pure white.

Do NOT use pure `#FFFFFF` as the page background.

### Primary text

```css
--color-text-primary: #1F1F1F

;
```

Used for:

- Main heading
- Primary labels
- Important interface text

The text should never be pure black.

### Secondary text

```css
--color-text-secondary: #5F6368

;
```

Used for:

- Input placeholder
- Secondary labels
- Supporting UI text

### Input surface

```css
--color-surface: #FFFFFF

;
```

The main prompt/input container is pure white.

### Input icon

```css
--color-icon: #3C4043

;
```

Icons should remain visually subtle.

### Border

Borders should be almost invisible.

```css
--color-border:

rgba
(
60
,
64
,
67
,
0.08
)
;
```

Prefer shadow/elevation over visible borders.

---

# 3.2 Dark Mode

### Global background

```css
--color-background: #0F0F0F

;
```

The dark screenshot uses a very dark neutral surface rather than pure black.

Do NOT use `#000000` as the default page background.

### Primary text

```css
--color-text-primary: #E3E3E3

;
```

### Secondary text

```css
--color-text-secondary: #C4C7C5

;
```

### Muted text

```css
--color-text-muted: #9AA0A6

;
```

### Input surface

```css
--color-surface: #1E1F20

;
```

This is one of the most important dark-mode colors.

The prompt bar must be clearly distinguishable from the page background, but only through a subtle tonal difference.

### Border

```css
--color-border:

rgba
(
255
,
255
,
255
,
0.04
)
;
```

Borders should remain nearly invisible.

---

# 4. Atmospheric Gradient

The radial glow is one of the defining characteristics of this design.

It must be subtle and blurred.

It should NOT look like a conventional gradient background.

It should resemble light illuminating the space behind the central interface.

---

## 4.1 Light Mode Glow

Approximate visual composition:

```css
background:

radial-gradient
(
ellipse

45
%
40
%
at

50
%
50
%
,
rgba
(
183
,
220
,
252
,
0.82
)
0
%
,
rgba
(
205
,
230
,
251
,
0.65
)
28
%
,
rgba
(
229
,
240
,
249
,
0.35
)
52
%
,
rgba
(
250
,
249
,
249
,
0
)
78
%
)
,
#FAF9F9

;
```

Characteristics:

- Cool pale blue
- Very soft edges
- Large diffusion radius
- Centered horizontally
- Concentrated around the main interaction area
- Never saturated

The glow should feel like atmospheric light rather than a visible gradient.

---

## 4.2 Dark Mode Glow

```css
background:

radial-gradient
(
ellipse

42
%
38
%
at

50
%
50
%
,
rgba
(
30
,
55
,
125
,
0.62
)
0
%
,
rgba
(
25
,
43
,
94
,
0.48
)
30
%
,
rgba
(
17
,
26
,
56
,
0.30
)
52
%
,
rgba
(
15
,
15
,
15
,
0
)
78
%
)
,
#0F0F0F

;
```

The dark glow should transition through:

```text
Deep Indigo
     ↓
Dark Blue
     ↓
Blue-black
     ↓
#0F0F0F
```

The glow MUST remain behind the content.

---

# 5. Typography

## Primary Typeface

Use:

```text
Google Sans
```

Google Sans is the preferred typeface for the interface.

Google Sans is part of Google's broader typography system, while Google has also developed Google Sans Flex for more
flexible typographic applications.

Recommended CSS:

```css
font-family:

"Google Sans"
,
"Google Sans Flex"
,
Arial,
sans-serif

;
```

If Google Sans is unavailable, use:

```css
"Google Sans Flex"
,
Arial,
sans-serif

;
```

Do NOT use:

- Times New Roman
- Georgia
- Serif fonts
- Heavy geometric display fonts
- Decorative fonts

---

# 6. Typography Scale

## Hero / Main Heading

The main greeting is the visual focal point.

Example:

```text
¿Por dónde empezamos?
```

Recommended:

```css
font-size:

34
px

;
font-weight:

400
;
line-height:

1.2
;
letter-spacing:

-
0.02
em

;
```

Desktop range:

```text
32px – 36px
```

Preferred:

```text
34px
```

The heading must feel light and elegant.

Do NOT use bold.

---

## Input Text

```css
font-size:

16
px

;
font-weight:

400
;
line-height:

1.5
;
letter-spacing:

0
;
```

Placeholder:

```css
color:

var
(
--color-text-secondary

)
;
```

---

## Model Selector

Example:

```text
Flash
```

Recommended:

```css
font-size:

14
px

;
font-weight:

500
;
line-height:

1.4
;
```

---

# 7. Font Weight System

Use a very restrained weight system.

```text
400 → Regular
500 → Medium
```

Primary usage:

```text
Headings        → 400
Body            → 400
Input           → 400
Navigation      → 400
Buttons         → 500
Model selector  → 500
```

Avoid:

```text
600
700
800
900
```

unless absolutely necessary.

The visual hierarchy should come from scale and whitespace, not from heavy font weights.

---

# 8. Page Composition

The interface should use a single centered composition.

Desktop:

```text
┌──────────────────────────────────────────────┐
│                                              │
│                                              │
│                                              │
│                                              │
│              Main heading                    │
│                                              │
│        ┌────────────────────────────┐        │
│        │  +  Prompt          Flash  │        │
│        └────────────────────────────┘        │
│                                              │
│                                              │
│                                              │
└──────────────────────────────────────────────┘
```

The central content must NOT feel vertically centered mathematically.

It should feel optically centered around the middle of the viewport.

---

# 9. Main Content Width

Maximum content width:

```css
--content-width:

640
px

;
```

Preferred prompt width:

```css
width:

min
(
614
px,

calc
(
100
vw

-
48
px

)
)
;
```

The screenshot's desktop prompt is approximately:

```text
614px wide
60px high
```

---

# 10. Vertical Composition

The main heading should sit approximately:

```text
45% – 42%
```

from the top of the viewport depending on viewport dimensions.

The prompt should sit approximately:

```text
50% – 54%
```

from the top.

Recommended structure:

```css
.hero {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}
```

But apply a small optical vertical offset:

```css
transform:

translateY
(
-
2
%
)
;
```

The objective is optical balance, not mathematical centering.

---

# 11. Heading → Input Spacing

Recommended:

```css
gap:

36
px

;
```

The heading should have substantial breathing room.

Do not place the input immediately below the heading.

Recommended visual relationship:

```text
Heading

      ~36px

Prompt
```

---

# 12. Prompt Bar

The prompt bar is the most important UI component.

It should resemble a floating capsule.

Dimensions:

```css
height:

60
px

;
width:

614
px

;
```

Maximum:

```css
max-width:

614
px

;
```

Mobile:

```css
width:

calc
(
100
vw

-
32
px

)
;
```

---

# 13. Prompt Bar Geometry

Use a full pill:

```css
border-radius:

9999
px

;
```

Never use:

```text
8px
12px
16px
20px
```

The prompt is intentionally much more rounded.

---

# 14. Prompt Bar — Light Mode

```css
background: #FFFFFF

;
```

Recommended shadow:

```css
box-shadow:

0
2
px

6
px

rgba
(
60
,
64
,
67
,
0.10
)
,
0
1
px

2
px

rgba
(
60
,
64
,
67
,
0.08
)
;
```

The shadow must be extremely soft.

The prompt should appear elevated without looking like a card.

---

# 15. Prompt Bar — Dark Mode

```css
background: #1E1F20

;
```

Recommended shadow:

```css
box-shadow:

0
2
px

8
px

rgba
(
0
,
0
,
0
,
0.18
)
;
```

Avoid strong borders.

The separation between:

```text
#0F0F0F
```

and

```text
#1E1F20
```

should provide most of the perceived elevation.

---

# 16. Prompt Internal Layout

Structure:

```text
┌────────────────────────────────────────────────────────┐
│  +    Pregunta a Gemini              Flash   ˅    🎙    │
└────────────────────────────────────────────────────────┘
```

Use:

```css
display: flex

;
align-items: center

;
```

Recommended horizontal padding:

```css
padding:

0
22
px

;
```

---

# 17. Prompt Icon

The leading "+" icon should be:

```text
18px – 20px
```

Use a lightweight stroke.

Recommended:

```css
stroke-width:

1.8
;
```

Do not use a filled icon.

---

# 18. Prompt Placeholder

Example:

```text
Pregunta a Gemini
```

Recommended:

```css
font-size:

16
px

;
font-weight:

400
;
```

Light mode:

```css
color: #5F6368

;
```

Dark mode:

```css
color: #C4C7C5

;
```

---

# 19. Model Selector

The model selector appears aligned toward the right.

Example:

```text
Flash  ˅
```

Recommended:

```css
font-size:

14
px

;
font-weight:

500
;
```

Use a small chevron:

```text
10px – 12px
```

Spacing:

```css
gap:

8
px

;
```

The selector must remain visually secondary to the prompt.

---

# 20. Microphone Icon

The microphone should be:

```text
18px
```

Positioned at the far right.

Use a lightweight outline icon.

Recommended:

```css
stroke-width:

1.8
;
```

Do not use a filled microphone.

---

# 21. Overall Border Radius Language

The interface is based almost entirely on rounded geometry.

Primary values:

```css
--radius-pill:

9999
px

;
--radius-large:

28
px

;
--radius-medium:

20
px

;
--radius-small:

12
px

;
```

Primary interactive elements should use:

```text
pill / capsule geometry
```

Secondary containers should use:

```text
20–28px
```

Avoid sharp corners.

---

# 22. Shadows

Shadows must be:

- Soft
- Diffused
- Low opacity
- Short range

Never use conventional strong card shadows.

Avoid:

```css
box-shadow:

0
10
px

30
px

rgba
(
0
,
0
,
0
,
.3
)
;
```

Prefer:

```css
box-shadow:

0
2
px

8
px

rgba
(
0
,
0
,
0
,
.08
)
;
```

---

# 23. Whitespace

Whitespace is a fundamental design element.

The interface should feel almost empty.

Do NOT try to fill unused space.

Large areas of empty background are intentional.

Recommended principles:

```text
More whitespace
Less decoration

More breathing room
Less UI chrome

More typography
Less visual noise
```

---

# 24. Interaction Design

Interactions should be subtle.

## Prompt hover

Light:

```css
box-shadow:

0
3
px

10
px

rgba
(
60
,
64
,
67
,
.12
)
,
0
1
px

3
px

rgba
(
60
,
64
,
67
,
.08
)
;
```

Dark:

```css
background: #202124

;
```

Do not dramatically transform the component.

---

# 25. Focus State

The focus state may intensify the surrounding blue atmospheric glow.

Recommended:

```css
box-shadow:

0
0
0
1
px

rgba
(
66
,
133
,
244
,
0.08
)
,
0
4
px

16
px

rgba
(
66
,
133
,
244
,
0.10
)
;
```

Avoid a conventional bright browser-style outline.

The focus state should feel integrated into the environment.

---

# 26. Animation

Animations should be almost imperceptible.

Recommended:

```css
transition:
box-shadow

180
ms ease,
background-color

180
ms ease,
opacity

180
ms ease

;
```

The background glow may have an extremely slow animation.

Example:

```css
animation:
ambientGlow

8
s ease-in-out infinite alternate

;
```

The animation should NOT be distracting.

---

# 27. Responsive Design

## Desktop

```text
Prompt width: 614px
Prompt height: 60px
Heading: 34px
```

## Tablet

```text
Prompt width:
calc(100vw - 64px)

Heading:
32px
```

## Mobile

```text
Prompt width:
calc(100vw - 32px)

Prompt height:
56px

Heading:
28px
```

On mobile, maintain the same visual language.

Do not introduce additional navigation or UI merely because the viewport is smaller.

---

# 28. Layout Grid

Use a simple centered grid.

```css
.container {
    width: 100%;
    max-width: 1200px;
    margin-inline: auto;
    padding-inline: 24px;
}
```

The primary hero content should remain independent from the maximum page container.

```css
.hero-content {
    width: min(100%, 640px);
    margin-inline: auto;
}
```

---

# 29. Visual Hierarchy

Priority order:

### 1. Main heading

Largest and darkest/lightest text element.

### 2. Prompt bar

Largest interactive component.

### 3. Prompt placeholder

Readable but secondary.

### 4. Model selector

Small and subtle.

### 5. Icons

Minimal visual weight.

The user should immediately understand:

```text
What can I do?
       ↓
Where do I type?
```

Nothing else should compete for attention.

---

# 30. Light / Dark Token Map

```css
/* LIGHT */

:root {
    --background: #FAF9F9;
    --surface: #FFFFFF;

    --text-primary: #1F1F1F;
    --text-secondary: #5F6368;
    --text-muted: #80868B;

    --icon: #3C4043;

    --border: rgba(60, 64, 67, 0.08);

    --glow-primary: rgba(183, 220, 252, 0.82);
    --glow-secondary: rgba(205, 230, 251, 0.65);
}


/* DARK */

.dark {
    --background: #0F0F0F;
    --surface: #1E1F20;

    --text-primary: #E3E3E3;
    --text-secondary: #C4C7C5;
    --text-muted: #9AA0A6;

    --icon: #C4C7C5;

    --border: rgba(255, 255, 255, 0.04);

    --glow-primary: rgba(30, 55, 125, 0.62);
    --glow-secondary: rgba(25, 43, 94, 0.48);
}
```

---

# 31. Recommended CSS Foundation

```css
* {
    box-sizing: border-box;
}

html,
body {
    width: 100%;
    min-height: 100%;
    margin: 0;
}

body {
    font-family: "Google Sans",
    "Google Sans Flex",
    Arial,
    sans-serif;

    color: var(--text-primary);

    background: radial-gradient(
            ellipse 45% 40% at 50% 50%,
            var(--glow-primary) 0%,
            var(--glow-secondary) 28%,
            rgba(229, 240, 249, 0.35) 52%,
            rgba(250, 249, 249, 0) 78%
    ),
    var(--background);

    -webkit-font-smoothing: antialiased;
    text-rendering: optimizeLegibility;
}
```

Dark mode should replace the atmospheric gradient with the dark blue/indigo version described above.

---

# 32. Accessibility

Maintain WCAG-compliant text contrast.

Do not reduce text opacity excessively.

Avoid relying exclusively on:

- Color
- Glow
- Shadow

to communicate interactive state.

Interactive elements must remain keyboard accessible.

Focus states should be visually distinguishable.

---

# 33. Design Do / Don't

## DO

- Use Google Sans
- Use enormous amounts of whitespace
- Use subtle blue atmospheric lighting
- Use pill-shaped interactive elements
- Use very soft shadows
- Use restrained typography
- Keep the interface centered
- Keep visual hierarchy extremely simple
- Use dark charcoal instead of pure black
- Use off-white instead of pure white for the light canvas

## DON'T

- Add gradients everywhere
- Add colorful cards
- Use glassmorphism
- Use strong borders
- Use heavy shadows
- Use bold headings
- Add unnecessary navigation
- Add excessive icons
- Use saturated blue backgrounds
- Use conventional dashboard layouts
- Fill empty space unnecessarily

---

# 34. Core Design Formula

```text
MINIMAL UI
+
GOOGLE SANS
+
EXTREME WHITESPACE
+
SOFT ROUNDED GEOMETRY
+
FLOATING PROMPT
+
ATMOSPHERIC BLUE GLOW
+
SUBTLE ELEVATION
=
GEMINI-INSPIRED INTERFACE
```

---

# 35. Primary Visual Reference

The design should visually resemble the following composition:

```text
                    EMPTY SPACE


                 ¿Por dónde empezamos?


              ┌──────────────────────────┐
              │ +  Pregunta a Gemini     │
              │                    Flash ˅│
              └──────────────────────────┘


                    EMPTY SPACE
```

The central interaction is the product.

Everything else exists to support it.

---

# 36. Final Design Principle

When implementing this design, always prefer:

```text
LESS
```

over:

```text
MORE
```

If a visual element is not necessary, remove it.

If a shadow can be softer, make it softer.

If a color can be less saturated, make it less saturated.

If more whitespace improves the composition, add it.

The final result should feel like a sophisticated AI interface that is almost disappearing into its own environment.
