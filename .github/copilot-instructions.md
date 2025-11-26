# Copilot Instructions for AI Agents

## Project Overview
This is a Hugo-based static site project. The workspace contains content, layouts, assets, and configuration files for building a multilingual website. The main theme is located in `themes/hugo-theme-stack/`.

## Key Architecture & Patterns
- **Content Organization:**
  - Markdown content is under `content/` (posts, pages, categories, etc.).
  - Archetypes for new content are in `archetypes/`.
- **Layouts & Templates:**
  - Hugo templates are in `layouts/` (e.g., `index.html`, `_default/`, `partials/`).
  - Custom partials for articles, pagination, sidebar, and footer are in `layouts/partials/`.
- **Assets:**
  - SCSS, images, and icons are in `assets/`.
  - TypeScript/JS code is in `assets/ts/`.
- **Configuration:**
  - Site config: `hugo.yaml`, `theme.toml`, `netlify.toml`.
  - Multilingual support: `i18n/*.yaml`.

## Developer Workflows
- **Build Site:**
  - Use `hugo` to build and serve the site locally.
  - Custom build scripts may exist (e.g., `debug.sh`).
- **Assets Compilation:**
  - SCSS and TypeScript are compiled by Hugo's asset pipeline.
- **Adding Content:**
  - Use archetypes for new posts/pages: `hugo new post/my-post.md`.
- **Theme Customization:**
  - Modify theme files in `themes/hugo-theme-stack/` or override in `layouts/`.

## Project-Specific Conventions
- **Main Sections:**
  - Defined in `.Site.Params.mainSections` (see `layouts/index.html`).
- **Pagination & Filtering:**
  - Custom logic for filtering and paginating content in `layouts/index.html`.
- **Partial Usage:**
  - Article lists, pagination, and sidebar use partials for modularity.
- **Multilingual:**
  - Content and UI strings are localized via `i18n/*.yaml`.

## Integration Points
- **Netlify:**
  - Deployment configuration in `netlify.toml`.
- **External Data:**
  - Data files in `data/` (e.g., `external.yaml`).

## Examples
- To add a new post: `hugo new post/my-new-post.md` (uses archetype from `archetypes/default.md`).
- To customize homepage layout, edit `layouts/index.html` and related partials.
- To add a new language, create a new YAML file in `i18n/` and update config.

## References
- Hugo documentation: https://gohugo.io/documentation/
- Theme: `themes/hugo-theme-stack/`
- Key files: `layouts/index.html`, `assets/ts/main.ts`, `archetypes/default.md`, `hugo.yaml`

---
_If any section is unclear or missing, please provide feedback for further refinement._
