# Nebo Pools Design System - Style Guide
## For Webflow Development

---

## Quick Reference

| Element | Value |
|---------|-------|
| **Heading Font** | Fraunces (Google Fonts) |
| **Body Font** | Outfit (Google Fonts) |
| **Primary Color** | #4DD0E1 (Cyan) |
| **Secondary Color** | #0A2540 (Deep Navy) |
| **Accent Color** | #E8B84A (Gold) |

---

## 1. Typography

### Font Families

```css
/* Google Fonts Import */
@import url('https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600;9..144,700&family=Outfit:wght@400;500;600;700&display=swap');

/* CSS Variables */
--font-heading: 'Fraunces', serif;
--font-body: 'Outfit', sans-serif;
```

### Heading Styles

| Element | Font | Size | Weight | Line Height |
|---------|------|------|--------|-------------|
| H1 | Fraunces | 48px (clamp 42-64px) | 700 | 1.1 |
| H2 | Fraunces | 36-40px | 600 | 1.2 |
| H3 | Fraunces | 32px | 600 | 1.3 |
| H4 | Fraunces | 22-24px | 600 | 1.4 |

### Body Text

| Type | Font | Size | Weight | Line Height |
|------|------|------|--------|-------------|
| Body Large | Outfit | 18px | 400 | 1.7-1.8 |
| Body Regular | Outfit | 16px | 400 | 1.6 |
| Body Small | Outfit | 14px | 400 | 1.6 |
| Caption | Outfit | 12-13px | 500-600 | 1.4 |

### Eyebrow/Label Text

```css
.eyebrow {
    font-family: 'Outfit', sans-serif;
    font-size: 12-13px;
    font-weight: 600-700;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: #4DD0E1; /* cyan */
}
```

---

## 2. Color Palette

### Primary Colors

| Name | Hex | RGB | Usage |
|------|-----|-----|-------|
| **Deep Navy** | `#0A2540` | 10, 37, 64 | Headers, footers, dark sections, text |
| **Cyan** | `#4DD0E1` | 77, 208, 225 | Primary buttons, accents, highlights |
| **Cyan Dark** | `#3BBCC9` | 59, 188, 201 | Button hover states |
| **Gold** | `#E8B84A` | 232, 184, 74 | Special highlights, premium features |

### Secondary Colors

| Name | Hex | Usage |
|------|-----|-------|
| **Coral** | `#FF6B6B` | Alerts, special offers, CTAs |
| **Light Blue** | `#E8F4F8` | Card backgrounds, subtle highlights |
| **Section Blue** | `#F0F7FA` | Section backgrounds |

### Neutral Colors

| Name | Hex | Usage |
|------|-----|-------|
| **White** | `#FFFFFF` | Backgrounds, text on dark |
| **Gray 100** | `#F5F7FA` | Light backgrounds |
| **Gray 200** | `#E5E7EB` | Borders, dividers |
| **Gray 500** | `#6B7280` | Secondary text, captions |
| **Gray 700** | `#374151` | Body text |
| **Gray 900** | `#1F2933` | Headings, primary text |

### CSS Variables (Copy to Webflow)

```css
:root {
    --deep-navy: #0A2540;
    --cyan: #4DD0E1;
    --cyan-dark: #3BBCC9;
    --gold: #E8B84A;
    --coral: #FF6B6B;
    --light-blue: #E8F4F8;
    --section-blue: #F0F7FA;
    --white: #FFFFFF;
    --gray-100: #F5F7FA;
    --gray-200: #E5E7EB;
    --gray-500: #6B7280;
    --gray-700: #374151;
    --gray-900: #1F2933;
}
```

---

## 3. Spacing System

### Section Padding

| Screen | Vertical Padding |
|--------|-----------------|
| Desktop | 80-100px |
| Tablet | 60-80px |
| Mobile | 48-60px |

### Container

```css
.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 24px;
}
```

### Common Spacing Values

