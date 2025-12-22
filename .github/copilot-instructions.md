# Copilot Instructions for Moss Barnett WordPress Theme

## Project Overview
This is a WordPress child theme for the "Dictum" parent theme, customizing header styles, menu colors, and layout elements for the Moss Barnett website.

## Architecture
- **styles.css**: Main child theme file with WordPress header comment and core customizations
- **additional.css**: Supplementary styles for additional overrides
- **main.min.css**: Reserved for minified compiled styles (currently empty)

## Key Patterns
- **Override Strategy**: Use `!important` extensively to override parent theme styles
- **Color Scheme**: 
  - Primary: `#6a1b2d` (burgundy) for headers and menu items
  - Secondary: `#f7f2ea` (light cream) for menu text on non-main pages
- **Class Prefixes**: Parent theme uses `qodef-` prefix (e.g., `.qodef-menu-item-text`, `.qodef-page-header`)
- **Page-Specific Styles**: 
  - `.home` for homepage customizations
  - `.page-id-1405` for contact page
  - Hide social share and read-more elements on home/contact

## Development Workflow
- Edit `styles.css` for main customizations
- Use `additional.css` for supplementary styles
- No build process required - direct CSS editing
- Test responsive behavior with mobile breakpoints (max-width: 767px)

## Common Tasks
- **Header Customization**: Target `#qodef-page-header` and nested elements
- **Menu Styling**: Use `.qodef-menu-item-text` for menu link colors
- **Mobile Adjustments**: Override font sizes and alignments in `@media (max-width: 767px)`
- **Element Hiding**: Use `display: none !important` for unwanted parent theme elements

## Examples
```css
/* Hide element on specific pages */
.home #qodef-page-content-bottom {
  display: none !important;
}

/* Menu color override */
.qodef-menu-item-text {
  color: #6a1b2d !important;
}
```