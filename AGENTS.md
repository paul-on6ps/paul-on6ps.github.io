# Repository Guidelines

## Project Structure & Module Organization
- Keep site entry points (for example `index.html`, `about.md`) in the repository root alongside `README.md`.
- Store shared media in `assets/`; use descriptive names like the existing `assets/Voorbeeld_Antenne.jpeg`.
- Group any future scripts or styles under dedicated folders (`scripts/`, `styles/`) to avoid cluttering the root.

## Build, Test, and Development Commands
- `python3 -m http.server 4000` – Serve the site locally at http://localhost:4000 for quick smoke checks.
- `npx serve .` – Alternative static preview if Node.js is available.
- `npx prettier --check "**/*.{html,css,js,json,md}"` – Verify formatting before committing (install Prettier once with `npm install --global prettier`).

## Coding Style & Naming Conventions
- Use two-space indentation for HTML, CSS, and any front matter to keep diffs small.
- Prefer lowercase, hyphenated file names (`about-page.html`) and meaningful asset names (`antenna-array.jpg`).
- Keep inline scripts minimal; move reusable JS or CSS into dedicated files under `assets/` or the future helper directories noted above.

## Testing Guidelines
- Preview with a local server and confirm images within `assets/` resolve without 404s.
- Check browser consoles for warnings and validate links using `npx linkinator ./ --concurrency 4` when Node.js is installed.
- Document manual test steps in pull requests whenever interactive behavior is introduced.

## Commit & Pull Request Guidelines
- Write imperative, concise commit messages (e.g., “Add hero image”) consistent with the existing history.
- Summarize intent, list key changes, and link related issues in every pull request.
- Include before/after screenshots or brief screen recordings for visual updates.
- Ensure any status checks or workflows added later finish successfully before requesting review.

## Deployment Notes
- GitHub Pages publishes the default branch automatically; expect a few minutes between merge and live updates.
- After deployment, spot-check the live site and roll back quickly if assets fail to load or regressions appear.
