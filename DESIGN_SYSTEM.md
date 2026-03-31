# Vanguard Glass-Morphism Design System

## Overview
A sophisticated, refined glass-morphism design system with deep, rich backgrounds, soft transparency effects, and elegant minimalism. Designed for luxury tech products with strong readability and premium aesthetics.

---

## 1. COLOR PALETTE

### Base Background Tones
```
--bg-primary:      #0f0f1a (Deep Navy - primary background)
--bg-secondary:    #191924 (Deep Charcoal - subtle contrast layers)
--bg-accent:       #141419 (Ultra-dark Slate - card backgrounds)
--bg-muted:        #0a0a0f (Almost-black for depth)
```

**Why these values:**
- `#0f0f1a` - Matte deep navy, NOT pure black (#000000)
- Provides luxury perception with visual comfort
- Slight warm-cool gradient (hint of blue) avoids pure black harshness

### Accent Color: Champagne Gold (Refined & Elegant)
```
--accent-primary:  #d4a574 (Warm champagne gold - main accent)
--accent-light:    #e8c29e (Soft champagne - highlights)
--accent-muted:    #9d8b75 (Muted bronze - secondary accent)
--accent-dim:      rgba(212, 165, 116, 0.12) (5% opacity for subtle backgrounds)
```

**Alternative accent options** (if you prefer different moods):
- **Soft Blue**: `#7fa5d4` (cool, professional)
- **Silver Metallic**: `#b0b5c4` (neutral, sophisticated)
- **Warm Bronze**: `#8b7355` (earthy, premium)

### Text & Semantic Colors
```
--text-primary:    #f5f5f7 (Off-white - main text, high contrast)
--text-secondary:  #a0a0a5 (Muted silver - secondary text)
--text-muted:      #6d6d73 (Soft gray - tertiary text)
--text-contrast:   #0f0f1a (Deep for text on light accents)
```

### Glass & Transparency Layer
```
--glass-light:     rgba(245, 245, 247, 0.05) (Barely-there white)
--glass-medium:    rgba(245, 245, 247, 0.08) (Subtle white glass)
--glass-strong:    rgba(245, 245, 247, 0.12) (Medium white glass - 12% opacity)
```

### Border & Dividers
```
--border-light:    rgba(212, 165, 116, 0.08) (Soft gold borders - 8% opacity)
--border-medium:   rgba(212, 165, 116, 0.12) (Medium gold borders - 12% opacity)
--border-strong:   rgba(212, 165, 116, 0.18) (Prominent gold borders - 18% opacity)
--divider-subtle:  rgba(160, 160, 165, 0.04) (Nearly invisible dividers)
```

---

## 2. BACKGROUND SPECIFICATIONS

### Base Background (Body)
```css
background: linear-gradient(135deg, #0f0f1a 0%, #141922 25%, #0d1419 50%, #0a0f18 75%, #0f0f1a 100%);
```

**Characteristics:**
- Subtle gradient (only 1-3% variance between stops)
- Flow from cool to slightly warmer tones
- Creates depth without overwhelming distraction
- Maintains excellent contrast for text
- Duration: 4s rotate animation (optional, very slow)

### Accent Background Gradient (CTAs, Highlights)
```css
background: linear-gradient(135deg, #d4a574 0%, #e5b88d 100%);
```
Used only on primary CTAs and key interactive elements

---

## 3. GLASS CARD STYLES

### Standard Glass Card (Base Template)
```css
.card-base {
  background: rgba(20, 20, 25, 0.6);  /* Deep card base + 60% opacity */
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
  border: 1px solid rgba(212, 165, 116, 0.08);
  border-radius: 16px;
  padding: 24px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2);  /* Subtle shadow for depth */
}
```

### Premium Glass Card (Services, Features)
```css
.card-premium {
  background: rgba(20, 20, 25, 0.5);  /* More transparent premium feel */
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  border: 1px solid rgba(212, 165, 116, 0.12);
  border-radius: 20px;
  padding: 40px;
  box-shadow: 
    0 12px 40px rgba(0, 0, 0, 0.15),
    inset 0 1px 0 rgba(212, 165, 116, 0.12);  /* Inset highlight for luxury */
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}
```

### Glass Card Hover State
```css
.card-premium:hover {
  background: rgba(20, 20, 25, 0.55);
  border-color: rgba(212, 165, 116, 0.18);
  box-shadow: 
    0 16px 48px rgba(0, 0, 0, 0.2),
    inset 0 1px 0 rgba(212, 165, 116, 0.16);
}
```

### Light Glass Card (Overlaid on backgrounds)
```css
.card-light {
  background: rgba(245, 245, 247, 0.05);  /* 5% white transparency */
  backdrop-filter: blur(6px);
  -webkit-backdrop-filter: blur(6px);
  border: 1px solid rgba(245, 245, 247, 0.08);
  border-radius: 12px;
  padding: 20px;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.1);
}
```

### Nested Accent Glass (Accent-tinted glass)
```css
.card-accent {
  background: rgba(212, 165, 116, 0.06);  /* 6% champagne gold - subtle */
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
  border: 1px solid rgba(212, 165, 116, 0.10);
  border-radius: 16px;
  padding: 24px;
}
```

---

## 4. TEXT HIERARCHY

### Display / Hero Text (Primary)
```css
.text-display {
  font-size: clamp(48px, 6vw, 96px);
  font-weight: 700;
  letter-spacing: -0.03em;
  line-height: 1.1;
  color: #f5f5f7;  /* --text-primary */
  font-family: 'Playfair Display', serif;
}
```

### Heading 1 (Sections)
```css
.text-h1 {
  font-size: clamp(32px, 3.5vw, 54px);
  font-weight: 700;
  letter-spacing: -0.02em;
  line-height: 1.2;
  color: #f5f5f7;  /* --text-primary */
  font-family: 'Playfair Display', serif;
}
```

### Heading 2 (Cards, Subsections)
```css
.text-h2 {
  font-size: 20px;
  font-weight: 600;
  letter-spacing: -0.01em;
  line-height: 1.3;
  color: #f5f5f7;  /* --text-primary */
  font-family: 'Playfair Display', serif;
}
```

### Body Text (Primary Content)
```css
.text-body {
  font-size: 16px;
  font-weight: 400;
  letter-spacing: 0;
  line-height: 1.6;
  color: #a0a0a5;  /* --text-secondary */
  font-family: 'Roboto Mono', monospace;
}
```

### Body Small (Secondary Content)
```css
.text-body-sm {
  font-size: 14px;
  font-weight: 400;
  letter-spacing: 0.01em;
  line-height: 1.5;
  color: #6d6d73;  /* --text-muted */
  font-family: 'Roboto Mono', monospace;
}
```

### Label / Caption
```css
.text-label {
  font-size: 11px;
  font-weight: 500;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: #d4a574;  /* --accent-primary */
  font-family: 'Roboto Mono', monospace;
}
```

---

## 5. BUTTON & CTA STYLES

### Primary CTA Button
```css
.btn-primary {
  background: linear-gradient(135deg, #d4a574 0%, #e5b88d 100%);
  color: #0f0f1a;  /* --text-contrast */
  border: 1px solid rgba(212, 165, 116, 0.3);
  padding: 12px 28px;
  border-radius: 100px;
  font-size: 14px;
  font-weight: 600;
  letter-spacing: -0.01em;
  transition: all 0.3s ease;
  cursor: pointer;
}

.btn-primary:hover {
  background: linear-gradient(135deg, #e5b88d 0%, #fff0d9 100%);
  border-color: rgba(212, 165, 116, 0.5);
  box-shadow: 0 8px 24px rgba(212, 165, 116, 0.2);
}
```

### Secondary Glass Button
```css
.btn-secondary {
  background: rgba(212, 165, 116, 0.08);
  color: #d4a574;  /* --accent-primary */
  border: 1px solid rgba(212, 165, 116, 0.20);
  padding: 12px 28px;
  border-radius: 100px;
  font-size: 14px;
  font-weight: 600;
  letter-spacing: -0.01em;
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
  transition: all 0.3s ease;
  cursor: pointer;
}

.btn-secondary:hover {
  background: rgba(212, 165, 116, 0.12);
  border-color: rgba(212, 165, 116, 0.35);
  color: #e8c29e;  /* --accent-light */
}
```

### Ghost Button (Minimal)
```css
.btn-ghost {
  background: transparent;
  color: #a0a0a5;  /* --text-secondary */
  border: 1px solid rgba(212, 165, 116, 0.12);
  padding: 12px 28px;
  border-radius: 100px;
  font-size: 14px;
  font-weight: 600;
  letter-spacing: -0.01em;
  transition: all 0.3s ease;
  cursor: pointer;
}

.btn-ghost:hover {
  border-color: rgba(212, 165, 116, 0.25);
  color: #d4a574;  /* --accent-primary */
}
```

---

## 6. ACCENT COLOR USAGE RULES

### When to Use Accent Color
1. **Primary CTAs**: Main calls-to-action (Sign Up, Start Demo, Continue)
2. **Interactive Highlights**: Hover states, active states
3. **Key Statistics**: Numbers that need visual emphasis
4. **Icons & Indicators**: Leading icons on important elements
5. **Labels & Badges**: Section labels, status badges
6. **Link Text**: Active/hover link states

### When NOT to Use Accent Color
- Body text (use --text-secondary instead)
- Borders that should be subtle (use --border-light)
- Background plates for cards (use glass layer)
- Large text blocks (maintains hierarchy)

### Opacity Rules for Accent Color
| Use Case | Opacity | HEX Code |
|----------|---------|----------|
| Subtle background | 6% | `rgba(212, 165, 116, 0.06)` |
| Light border | 8% | `rgba(212, 165, 116, 0.08)` |
| Medium border | 12% | `rgba(212, 165, 116, 0.12)` |
| Strong border | 18% | `rgba(212, 165, 116, 0.18)` |
| Button background (hover) | 12% | `rgba(212, 165, 116, 0.12)` |
| Shadow/glow | 20% | `rgba(212, 165, 116, 0.20)` |
| Solid text/icon | 100% | `#d4a574` |

---

## 7. COMMON COMPONENT SPECIFICATIONS

### Navigation Bar
```css
#navbar {
  background: rgba(15, 15, 26, 0.4);  /* Deep with 40% opacity */
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  border-bottom: 1px solid rgba(212, 165, 116, 0.08);
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.15);
}
```

### Input Fields
```css
.input-field {
  background: rgba(20, 20, 25, 0.4);
  border: 1px solid rgba(212, 165, 116, 0.12);
  color: #f5f5f7;
  padding: 12px 16px;
  border-radius: 8px;
  backdrop-filter: blur(8px);
}

.input-field:focus {
  border-color: rgba(212, 165, 116, 0.25);
  box-shadow: 0 0 16px rgba(212, 165, 116, 0.1);
}
```

### Badge / Tag
```css
.badge {
  background: rgba(212, 165, 116, 0.12);
  color: #d4a574;
  border: 1px solid rgba(212, 165, 116, 0.20);
  padding: 4px 12px;
  border-radius: 100px;
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.05em;
}
```

### Divider Line
```css
.divider {
  border: none;
  height: 1px;
  background: rgba(212, 165, 116, 0.08);
}
```

---

## 8. SHADOW & DEPTH SYSTEM

### Subtle Shadows (Cards, subtle depth)
```
box-shadow: 0 4px 16px rgba(0, 0, 0, 0.12);
```

### Medium Shadows (Containers, moderate elevation)
```
box-shadow: 0 8px 32px rgba(0, 0, 0, 0.15);
```

### Strong Shadows (Floating, hero elements)
```
box-shadow: 0 16px 48px rgba(0, 0, 0, 0.2);
```

### Inset Highlight (For luxury glass effect)
```
box-shadow: inset 0 1px 0 rgba(212, 165, 116, 0.12);
```

---

## 9. BLUR SPECIFICATIONS

| Type | Blur Value | Use Case |
|------|-----------|----------|
| Subtle | `blur(6px)` | Minimal effect, backgrounds behind text |
| Standard | `blur(8px)` | Cards, normal glass elements |
| Medium | `blur(12px)` | Buttons, navigation bars |
| Strong | `blur(16px)` | Hero sections, high prominence |
| Heavy | `blur(24px)` | Background frosted layers only |

**Rule**: Blur should never exceed 16px on interactive elements (reduces usability).

---

## 10. BORDER RADIUS GUIDELINES

| Element | Border Radius |
|---------|--------------|
| Buttons | `100px` (pill shape) |
| Cards | `16px` |
| Containers | `20px` |
| Inputs | `8px` |
| Badges | `100px` |
| Icons | `50%` |
| Large sections | `28px` |

---

## 11. SPACING SYSTEM

```
Base unit: 4px

--spacing-xs:   4px   (minimal spaces)
--spacing-sm:   8px   (small gaps)
--spacing-md:   16px  (standard)
--spacing-lg:   24px  (comfortable)
--spacing-xl:   32px  (section spacing)
--spacing-2xl:  48px  (large sections)
--spacing-3xl:  64px  (hero sections)
```

---

## 12. ANIMATION PRINCIPLES

- **Transitions**: 300-400ms for UI interactions
- **Easings**: `cubic-bezier(0.4, 0, 0.2, 1)` for smooth, premium feel
- **Delays**: Stagger animations by 50-100ms for cascading effects
- **Avoid**: Rapid blinks, harsh easing, animations on scroll (use sparingly)
- **Subtle motion**: Slightly raising/expanding on hover (2-4px), not dramatic shifts

---

## 13. RESPONSIVE ADJUSTMENTS

### Mobile (< 768px)
- Reduce blur amounts by 2px (too strong on small screens)
- Decrease padding by 20% (optimize touch targets)
- Increase font sizes slightly for readability
- Simplify shadows (single layer, no insets)

### Tablet (768px - 1024px)
- Standard blur and spacing
- Adjust grid layouts to 2 columns where appropriate

### Desktop (> 1024px)
- Full design system as specified
- Enable enhanced shadows and insets

---

## 14. ACCESSIBILITY & CONTRAST CHECKLIST

✓ Primary text (#f5f5f7) on deep backgrounds (#0f0f1a): **WCAG AAA** (18.5:1)
✓ Secondary text (#a0a0a5) on deep backgrounds: **WCAG AA** (8.2:1)
✓ Accent color (#d4a574) text needs dark background (only on CTAs with #0f0f1a bg)
✓ All interactive elements have visible hover/focus states
✓ No information conveyed by color alone
✓ Minimum 44px touch targets for mobile
✓ Button text always has adequate contrast

---

## 15. QUICK REFERENCE CSS VARIABLES

```css
:root {
  /* Backgrounds */
  --bg-primary: #0f0f1a;
  --bg-secondary: #191924;
  --bg-accent: #141419;
  --bg-muted: #0a0a0f;
  
  /* Accent */
  --accent-primary: #d4a574;
  --accent-light: #e8c29e;
  --accent-muted: #9d8b75;
  --accent-dim: rgba(212, 165, 116, 0.12);
  
  /* Text */
  --text-primary: #f5f5f7;
  --text-secondary: #a0a0a5;
  --text-muted: #6d6d73;
  --text-contrast: #0f0f1a;
  
  /* Glass */
  --glass-light: rgba(245, 245, 247, 0.05);
  --glass-medium: rgba(245, 245, 247, 0.08);
  --glass-strong: rgba(245, 245, 247, 0.12);
  
  /* Borders */
  --border-light: rgba(212, 165, 116, 0.08);
  --border-medium: rgba(212, 165, 116, 0.12);
  --border-strong: rgba(212, 165, 116, 0.18);
  --divider-subtle: rgba(160, 160, 165, 0.04);
}
```

---

## IMPLEMENTATION NOTES

1. **Always use CSS custom properties** (--variables) for consistency
2. **Test all interactive elements** for sufficient contrast and hover states
3. **Layer transparency strategically** - don't use multiple overlapping glass layers (causes visual confusion)
4. **Preserve readability above aesthetics** - if a design choice reduces contrast/clarity, reconsider
5. **Mobile-first approach** - reduce blur and effects on smaller screens
6. **Use `backdrop-filter` with fallback** - some browsers don't support it yet
7. **Animate smoothly** - avoid jarring transitions, use standard easing curves

