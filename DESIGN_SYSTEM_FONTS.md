# 🎨 Design System Fonts Implementation

## ✅ Complete Font System Setup

All fonts throughout the website now follow the design system JSON specifications.

---

## 📚 Font Families

### Display Font (Headings)
**Playfair Display** - Serif
- Usage: Large headings, hero titles, impactful statements
- Weights: 400, 600, 700, 900
- CSS Variable: `--font-display`

### Body Font (Content)
**Roboto** - Sans-serif
- Usage: Paragraphs, descriptions, readable content
- Weights: 300, 400, 500, 600, 700
- CSS Variable: `--font-body`

### UI Font (Interface)
**Poppins** - Sans-serif
- Usage: Buttons, navigation, UI elements
- Weights: 400, 500, 600, 700
- CSS Variable: `--font-ui`

### Accent Font (Labels)
**Montserrat** - Sans-serif
- Usage: Badges, labels, eyebrow text, uppercase elements
- Weights: 400, 500, 600, 700
- CSS Variable: `--font-accent`

---

## 📏 Font Sizes (Fluid Typography)

```css
--font-size-hero: clamp(2.6rem, 4.8vw, 3.6rem)
--font-size-h1: clamp(2.25rem, 6vw, 3.5rem)
--font-size-h2: clamp(2rem, 5vw, 2.75rem)
--font-size-h3: 1.375rem
--font-size-h4: 1.25rem
--font-size-body: 1.0625rem
--font-size-body-small: 0.9375rem
--font-size-label: 0.8125rem
```

---

## ⚖️ Font Weights

```css
--font-weight-light: 300
--font-weight-regular: 400
--font-weight-medium: 500
--font-weight-semibold: 600
--font-weight-bold: 700
--font-weight-extrabold: 900
```

---

## 📐 Line Heights

```css
--line-height-tight: 1.2      /* For headings */
--line-height-normal: 1.5     /* For UI elements */
--line-height-relaxed: 1.7    /* For body text */
```

---

## 🔤 Letter Spacing

```css
--letter-spacing-tight: -0.02em    /* Large headings */
--letter-spacing-normal: 0         /* Default */
--letter-spacing-wide: 0.1em       /* Uppercase labels */
--letter-spacing-wider: 0.15em     /* Badges */
```

---

## 🎯 Usage Examples

### Headings
```css
h1 {
  font-family: var(--font-display);
  font-size: var(--font-size-h1);
  font-weight: var(--font-weight-bold);
  line-height: var(--line-height-tight);
  letter-spacing: var(--letter-spacing-tight);
}
```

### Body Text
```css
p {
  font-family: var(--font-body);
  font-size: var(--font-size-body);
  line-height: var(--line-height-relaxed);
}
```

### Buttons
```css
button {
  font-family: var(--font-ui);
  font-size: 1rem;
  font-weight: var(--font-weight-semibold);
}
```

### Badges/Labels
```css
.badge {
  font-family: var(--font-accent);
  font-size: var(--font-size-label);
  font-weight: var(--font-weight-semibold);
  text-transform: uppercase;
  letter-spacing: var(--letter-spacing-wide);
}
```

---

## 📋 Typography Hierarchy

### Hero Section
- Font: Playfair Display
- Size: clamp(2.6rem, 4.8vw, 3.6rem)
- Weight: 700
- Line Height: 1.2
- Letter Spacing: -0.02em

### H1 (Page Titles)
- Font: Playfair Display
- Size: clamp(2.25rem, 6vw, 3.5rem)
- Weight: 700
- Line Height: 1.2
- Letter Spacing: -0.02em

### H2 (Section Titles)
- Font: Playfair Display
- Size: clamp(2rem, 5vw, 2.75rem)
- Weight: 700
- Line Height: 1.2

### H3 (Card Titles)
- Font: Poppins
- Size: 1.375rem
- Weight: 600
- Line Height: 1.3

### Body Text
- Font: Roboto
- Size: 1.0625rem
- Weight: 400
- Line Height: 1.7

### Small Text
- Font: Roboto
- Size: 0.9375rem
- Weight: 400
- Line Height: 1.6

### Labels
- Font: Poppins
- Size: 0.8125rem
- Weight: 600
- Line Height: 1.5

### Badges/Eyebrow
- Font: Montserrat
- Size: 0.8125rem
- Weight: 600
- Text Transform: Uppercase
- Letter Spacing: 0.1em

---

## 🎨 Component Font Usage

### Navbar
- Logo: Poppins, 700
- Links: Poppins, 500
- CTA Button: Poppins, 600

