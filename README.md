# UISEL — Universal Institute of Skills & Entrepreneurship (Portfolio Website)

Global Skills for a Connected Future — a responsive marketing and application site built with React for UISEL (Universal Institute of Skills & Entrepreneurship Ltd.), showcasing programs, accreditations, training areas, and providing application forms for trainees and employer partners.

Badges
- Framework: Create React App + React 19
- Styling: Tailwind CSS + custom CSS
- Routing: react-router-dom
- Email: EmailJS (client-side form email integration)

---

## Table of contents
- [Quick summary](#quick-summary)
- [Features](#features)
- [Stack](#stack)
- [Project structure](#project-structure)
- [Getting started](#getting-started)
- [Configuration / Environment variables](#configuration--environment-variables)
- [Build & deploy](#build--deploy)
- [Notes & troubleshooting](#notes--troubleshooting)
- [Contact](#contact)

---

## Quick summary
This repository contains a production-ready single-page React website for UISEL with:
- Fully responsive landing/home pages that present services, training areas, accreditations, testimonials, global reach and contact information.
- Dedicated pages and client-side application forms for Applicants (employees/trainees) and Employers that send emails using EmailJS.
- Modular React component structure for Navbar, Footer, and ScrollToTop, plus page components for Home, Training and Apply.

---

## Features
- Responsive, accessible UI with Tailwind CSS + custom styles
- React Router (Routes) for client-side navigation (/, /training, /apply)
- EmailJS integration to submit forms from the client
- Static assets (logos, hero images, flags) in src/assets
- Clean, componentized React pages: Home.jsx, Training.jsx, Apply.jsx
- Reusable UI components: Navbar.jsx, Footer.jsx, ScrollToTop.jsx

---

## Stack
- Language(s): JavaScript (ES202x)
- Framework / runtime: React 19 (Create React App scaffold)
- Notable libraries:
  - react-router-dom (routing)
  - tailwindcss + postcss (utility-first styling)
  - emailjs-com (client-side email delivery)
  - @fortawesome/fontawesome-free (icons)

---

## Project structure (top-level, annotated)

How it fits together:
- App.js provides Router and Routes; each page (Home, Training, Apply) is a self-contained route component composed from smaller components (Navbar, Footer).
- Apply.jsx implements two interactive forms (employee, employer) and uses emailjs-com to send submissions to the configured EmailJS service/template.

---

## How to run it (local development)
Prerequisites: Node.js and npm installed (Node 16+ recommended; use Node 18+ for latest toolchain stability).

1. Clone the repo
   git clone https://github.com/jawadul1707/uisel-portfolio-website.git
2. Install dependencies
   npm install
3. Start development server
   npm start
4. Open in browser
   http://localhost:3000

Available npm scripts (from package.json):
- npm start — development server (react-scripts start)
- npm run build — production build into `build/`
- npm test — launch tests (react-scripts test)
- npm run eject — (one-way) eject CRA config

---

## Configuration / Environment variables
Apply.jsx currently contains EmailJS constants. For production you should not keep secrets or user IDs inline. Replace with environment variables:

Recommended environment variables (create a .env in project root):
- REACT_APP_EMAILJS_SERVICE_ID=your_service_id
- REACT_APP_EMAILJS_TEMPLATE_ID_EMPLOYEE=your_template_id_employee
- REACT_APP_EMAILJS_TEMPLATE_ID_EMPLOYER=your_template_id_employer
- REACT_APP_EMAILJS_USER_ID=your_emailjs_public_user_id

Update src/pages/Apply.jsx to read from process.env, for example:
- const EMAILJS_SERVICE_ID = process.env.REACT_APP_EMAILJS_SERVICE_ID

Important: With Create React App, environment variables must be prefixed with REACT_APP_.

Assets:
- src/assets/logos/* and other images are used by pages; ensure your images exist or replace with proper files.

---

## Build & deploy
1. Build
   npm run build
2. Deploy the contents of the build/ folder to any static hosting (Netlify, Vercel, GitHub Pages, S3 + CloudFront, or your preferred host).

Notes:
- This is a static SPA; server-side rendering is not used.
- If deploying to a subpath or GitHub Pages, ensure your router configuration is compatible (HashRouter or configure redirects on host).

---

## Notes & troubleshooting
- CRA / react-scripts: If `npm run build` fails to minify, check that any third-party code is transpiled or remove unsupported modern syntax from vendor files.
- Email delivery: EmailJS is client-side—ensure your EmailJS templates use the variable names used in Apply.jsx (e.g. {{fullName}}, {{email}}, {{phone}}, etc.). Also configure the allowed origins in the EmailJS dashboard.
- Tailwind: Tailwind is configured (tailwind.config.js + postcss.config.js). If utilities don't apply, ensure Tailwind directives are present in src/index.css and PostCSS is running.

---

## Contact
UISEL — info@uisel.com  
Site maintained in this repository: https://github.com/jawadul1707/uisel-portfolio-website
