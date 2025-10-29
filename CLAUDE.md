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

# Mintlify documentation

## Working relationship

- You can push back on ideas-this can lead to better documentation. Cite sources and explain your reasoning when you do so
- ALWAYS ask for clarification rather than making assumptions
- NEVER lie, guess, or make up information

## Project context

- Format: MDX files with YAML frontmatter
- Config: docs.json for navigation, theme, settings
- Components: Mintlify components

## Content strategy

- Document just enough for user success - not too much, not too little
- Prioritize accuracy and usability of information
- Make content evergreen when possible
- Search for existing information before adding new content. Avoid duplication unless it is done for a strategic reason
- Check existing patterns for consistency
- Start by making the smallest reasonable changes

## docs.json

- Refer to the [docs.json schema](https://mintlify.com/docs.json) when building the docs.json file and site navigation

## Frontmatter requirements for pages

- title: Clear, descriptive page title
- description: Concise summary for SEO/navigation

## Writing standards

- Second-person voice ("you")
- Prerequisites at start of procedural content
- Test all code examples before publishing
- Match style and formatting of existing pages
- Include both basic and advanced use cases
- Language tags on all code blocks
- Alt text on all images
- Relative paths for internal links
- **NEVER use emdashes (—) in documentation**: Use colons, commas, or parentheses instead. This is mandatory.

## Git workflow

- NEVER use --no-verify when committing
- Ask how to handle uncommitted changes before starting
- Create a new branch when no clear branch exists for changes
- Commit frequently throughout development
- NEVER skip or disable pre-commit hooks

## Do not

- Skip frontmatter on any MDX file
- Use absolute URLs for internal links
- Include untested code examples
- Make assumptions - always ask for clarification
