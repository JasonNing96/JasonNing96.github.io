# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Quick Start Commands

### Local Development
```bash
# Install dependencies
bundle install

# Run local server with live reload
bundle exec jekyll serve -l -H localhost

# Alternative: Use Docker
docker compose up
```

### Build & Deploy
```bash
# Build for production
bundle exec jekyll build

# Check for broken links (requires html-proofer)
bundle exec htmlproofer ./_site --disable-external
```

### Content Management
```bash
# Generate publications from TSV
python markdown_generator/publications.py

# Generate talks from TSV  
python markdown_generator/talks.py

# Update CV JSON from markdown
bash scripts/update_cv_json.sh
```

## Architecture Overview

This is a **Jekyll-based academic portfolio website** using the Academic Pages template. Key components:

### Content Structure
- **`_posts/`** - Blog posts organized by date
- **`_publications/`** - Research papers in markdown format
- **`_talks/`** - Conference presentations and talks
- **`_teaching/`** - Teaching experience
- **`_portfolio/`** - Project portfolio items
- **`_pages/`** - Static pages (About, CV, etc.)

### Data Sources
- **`_data/cv.json`** - Structured CV data (primary source)
- **`_data/navigation.yml`** - Site navigation
- **`markdown_generator/`** - Python scripts for bulk content generation
- **`files/`** - PDFs, presentations, and other assets

### Styling & Layout
- **`_sass/`** - SCSS stylesheets with themes
- **`_includes/`** - Reusable HTML components
- **`_layouts/`** - Page templates (single, archive, talk, etc.)
- **`assets/`** - CSS, JS, and web fonts

### Key Configurations
- **`_config.yml`** - Jekyll configuration and site metadata
- **`Gemfile`** - Ruby dependencies (Jekyll plugins)
- **`package.json`** - Node.js dependencies for asset building

## Content Workflow

1. **Publications**: Add new papers to `_publications/` or use `markdown_generator/publications.py` with TSV data
2. **CV Updates**: Edit `_data/cv.json` for structured CV data, then run update script to sync markdown CV
3. **Talks**: Add to `_talks/` or use `markdown_generator/talks.py` with TSV data
4. **Blog Posts**: Create new markdown files in `_posts/` with proper front matter

## Deployment

Auto-deploys to GitHub Pages on push to `master` branch. Site available at `https://JasonNing96.github.io`.