# Text Reveal Animation (React + Vite)

A small React demo that showcases per-line text reveal animations on load/scroll using GSAP SplitText + ScrollTrigger, with smooth scrolling powered by Lenis. Built with Vite for a fast DX.

This project renders a simple landing page with animated headings and paragraphs, and includes two example images (hero and about) to demonstrate layered content and animations.

## Tech Stack
- React 19
- Vite 7
- GSAP 3 (`gsap`, `@gsap/react`) — using SplitText and ScrollTrigger plugins
- Lenis (smooth scrolling)
- ESLint (configured for React hooks and Vite refresh)
- Package manager: npm (package-lock.json present)

## Requirements
- Node.js 18+ (LTS recommended)
- npm 9+ (npm is used by this repo)

## Getting Started
1. Install dependencies
   - npm install
2. Start the dev server
   - npm run dev
   - Vite will print a local URL (by default http://localhost:5173)
3. Build for production
   - npm run build
   - Output will be generated in the dist folder
4. Preview the production build locally
   - npm run preview

## Scripts
- npm run dev — start Vite dev server with HMR
- npm run build — build the production bundle
- npm run preview — preview the built app locally
- npm run lint — run ESLint on the project

## Entry Points and Structure
- index.html — Loads the React app and includes the root div
- src/main.jsx — React entry; mounts the app and imports global styles
- src/App.jsx — Main page layout, sections, and usage of Copy animation wrapper
- src/components/Copy.jsx — Core animation component using GSAP SplitText + ScrollTrigger
- src/index.css — Global styles and layout
- public/hero.jpg, public/about.jpg — Example images referenced by the UI

### Project Tree (simplified)
- index.html
- package.json
- vite.config.js
- eslint.config.js
- public/
  - hero.jpg
  - about.jpg
- src/
  - main.jsx
  - App.jsx
  - index.css
  - components/
    - Copy.jsx

## Environment Variables
No environment variables are required for local development.

- TODO: Document any future environment variables here if deployment or external services are added.

## Tests
No automated tests are currently configured in this repository.

- TODO: Add a testing setup (e.g., Vitest + React Testing Library) and document how to run tests.

## Linting
ESLint is configured via eslint.config.js.

- Run lint: npm run lint

## License
A license file is not present.

- TODO: Add a LICENSE file (e.g., MIT) and note the license here.

## Notes
- The GSAP SplitText plugin is used via gsap/SplitText imports and registered alongside ScrollTrigger in src/components/Copy.jsx.
- Smooth scrolling is provided by Lenis through ReactLenis in src/App.jsx.
- If you deploy this app, ensure the public assets (hero.jpg, about.jpg) are available at the root/public path expected by Vite.
