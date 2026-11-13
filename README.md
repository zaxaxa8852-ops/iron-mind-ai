# IRON MIND AI — Release 1.1.0

**Knowledge for Everyone.** A free, responsive Arabic/English fitness and nutrition learning platform built with React and Vite.

## What is included

- Dark responsive interface with Arabic RTL / English LTR switching.
- Exercise library with search and filters, exercise details and technique notes.
- Eight training program/split guides.
- Introductory nutrition knowledge library.
- Food reference database and meal ideas with estimated macro totals.
- Adult BMI, BMR and TDEE educational estimator.
- About page for founder Ahmed Eissa and Instagram link: [@ahmed_sag32](https://instagram.com/ahmed_sag32).
- AI Coach interface is intentionally **under development / offline**. No AI answer is fabricated and no API key is required to use the rest of the website.
- GitHub Actions workflow for automatic GitHub Pages deployment.

## Run locally

Requirements: Node.js 20 or newer and npm.

```bash
npm install
npm run dev
```

Create a production build:

```bash
npm run build
npm run preview
```

## Publish free with GitHub Pages

1. Create a **public** repository on GitHub, for example `iron-mind-ai`.
2. Upload/push the contents of this project to the repository's `main` branch. Keep the `.github/workflows/deploy.yml` file.
3. In GitHub open **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **GitHub Actions**.
5. Open the **Actions** tab and wait for **Deploy IRON MIND AI to GitHub Pages** to finish successfully.
6. Your site URL will appear in **Settings → Pages** and in the successful deployment run.

The site uses hash-based navigation so direct links and refreshes work on GitHub Pages without a custom server rewrite. Vite's relative asset base supports project repository URLs.

### Upload using Git (from this folder)

```bash
git init
git add .
git commit -m "Release IRON MIND AI 1.1.0"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/iron-mind-ai.git
git push -u origin main
```

Replace `YOUR_USERNAME` and the repository name with your actual GitHub details.

## AI Coach status

AI Coach is deliberately left under development. The interface can connect to a future server endpoint through `VITE_API_BASE_URL`, but no backend is included in this release. When implementing it, keep provider API keys on the server only; never put secrets in frontend code or `VITE_*` variables.

## Important content notes

- Exercise guidance is educational; technique should be adapted to the individual and equipment.
- Food values are reference estimates and may differ by brand, recipe and cooking method. Some local-food entries are explicitly approximate.
- BMI is not a diagnosis and does not distinguish fat from lean mass.
- The energy estimator uses Mifflin–St Jeor and is intended for adults only. It is not medical advice.
- Nutrition content is introductory and should receive expert editorial review before being used as clinical guidance.

## Project structure

```text
.github/workflows/deploy.yml
src/App.jsx
src/styles.css
src/data/exercises.js
src/data/nutrition.js
src/data/programs.js
src/data/i18n.js
```

## Verification status

See [TEST_REPORT.md](./TEST_REPORT.md). The deployment workflow will run the production build in GitHub Actions after you push the repository. No public URL is claimed until GitHub reports a successful deployment.