| Size | Value | Usage |
|------|-------|-------|
| XS | 8px | Icon gaps, tight spacing |
| SM | 12px | List items, small gaps |
| MD | 16px | Paragraph margins |
| LG | 24px | Card padding, section gaps |
| XL | 32px | Major section gaps |
| 2XL | 48px | Between content blocks |
| 3XL | 60-80px | Between sections |

---

## 4. Buttons

### Primary Button (Cyan)

```css
.btn-primary {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    background: #4DD0E1;
    color: #0A2540;
    padding: 16px 32px;
    border-radius: 8px;
    font-family: 'Outfit', sans-serif;
    font-weight: 700;
    font-size: 15-16px;
    text-decoration: none;
    transition: all 0.3s ease;
}

.btn-primary:hover {
    background: #FFFFFF;
    transform: translateY(-2px);
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
}
```

### Secondary Button (Outline)

```css
.btn-secondary {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    background: transparent;
    border: 2px solid rgba(255, 255, 255, 0.4);
    color: #FFFFFF;
    padding: 14px 30px;
    border-radius: 8px;
    font-family: 'Outfit', sans-serif;
    font-weight: 600;
    font-size: 15-16px;
    text-decoration: none;
    transition: all 0.3s ease;
}

.btn-secondary:hover {
    border-color: #FFFFFF;
    background: rgba(255, 255, 255, 0.1);
}
```

### Nav CTA Button

```css
.nav-cta {
    background: #4DD0E1;
    color: #0A2540;
    padding: 12px 24px;
    border-radius: 6px;
    font-weight: 600;
    transition: all 0.3s;
}

.nav-cta:hover {
    background: #3BBCC9;
    transform: translateY(-1px);
}
```

---

## 5. Cards

### Project Card

```css
.project-card {
    background: #FFFFFF;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 4px 20px rgba(10, 37, 64, 0.08);
    transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
}

.project-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 20px 40px rgba(10, 37, 64, 0.15);
}
```

### Service Card

```css
.service-card {
    background: #FFFFFF;
    border-radius: 12px;
    padding: 32px;
    box-shadow: 0 2px 12px rgba(10, 37, 64, 0.06);
    transition: all 0.3s;
}

.service-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 12px 32px rgba(10, 37, 64, 0.1);
}
```

### Card Image Aspect Ratios

| Type | Ratio |
|------|-------|
| Standard | 4:3 |
| Featured | 16:12 |
| Square | 1:1 |
| Wide | 16:9 |

---

## 6. Header

### Desktop Header

```css
.header {
    background: #0A2540;
    padding: 16px 0;
    position: fixed;
    width: 100%;
    top: 0;
    z-index: 1000;
}
```

### Logo

```css
.logo {
    font-family: 'Fraunces', serif;
    font-size: 24px;
    font-weight: 700;
    color: #FFFFFF;
    letter-spacing: 2px;
    text-transform: uppercase;
}

.logo span {
    color: #4DD0E1;
}
```

### Navigation Links

```css
.nav a {
    color: rgba(255, 255, 255, 0.85);
    font-family: 'Outfit', sans-serif;
    font-size: 14px;
    font-weight: 500;
    transition: color 0.2s;
}

.nav a:hover {
    color: #FFFFFF;
}
```

---

## 7. Footer

### Footer Container

```css
.footer {
    background: #0A2540;
    padding: 60px 0 32px;
    text-align: center;
}
```

### Footer Logo

```css
.footer-logo {
    font-family: 'Fraunces', serif;
    font-size: 28px;
    font-weight: 700;
    color: #FFFFFF;
    letter-spacing: 3px;
    text-transform: uppercase;
}

.footer-logo span {
    color: #4DD0E1;
}
```

### Footer Column Heading

```css
.footer-col h4 {
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 1px;
    text-transform: uppercase;
    color: #4DD0E1;
    margin-bottom: 16px;
}
```

### Footer Links

```css
.footer-col a {
    color: rgba(255, 255, 255, 0.65);
    font-size: 14px;
    transition: color 0.2s;
}

.footer-col a:hover {
    color: #FFFFFF;
}
```

