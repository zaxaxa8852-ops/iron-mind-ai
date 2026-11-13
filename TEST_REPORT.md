# IRON MIND AI 1.1.0 — QA and release status

## Changes in this release
- Switched to hash-based routing for GitHub Pages compatibility (deep links and refreshes do not depend on server-side SPA rewrites).
- Added automatic GitHub Pages build/deploy workflow at `.github/workflows/deploy.yml`.
- Updated page metadata and document language/direction when switching Arabic/English.
- Kept AI Coach explicitly offline / under development; no client-side API secret or fake AI response is included.
- Updated release and publishing instructions.

## Included functionality (code review)
- [x] Home page and primary navigation routes.
- [x] Arabic / English toggle and RTL / LTR layout direction.
- [x] Exercise search and muscle group / target area / level filters.
- [x] Exercise detail routes and content.
- [x] Eight program overview and detail routes.
- [x] Nutrition topic cards.
- [x] Food database search and category filter.
- [x] Meal category filters and calculated estimated macros.
- [x] Adult BMI, BMR and TDEE estimator with basic input validation.
- [x] AI Coach visibly offline / under development until a secure backend is supplied.
- [x] Responsive CSS breakpoints.
- [x] GitHub Actions deployment workflow added.

## Not verified in this environment
- [ ] `npm install` did not complete before the environment command timeout.
- [ ] Production `npm run build` therefore could not be run here.
- [ ] GitHub Actions workflow has not run; no live website URL exists yet.
- [ ] Browser console, cross-browser, screen-reader and keyboard accessibility audits.
- [ ] Scientific editorial review and expansion of food/micronutrient references.
- [ ] Real exercise photography/animations (current visuals are icon/graphic treatments).
- [ ] AI backend and security (intentionally deferred).

## Release caveat
This is a prepared deployable project package, not a verified live deployment. After pushing to GitHub and selecting **Settings → Pages → GitHub Actions**, the workflow will install dependencies and attempt the production build. Treat the release as published only after that workflow succeeds.
