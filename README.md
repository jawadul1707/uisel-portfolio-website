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
- [Contributing](#contributing)
- [License](#license)
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
