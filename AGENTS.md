# Repository Guidelines

## Project Structure & Module Organization
This repository is a static website with page-level HTML files at the root:
- `index.html`: main landing page and primary styles/scripts.
- `contact.html`: dedicated contact page with form UI.
- `.gitkeep`: placeholder file only.

There is currently no `src/`, `tests/`, or asset pipeline directory. Keep related markup, CSS, and JavaScript close to the page that uses it unless a shared file structure is introduced.

## Build, Test, and Development Commands
No build step is required.
- `python3 -m http.server 8000` (run in repo root): start a local server.
- `xdg-open http://localhost:8000/index.html` (optional): open the site in a browser.
- `git status`: verify changed files before committing.

If you add tooling (linters/tests), document new commands in this file in the same PR.

## Coding Style & Naming Conventions
Use 2-space indentation in HTML, CSS, and JavaScript to match existing files. Prefer semantic HTML and descriptive class names (for example, `hero-grid`, `section-title`, `contact-wrap`). Keep CSS custom properties in a top-level `:root` block where applicable.

For JavaScript:
- Prefer `const`/`let` over `var` for new code.
- Keep scripts small and page-scoped unless shared behavior is needed.
- Avoid introducing external dependencies for simple interactions.

## Testing Guidelines
This repo has no automated test suite yet. Use manual verification for every change:
1. Serve locally with `python3 -m http.server 8000`.
2. Check `index.html`, `contact.html`, and any touched page in desktop and mobile widths.
3. Validate links, navigation, and form behavior from the browser console/network tab.

When fixing bugs, include clear reproduction and verification steps in the PR description.

## Commit & Pull Request Guidelines
Recent commits use short, sentence-style summaries (for example, `Adds dedicated contact page with form and modern styling`). Follow that style: concise, present tense, and specific to user-visible changes.

For pull requests:
- Include a clear summary of what changed and why.
- Link related issues/tasks when available.
- Add before/after screenshots for UI changes.
- Keep scope focused; separate unrelated updates into different PRs.