---

## 8. Animations

### Scroll Reveal (Fade In Up)

```css
.fade-in-up {
    opacity: 0;
    transform: translateY(40px);
    transition: opacity 0.8s cubic-bezier(0.16, 1, 0.3, 1),
                transform 0.8s cubic-bezier(0.16, 1, 0.3, 1);
}

.fade-in-up.visible {
    opacity: 1;
    transform: translateY(0);
}
```

### Hero Animation (Page Load)

```css
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* Staggered delays */
.hero-eyebrow { animation-delay: 0.1s; }
.hero h1 { animation-delay: 0.2s; }
.hero-text { animation-delay: 0.3s; }
.stats-row { animation-delay: 0.4s; }
.hero-cta { animation-delay: 0.5s; }
```

### Hover Transitions

```css
/* Button hover lift */
transform: translateY(-2px);

/* Card hover lift */
transform: translateY(-8px);

/* Image zoom on hover */
.card-image img:hover {
    transform: scale(1.05);
}

/* Timing function for smooth animations */
transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
```

---

## 9. Special Elements

### Wave Divider SVG

```html
<div class="wave-divider">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
        <path d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z" opacity=".25" fill="#FFFFFF"></path>
        <path d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z" opacity=".5" fill="#FFFFFF"></path>
        <path d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z" fill="#FFFFFF"></path>
    </svg>
</div>
```

```css
.wave-divider {
    position: relative;
    width: 100%;
    overflow: hidden;
    line-height: 0;
}

.wave-divider svg {
    display: block;
    width: calc(100% + 1.3px);
    height: 60px;
}

/* Flip for top of section */
.wave-divider.top {
    transform: rotate(180deg);
}
```

### Noise Texture Overlay

```css
.texture-overlay::before {
    content: '';
    position: absolute;
    inset: 0;
    background: url("data:image/svg+xml,%3Csvg viewBox='0 0 400 400' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.8' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)'/%3E%3C/svg%3E");
    opacity: 0.03;
    pointer-events: none;
}
```

### Water Texture Gradient

```css
.water-texture::after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 200px;
    background: radial-gradient(ellipse at 50% 0%, rgba(77, 208, 225, 0.08) 0%, transparent 70%);
    pointer-events: none;
}
```

---

## 10. Responsive Breakpoints

| Breakpoint | Width | Usage |
|------------|-------|-------|
| Desktop | 1200px+ | Full layout |
| Tablet | 768px - 1024px | 2-column grids |
| Mobile | < 768px | Single column, hamburger nav |

### Key Responsive Changes

**At 768px:**
- Navigation becomes hamburger menu
- Grid layouts become single column
- Font sizes reduce by ~15-20%
- Section padding reduces to 60px

---

## 11. File Structure

```
nebo-pools-design/
├── index.html                    # Location page template (v4)
├── portfolio/
│   └── nebo-pools-portfolio-v2.html  # Portfolio/Gallery page
├── project/
│   └── nebo-pools-project-v2.html    # Individual project page
└── STYLE-GUIDE.md               # This file
```

---

## 12. Live Preview URLs

After GitHub Pages is enabled:

| Page | URL |
|------|-----|
| Location Template | `https://veobit.github.io/nebo-pools-location-template/index.html` |
| Portfolio | `https://veobit.github.io/nebo-pools-location-template/portfolio/nebo-pools-portfolio-v2.html` |
| Project | `https://veobit.github.io/nebo-pools-location-template/project/nebo-pools-project-v2.html` |

---

## Notes for Webflow Developer

1. **Fonts**: Add Fraunces and Outfit from Google Fonts in Project Settings
2. **Colors**: Create color swatches using the hex values above
3. **Interactions**: Use Webflow's scroll-triggered animations with the timing functions specified
4. **Wave Dividers**: Can be added as custom code embeds or SVG elements
5. **Mobile Menu**: Use Webflow's native navbar component with custom styling

---

*Generated: February 2026*
*Version: 4.0*
