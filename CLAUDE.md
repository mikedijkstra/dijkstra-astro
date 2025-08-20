# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development Commands

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run astro` - Run Astro CLI commands

## Architecture Overview

This is Mike Dijkstra's portfolio website built with Astro 5.2.1, featuring a component-based architecture with static site generation.

### Technology Stack
- **Astro 5.2.1** - Static site generator with TypeScript support
- **Tailwind CSS 4.0** - Styling with custom design tokens
- **Alpine.js** - Lightweight JavaScript for interactive components
- **MDX** - Content authoring support

### Key Directories
- `src/components/` - Reusable Astro components (LinkList, Work, Button, SiteNav)
- `src/layouts/` - Page layouts (BaseLayout.astro provides consistent structure)
- `src/pages/` - File-based routing (services/, work/ subdirectories for content organization)
- `src/assets/` - Optimized images and media
- `src/styles/` - Global CSS and design system

### Component Architecture
- **BaseLayout.astro** - Main layout template with navigation and meta tags
- **SiteNav.astro** - Responsive navigation with Alpine.js mobile menu
- **LinkList.astro** - Flexible link component with descriptions and animations
- **Work.astro** - Portfolio showcase component with gallery support

### Design System
- **Color Palette**: Gulf blue (#03115b), Crimson (#eb0052), Torch (#fc0c1b)
- **Typography**: Custom "Anarchy-Book" font with system fallbacks
- **Custom CSS Properties**: Defined in `src/styles/global.css`

### Content Management
- Work items and services are defined as JavaScript objects in component files
- Images stored in both `src/assets/` (optimized) and `public/images/` (static)
- Uses Astro's Picture component for responsive images

### Interactive Features
- Touch detection for hover states (`src/components/SiteNav.astro`)
- Alpine.js state management for mobile navigation
- CSS counter implementation for numbered lists
- Custom link animations with right arrow effects

### Build Configuration
- Site URL: `https://dijkstra.com.au` (configured in astro.config.mjs)
- Static generation targeting GitHub Pages deployment
- Vite integration with Tailwind CSS plugin
- TypeScript strict mode enabled

### Code Quality
- Prettier configured with Astro plugin for consistent formatting
- ES modules throughout codebase
- Component props properly typed with TypeScript