# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Mintlify documentation site for Dimedove's API documentation. The project uses the Mintlify platform with the "maple" theme to create and host documentation.

## Development Commands

### Local Development
```bash
# Install Mintlify CLI globally (Node.js 18.10.0+ required)
npm i -g mintlify

# Start local development server
mintlify dev

# Start on custom port
mintlify dev --port 3333
```

The local development server runs at `http://localhost:3000` by default.

### Updates and Deployment
```bash
# Update Mintlify CLI to latest version
npm i -g mintlify@latest

# Deployment is handled automatically via GitHub app
# Just commit and push changes to trigger deployment
```

## Architecture

### Configuration
- **docs.json**: Main configuration file defining navigation, theme, colors, and site settings
- Uses Mintlify's "maple" theme with Inter font family
- Primary color: #0f0e0d, with light/dark mode support

### Content Structure
- **MDX files**: All documentation content uses MDX format (Markdown + React components)
- **Navigation groups**: 
  - Get Started (welcome, quickstart, development)
  - Essentials (markdown, code, images, settings, navigation, reusable-snippets)
  - Webhooks (introduction)
  - Legal (terms, privacy)

### Assets
- **favicon.ico**: Site favicon
- **images/**: Contains hero images and logos
  - `hero-light.png` / `hero-dark.png`: Main hero images
  - `logos/light.png` / `logos/dark.png`: Brand logos
- **snippets/**: Reusable content snippets

### Mintlify Components
The project uses Mintlify's built-in components:
- `<Card>` and `<CardGroup>`: For feature showcases
- `<Accordion>` and `<AccordionGroup>`: For collapsible content
- `<CodeGroup>`: For multiple code examples
- `<Frame>`: For image containers
- `<Info>`, `<Tip>`: For callout boxes

## File Editing Guidelines

- All content files use `.mdx` extension
- Front matter includes `title`, `sidebarTitle`, and `description`
- Use Mintlify components for enhanced layouts
- Images should reference paths relative to the docs root (e.g., `/images/hero-light.png`)
- Navigation structure is defined in `docs.json`, not inferred from file structure