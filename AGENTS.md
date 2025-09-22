# Repository Guidelines

## Project Structure & Module Organization
Core site configuration lives in `_config.yml`, `_includes`, `_layouts`, and `_sass`. Landing page copy and layout are in `index.html` and `_pages/`, while brand assets sit under `assets/` (grouped into `screenshot/`, `videos/`, and theme images). Global styles compile from `main.scss`; GitHub Pages reads front matter from every top-level template.

## Build, Test, and Development Commands
Run `bundle install` once to fetch the `github-pages` gem suite. Use `bundle exec jekyll serve --livereload` for a local preview at `http://127.0.0.1:4000`, and `bundle exec jekyll build` to produce the static `_site/` bundle that GitHub Pages publishes. When developing new assets, clear `_site/` if you notice stale build artefacts.

## Coding Style & Naming Conventions
Follow the existing HTML with 4-space indentation and attribute values in double quotes. SCSS variables mirror `_config.yml` keys; keep names kebab-case for classes (`.feature-item`) and snake_case for Liquid variables. Update YAML lists with 2-space indents and wrap text at roughly 100 characters to keep diffs readable. Run `bundle exec jekyll build` before committing to surface Liquid or YAML syntax errors.

## Testing Guidelines
There is no automated test harness; rely on `jekyll serve` to validate Liquid rendering and inspect pages (`/`, `/changelog`, `/privacypolicy`). Verify that new assets have correct dimensions (see README resolutions) and load paths. Document any manual test checklist in the pull request if behavior changes.

## Commit & Pull Request Guidelines
Recent commits (`update icons`, `remove presskit link`) use short, imperative subjects; follow that tone and keep body text optional. For pull requests, include: purpose summary, screenshots or GIFs for visual updates, steps to reproduce or verify locally, and any config keys that contributors must tweak. Reference linked issues with `Fixes #ID` when applicable.

## Deployment & Configuration Tips
GitHub Pages rebuilds automatically on push. When introducing new copy or branding, update `_config.yml` first, then mirror values in `main.scss` only if computed styles are required. Store private assets elsewhere—this repo is fully public.
