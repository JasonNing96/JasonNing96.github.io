# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Quick Start Commands

### Local Development
```bash
# Install dependencies
bundle install

# Fix permission errors during install (if needed)
bundle config set --local path 'vendor/bundle'
bundle install

# Run local server with live reload
bundle exec jekyll serve -l -H localhost

# Alternative: Use Docker
docker compose up

# Alternative: Use VS Code DevContainer
# Press F1 -> "DevContainer: Reopen in Container"
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
# Generate publications from TSV (run from markdown_generator/)
python markdown_generator/publications.py

# Generate talks from TSV (run from markdown_generator/)
python markdown_generator/talks.py

# Update CV JSON from markdown
bash scripts/update_cv_json.sh
```

## Architecture Overview

This is a **Jekyll-based academic portfolio website** using the Academic Pages template. Key components:

### Content Structure
- **`_posts/`** - Blog posts organized by date (YYYY-MM-DD-title.md format)
- **`_publications/`** - Research papers with frontmatter metadata
- **`_talks/`** - Conference presentations with location data for talkmap integration
- **`_teaching/`** - Teaching experience and workshops
- **`_portfolio/`** - Project portfolio items
- **`_pages/`** - Static pages (About, CV, sitemap, etc.)

### Data Sources
- **`_data/cv.json`** - Structured CV data following JSON Resume standard (primary source)
- **`_data/navigation.yml`** - Site navigation structure
- **`markdown_generator/`** - Python scripts for bulk content generation from TSV files
- **`files/`** - PDFs, presentations, and other assets (accessible at /files/*)

### Styling & Layout
- **`_sass/`** - SCSS stylesheets with modular organization (theme/, include/, layout/, vendor/)
- **`_includes/`** - Reusable HTML components (author-profile, seo, comments, footer, etc.)
- **`_layouts/`** - Page templates (single, talk, cv-layout, archive)
- **`assets/`** - CSS, JS, and web fonts

### Key Configurations
- **`_config.yml`** - Jekyll configuration, site metadata, collection settings, author profile
- **`Gemfile`** - Ruby dependencies (Jekyll plugins including jekyll-feed, jekyll-sitemap, jemoji)
- **`package.json`** - Node.js dependencies for asset building (jQuery, Fitvids, UglifyJS)

## Content Workflow

1. **Publications**: Add new papers to `_publications/` with frontmatter, or use `markdown_generator/publications.py` with TSV data containing columns: pub_date, title, venue, excerpt, citation, site_url, paper_url, url_slug

2. **CV Updates**: Edit `_pages/cv.md` for human editing, then run `scripts/update_cv_json.sh` to sync to `_data/cv.json`. The Python script `scripts/cv_markdown_to_json.py` handles conversion.

3. **Talks**: Add to `_talks/` with location data (venue location for geolocation), or use `markdown_generator/talks.py` with TSV data. Location data feeds into the talkmap visualization.

4. **Blog Posts**: Create new markdown files in `_posts/` with Jekyll front matter (title, date, categories, etc.)

## Unique Features

### Talkmap Visualization
- Interactive Leaflet map showing all talk locations
- Uses `talkmap.ipynb` Jupyter notebook for geocoding
- GitHub Action workflow `.github/workflows/scrape_talks.yml` automatically updates on changes to talks directory
- Enable/disable with `talkmap_link: true/false` in `_config.yml`

### Dual CV System
- Markdown CV (`_pages/cv.md`) for human editing
- JSON CV (`_data/cv.json`) for structured data display
- Synchronization via `scripts/update_cv_json.sh`

### Publication Categories
Configured in `_config.yml` under `publication_category`:
- `books` - Published books
- `manuscripts` - Journal articles
- `conferences` - Conference papers

## Deployment

Auto-deploys to GitHub Pages on push to `master` branch. Site available at `https://JasonNing96.github.io`.

Docker and VS Code DevContainer support available for consistent development environments.