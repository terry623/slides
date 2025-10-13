# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Slidev presentation project for demonstrating monorepo concepts. Slidev is a slide deck tool designed for developers that uses Markdown files for content and Vue.js components for interactive elements.

## Commands

- `pnpm install` - Install dependencies
- `pnpm dev` - Start development server with auto-open at http://localhost:3030
- `pnpm build` - Build presentation for production
- `pnpm export` - Export slides to static files

## Architecture

- **slides.md** - Main presentation file containing all slides in Markdown format with frontmatter configuration
- **components/** - Vue.js components used within slides (e.g., Counter.vue for interactive elements)
- **snippets/** - TypeScript files with code examples referenced in slides using `<<< @/snippets/filename.ts#region` syntax
- **pages/** - Additional slide files that can be imported into main presentation

## Key Conventions

- Slides use frontmatter YAML configuration for theming, transitions, and metadata
- Interactive Vue components can be embedded directly in Markdown slides
- Code snippets support syntax highlighting, line highlighting, and TypeScript hover information
- External code files in snippets/ can be imported with region-specific includes
- Uses Seriph theme by default with UnoCSS for styling