### Hero
- Eyebrow: Montserrat, 600, uppercase
- Title: Playfair Display, 700
- Subtitle: Roboto, 400
- Buttons: Poppins, 600

### Service Cards
- Title: Poppins, 600
- Description: Roboto, 400
- Bullet Points: Roboto, 400

### Service Detail Pages
- Badge: Montserrat, 600, uppercase
- Title: Playfair Display, 700
- Description: Roboto, 400
- Section Titles: Playfair Display, 700
- Body Text: Roboto, 400
- Process Labels: Poppins, 600

### Contact Form
- Labels: Poppins, 600
- Input Text: Roboto, 400
- Button: Poppins, 600
- Info Labels: Montserrat, 600, uppercase

### Toast Notifications
- Message: Roboto, 500

---

## 📱 Responsive Typography

### Desktop (> 900px)
- Hero: 3.6rem
- H1: 3.5rem
- H2: 2.75rem
- Body: 1.0625rem

### Tablet (768px - 900px)
- Hero: ~3rem
- H1: ~2.75rem
- H2: ~2.25rem
- Body: 1.0625rem

### Mobile (< 768px)
- Hero: 2.6rem
- H1: 2.25rem
- H2: 2rem
- Body: 1rem

---

## 🔧 CSS Variables Setup

All font variables are defined in `globals.css`:

```css
:root {
  /* Font Families */
  --font-display: 'Playfair Display', serif;
  --font-body: 'Roboto', sans-serif;
  --font-ui: 'Poppins', sans-serif;
  --font-accent: 'Montserrat', sans-serif;
  
  /* Font Sizes */
  --font-size-hero: clamp(2.6rem, 4.8vw, 3.6rem);
  --font-size-h1: clamp(2.25rem, 6vw, 3.5rem);
  --font-size-h2: clamp(2rem, 5vw, 2.75rem);
  --font-size-h3: 1.375rem;
  --font-size-h4: 1.25rem;
  --font-size-body: 1.0625rem;
  --font-size-body-small: 0.9375rem;
  --font-size-label: 0.8125rem;
  
  /* Font Weights */
  --font-weight-light: 300;
  --font-weight-regular: 400;
  --font-weight-medium: 500;
  --font-weight-semibold: 600;
  --font-weight-bold: 700;
  --font-weight-extrabold: 900;
  
  /* Line Heights */
  --line-height-tight: 1.2;
  --line-height-normal: 1.5;
  --line-height-relaxed: 1.7;
  
  /* Letter Spacing */
  --letter-spacing-tight: -0.02em;
  --letter-spacing-normal: 0;
  --letter-spacing-wide: 0.1em;
  --letter-spacing-wider: 0.15em;
}
```

---

## 📦 Font Loading

Fonts are loaded via Google Fonts:

```css
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700;900&family=Roboto:wght@300;400;500;600;700&family=Poppins:wght@400;500;600;700&family=Montserrat:wght@400;500;600;700&display=swap');
```

**Loaded Weights:**
- Playfair Display: 400, 600, 700, 900
- Roboto: 300, 400, 500, 600, 700
- Poppins: 400, 500, 600, 700
- Montserrat: 400, 500, 600, 700

---

## 🎯 Design Principles

### 1. Clear Hierarchy
- Display fonts for headings
- Sans-serif for body
- Consistent sizing scale

### 2. Readability
- Line height 1.7 for body text
- Adequate font sizes
- Proper contrast

### 3. Consistency
- Use CSS variables
- Follow design system
- Maintain hierarchy

### 4. Performance
- Load only needed weights
- Use font-display: swap
- Optimize loading

### 5. Accessibility
- Minimum 16px body text
- High contrast ratios
- Scalable fonts

---

## ✅ Implementation Checklist

- [x] Import Google Fonts
- [x] Define CSS variables
- [x] Set up font families
- [x] Configure font sizes
- [x] Set font weights
- [x] Define line heights
- [x] Set letter spacing
- [x] Apply to body
- [x] Style headings
- [x] Style buttons
- [x] Style labels
- [x] Style badges
- [x] Test responsive scaling
- [x] Verify accessibility

---

## 🚀 Benefits

### Before
- Inconsistent fonts
- Mixed font families
- No design system
- Hard to maintain

### After
- ✅ Consistent typography
- ✅ Design system compliant
- ✅ Easy to maintain
- ✅ Professional appearance
- ✅ Better readability
- ✅ Scalable system

---

## 📚 Resources

- **Design System:** `design-system.json`
- **Global Styles:** `src/styles/globals.css`
- **Google Fonts:** https://fonts.google.com

---

**🎉 Typography system is now fully aligned with the design system!**

All fonts follow the specifications from `design-system.json` for a consistent, professional appearance.
