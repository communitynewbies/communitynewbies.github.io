# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a GitHub Pages site (`communitynewbies.github.io`) serving as a community hub for various local groups and activities in Ghana. The site follows a minimalist approach with a main index page containing a colorful grid layout that links to different community subpages.

## Architecture

### Site Structure
- **Main Landing Page**: `index.html` - A responsive grid layout with color-coded blocks linking to different community groups
- **Community Subpages**: Each community has its own directory with an `index.html` file:
  - `akwasidae/` - Akwasidae Festival event page with calendar integration
  - `poolclub/` - Amateur Pool Club with WhatsApp integration and Google Maps
  - `tumidinner/` - Dinner event page
  - `hag/` - Community group page
  - `logiclounge/` - Logic Lounge community
  - `researchinghana/` - Research community
  - `request/` - Request/contact page (with plus symbol)

### Design Patterns
- **Static HTML**: Pure HTML, CSS, and JavaScript - no build process required
- **Responsive Design**: Mobile-first approach with breakpoints at 768px and 480px
- **Color-coded Navigation**: Each community has a distinct color theme
- **Embedded Services**: Integration with WhatsApp, Google Maps, and calendar services

## Development Guidelines

### CSS Architecture
- Inline styles in `<style>` tags within each HTML file
- CSS reset using `* { margin: 0; padding: 0; box-sizing: border-box; }`
- Responsive breakpoints: 768px (tablet), 480px (mobile)
- Color themes per community (e.g., `#FB923C` for tumidinner, `#3B82F6` for hag)

### JavaScript Patterns
- Vanilla JavaScript for dynamic content generation
- Grid generation using `items` array with color/URL mapping
- Event handling for interactive elements
- Third-party library integration (e.g., add-to-calendar-button)

### HTML Structure
- Semantic HTML5 elements
- Meta tags for viewport and Open Graph
- Accessibility features (aria-labels, proper headings)
- External CDN resources for specialized functionality

## Common Tasks

### Adding New Community
1. Create new directory: `mkdir newcommunity/`
2. Create `index.html` in the new directory
3. Add entry to main `index.html` items array with unique color and URL
4. Follow existing responsive design patterns

### Updating Event Information
- Event pages use structured data in HTML
- Calendar integration requires updating date/time attributes
- Map embeds use Google Maps iframe with specific coordinates

### Styling Guidelines
- Use existing color palette for consistency
- Maintain mobile-responsive design
- Include hover effects and transitions for interactive elements
- Use box-shadow for depth and visual hierarchy

## Deployment

This is a GitHub Pages site that deploys automatically from the main branch. No build process is required - changes to HTML files are immediately reflected on the live site.

## Testing

Test pages locally by opening HTML files in a browser. Ensure:
- Mobile responsiveness across different screen sizes
- External service integration (WhatsApp links, Google Maps, calendar buttons)
- Cross-browser compatibility
- Accessibility features work properly