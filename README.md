# Cornice - Image-Text Grid Component

## Overview
The Defcon Image-Text Grid is a responsive, asymmetrical grid component designed for modern web applications. This component features a visually striking layout that combines text content with full-bleed images in an engaging, non-traditional grid pattern. Built with pure HTML and CSS, it offers a lightweight yet sophisticated solution for showcasing content with visual impact.
<img width="1920" height="875" alt="cornice" src="https://github.com/user-attachments/assets/aeb0a8ee-26bc-4e67-b68d-891b0f13646b" />

## Live Preview
**View the component in action:** [Cornice](https://lefajmofokeng.github.io/Cornice)

## Features

### Core Characteristics
- **Asymmetrical Grid Layout**: 2×3 grid with strategic spanning for visual hierarchy
- **Responsive Design**: Adapts gracefully across desktop, tablet, and mobile devices
- **Modern Aesthetic**: Clean typography with a professional color palette
- **Performance Optimized**: Pure CSS implementation with no JavaScript dependencies
- **Accessibility Ready**: Semantic HTML structure with proper image alt attributes

### Layout Structure
The component implements a sophisticated grid pattern:
- **Desktop (≥992px)**: 3-column grid with:
  - Top row: Text (1 column) + Image (2 columns)
  - Bottom row: Image (1 column) + Image (1 column) + Text (1 column)
- **Tablet (768px-992px)**: 2-column grid with all items equally sized
- **Mobile (<768px)**: Single column stack for optimal readability

## Technical Implementation

### CSS Architecture

#### CSS Custom Properties (Variables)
```css
:root {
    --defcon-navy: #06273e;      /* Primary text color */
    --defcon-blue: #0091ff;      /* Accent color (available but not used in current version) */
    --defcon-light-gray: #e5e5e5;/* Background for text blocks */
    --defcon-white: #ffffff;     /* Section background */
    --defcon-black: #000000;     /* Available for future use */
    --font-family-inter: 'Inter', sans-serif;
    --border-radius-1px: 12px;
    --content-max-width: 1100px;
}
```

#### Grid System
The component uses CSS Grid with `grid-template-columns: repeat(3, 1fr)` for the base layout. Strategic use of `grid-column: span` creates the asymmetrical appearance while maintaining a clean underlying structure.

#### Responsive Breakpoints
1. **Default (Desktop)**: 3-column layout with custom spanning
2. **Medium Screens (max-width: 992px)**: 2-column equal grid
3. **Small Screens (max-width: 768px)**: Single column stack

### Typography
- **Primary Font**: Inter (loaded via Google Fonts CDN)
- **Text Hierarchy**:
  - Main text blocks: 1.8rem (700 weight) on desktop, scaling to 1.1rem on mobile
  - Line height: 1.3-1.4 for optimal readability
- **Font Loading Strategy**: Preconnected to fonts.gstatic.com for performance

### Image Handling
- **Object-fit**: `cover` ensures consistent aspect ratio maintenance
- **Height Control**: Fixed to `40vh` for consistent visual proportions
- **Border Radius**: 12px radius applied to all images matching text blocks
- **Accessibility**: All images include descriptive alt text

## Integration Guide

### Basic Implementation
1. Include the HTML structure in your project
2. Ensure the CSS styles are loaded (either inline or in external stylesheet)
3. Update image paths in the `<img>` tags
4. Modify text content as needed

### Customization Options

#### Color Scheme Modification
Edit the CSS custom properties in the `:root` selector to match your brand:
```css
:root {
    --defcon-navy: #your-color;
    --defcon-blue: #your-accent-color;
    --defcon-light-gray: #your-light-background;
}
```

#### Layout Adjustments
- Modify `grid-template-columns` in `.defcon-content-grid` for different column counts
- Adjust `grid-column: span` values in individual item classes for different spanning patterns
- Change breakpoint values in media queries for different device targeting

#### Content Customization
- Replace placeholder images with your own (maintain similar aspect ratios for best results)
- Adjust padding values in `.defcon-grid-item-text` for different text densities
- Modify font sizes in responsive breakpoints for different typography scales

## Browser Compatibility
- **Fully Supported**: Chrome 57+, Firefox 52+, Safari 10.1+, Edge 16+
- **Partial Support**: IE11 (requires polyfills for CSS Grid and CSS Variables)
- **Tested On**: Latest versions of all major browsers

## Performance Considerations
- **CSS Efficiency**: All styles are contained within the component with no external dependencies beyond Google Fonts
- **Image Optimization**: Recommend serving WebP format with fallbacks for maximum performance
- **Font Loading**: Fonts are preconnected for faster loading
- **Render Performance**: Uses modern CSS Grid which is GPU-accelerated in most browsers

## Accessibility Features
- **Semantic HTML**: Proper use of `<section>` and descriptive classes
- **Color Contrast**: Text meets WCAG AA standards against background colors
- **Responsive Text**: Font sizes scale appropriately for different viewports
- **Image Descriptions**: All images include meaningful alt text
- **Keyboard Navigation**: Natural document flow maintained

## Future Enhancements
Potential areas for extension:
1. **JavaScript Integration**: Add intersection observers for scroll-triggered animations
2. **Dynamic Content**: Connect to CMS via JavaScript data binding
3. **Theme Variants**: Create light/dark mode toggle
4. **Interactive Elements**: Add hover effects or click interactions
5. **Lazy Loading**: Implement native lazy loading for images

## File Structure
```
project/
├── index.html              # Main component file
├── cornice.css             # CSS
└── (optional) README.md    # This documentation
```

## License & Attribution
- **Component Code**: Free to use and modify
- **Sample Images**: Placeholder images from Pexels (replace with licensed images for production)
- **Font**: Inter by Rasmus Andersson (Open Font License)

## Support
For issues or questions:
1. Check the live preview for implementation reference
2. Review browser compatibility section
3. Ensure image paths are correctly referenced
4. Validate custom CSS modifications don't break the grid layout

---

*Last Updated: Dec13, 2025*  
*Component Version: 1.0*  
