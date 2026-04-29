---
name: Intellectual Editorial
colors:
  surface: '#fcf9f8'
  surface-dim: '#dcd9d9'
  surface-bright: '#fcf9f8'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f6f3f2'
  surface-container: '#f0eded'
  surface-container-high: '#eae7e7'
  surface-container-highest: '#e5e2e1'
  on-surface: '#1c1b1c'
  on-surface-variant: '#41493e'
  inverse-surface: '#313030'
  inverse-on-surface: '#f3f0f0'
  outline: '#717a6d'
  outline-variant: '#c0c9bb'
  surface-tint: '#2e6b2f'
  primary: '#002c06'
  on-primary: '#ffffff'
  primary-container: '#00450d'
  on-primary-container: '#74b46e'
  inverse-primary: '#95d78e'
  secondary: '#705d00'
  on-secondary: '#ffffff'
  secondary-container: '#fce17e'
  on-secondary-container: '#766307'
  tertiary: '#705d00'
  on-tertiary: '#ffffff'
  tertiary-container: '#c5aa3c'
  on-tertiary-container: '#4c3f00'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#b0f3a7'
  primary-fixed-dim: '#95d78e'
  on-primary-fixed: '#002203'
  on-primary-fixed-variant: '#135219'
  secondary-fixed: '#fce17e'
  secondary-fixed-dim: '#dfc566'
  on-secondary-fixed: '#221b00'
  on-secondary-fixed-variant: '#544600'
  tertiary-fixed: '#ffe16e'
  tertiary-fixed-dim: '#e1c554'
  on-tertiary-fixed: '#221b00'
  on-tertiary-fixed-variant: '#544600'
  background: '#fcf9f8'
  on-background: '#1c1b1c'
  surface-variant: '#e5e2e1'
typography:
  display-lg:
    fontFamily: Newsreader
    fontSize: 64px
    fontWeight: '400'
    lineHeight: '1.1'
    letterSpacing: -0.02em
  display-md:
    fontFamily: Newsreader
    fontSize: 48px
    fontWeight: '400'
    lineHeight: '1.1'
  headline-lg:
    fontFamily: Newsreader
    fontSize: 32px
    fontWeight: '500'
    lineHeight: '1.2'
  headline-md:
    fontFamily: Newsreader
    fontSize: 24px
    fontWeight: '500'
    lineHeight: '1.3'
  body-lg:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
  label-lg:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '600'
    lineHeight: '1.2'
    letterSpacing: 0.05em
  label-sm:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '500'
    lineHeight: '1.2'
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  base: 8px
  section-gap: 80px
  golden-ratio-thin: 38.2%
  golden-ratio-wide: 61.8%
  gutter: 24px
  margin: 32px
---

## Brand & Style

The design system embodies the **Academic Vanguard**—a fusion of historic institutional authority and the kinetic energy of modern intellectual youth. It is built to serve as a digital broadsheet for scholarly discourse and community leadership. 

The aesthetic leans heavily into **High-End Editorial** styling. It prioritizes clarity, prestige, and "The Power of the Word." This is achieved through a Minimalist foundation punctuated by sophisticated Glassmorphism and asymmetric compositions that break the monotony of standard corporate layouts. The goal is to evoke the feeling of reading a premium journal where every piece of information has been curated with intentionality and rigor.

## Colors

The palette is anchored in a deep, scholarly green representing growth and institutional legacy. 

- **Primary & Container:** Used for core branding and high-importance UI elements. The gradient between these two greens creates depth without relying on shadows.
- **Gold Accents:** The Gold Dark and Light shades are reserved for "Excellence" markers, such as awards, premium tags, or highlighted scholarly contributions.
- **Neutrality:** The Charcoal (#5f5e5e) is the primary color for body text to reduce eye strain, while the Surface Low (#f3f3f3) provides a subtle tier of separation for secondary content areas.
- **Interaction:** State changes should favor subtle opacity shifts or background shifts toward the Primary Container rather than introduce new hues.

## Typography

This design system utilizes a high-contrast typographic pairing to signal intellectual authority.

- **Newsreader:** This serif face is the voice of the institution. Use it for all display text and headlines. It should be sized generously to allow its elegant terminals and classic proportions to breathe.
- **Inter:** A functional, neutral workhorse used for the UI and long-form body copy. Its high legibility balances the expressive nature of the serif headlines.
- **Hierarchy Rules:** Maintain a clear vertical rhythm. Headlines should always have significantly more "top-room" than "bottom-room" to create a structured, editorial flow. Labels should frequently use uppercase with slight tracking to differentiate UI metadata from content.

## Layout & Spacing

The layout philosophy rejects the standard symmetrical grid in favor of **Intentional Asymmetry** driven by the Golden Ratio.

- **The 38/62 Split:** Primary layouts (such as landing pages or dashboards) should divide their horizontal space into a 38% auxiliary column and a 62% content column. This creates a natural focal point that feels "designed" rather than merely "placed."
- **Expansive Whitespace:** Content must not feel crowded. Use the `section-gap` for vertical spacing between major themes to allow the user to digest information.
- **Margins & Gutters:** A 12-column fluid grid is used for internal component placement, but the overall page wrapper should maintain wide margins to simulate the feel of a printed broadsheet.

## Elevation & Depth

Depth in this design system is achieved through atmospheric effects rather than physical barriers.

- **Glassmorphism:** The sticky Navbar uses a backdrop-blur (12-20px) with a semi-transparent white (#ffffff90) fill. This keeps the user grounded in their scroll position while maintaining a light, modern feel.
- **Ambient Shadows:** Shadows should be extremely soft, utilizing the Primary color (#00450d) at 4-8% opacity for the tint. Avoid generic grey shadows to maintain the "Academic Vanguard" color profile.
- **Surface Tiering:** Use Tonal Layers (Surface to Surface Low) to create hierarchy. No 1px black borders are allowed; instead, use 1px strokes of #1b5e20 at 10% opacity for subtle definition if a border is strictly necessary.

## Shapes

The shape language is controlled and sophisticated. 

- **Corner Radius:** A base of 0.25rem (Soft) is used for small elements like tags or inputs. Larger elements like Cards and Buttons utilize the `rounded-xl` (0.75rem) specification to soften the "intellectual" sharpness with "youthful" energy.
- **Visual Weight:** Elements should feel like high-quality stationery. Cards should have no border, relying on a subtle background shift (from White to Surface Low) on hover to indicate interactivity.

## Components

### Buttons
Primary buttons feature a **135-degree gradient** from Primary (#00450d) to Primary Container (#1b5e20). The corner radius is strictly **0.75rem**. Typography inside buttons should be Inter Bold, Uppercase, 14px.

### Cards
Cards are clean, white containers with ambient shadows. Upon hover, they should undergo a "Background Shift"—transforming the surface color or slightly enlarging the shadow—while maintaining the 0.75rem radius.

### Sticky Navbar
The Navbar is fixed to the top with a glassmorphism effect. It must have a blur radius of 12-20px. Navigation links use Inter 14px Medium with a subtle Gold Dark underline for the active state.

### Input Fields
Inputs are minimalist, using Surface Low (#f3f3f3) as the fill color and a 0.25rem radius. The focus state replaces the borderless look with a soft Primary color glow.

### Editorial Accents
Include "Pull Quotes" using Newsreader Italic and "Vertical Dividers" that follow the 38/62 split lines to reinforce the editorial theme.