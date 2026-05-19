# Learning Homeopathy

An interactive, single-page learning website for studying classical homeopathy from first principles through practical home-kit reference material.

Live site: [homeopathy.adityamahajan.in](https://homeopathy.adityamahajan.in)

## What This Website Covers

The site is built as a self-paced curriculum called **Homeopathy Academy**. It takes a beginner through a structured learning path:

1. **History & Origins** - Hahnemann, the cinchona experiment, the Organon, key figures, and a short quiz.
2. **Core Principles** - law of similars, vital force, drug proving, Hering's law, and system comparisons.
3. **Potencies & Preparations** - X/C/LM scales, dilution math, remedy preparation, and a potency calculator.
4. **Materia Medica** - remedy pictures, polychrest remedy tabs, first-aid remedy search, and study guidance.
5. **Repertory** - Kent-style repertory structure, rubric selection, and a mini repertorization demo.
6. **Case Taking** - symptom hierarchy, PQRS features, modalities, and a case-summary generator.
7. **Miasms & Chronic Disease** - psora, sycosis, syphilitic, and tubercular miasm patterns.
8. **Home Kit & Practical Self-Help** - 35-remedy home kit, storage guidance, red flags, and safe-use reminders.

## Key Features

- Sticky navigation with module anchors.
- Seven-phase learning roadmap.
- Dark/light theme toggle saved in `localStorage`.
- Module completion tracker saved in `localStorage`.
- Timeline, cards, accordions, tabs, searchable tables, and charts.
- Interactive history quiz.
- Potency calculator.
- Polychrest remedy tabs.
- First-aid and home-kit remedy search.
- Mini repertorization demo that highlights remedy overlap.
- Case-taking form that generates a structured summary.
- Emergency red-flag section.
- Global remedy search modal.
- Back-to-top button, scroll reveal animations, print styles, and study-tip toasts.

## Tech Stack

This is a static website with no build step.

- HTML, CSS, and vanilla JavaScript in one file: `index.html`
- [Bootstrap 5](https://getbootstrap.com/) via CDN
- [Chart.js](https://www.chartjs.org/) via CDN
- [Animate.css](https://animate.style/) via CDN
- [Font Awesome](https://fontawesome.com/) via CDN
- Google Fonts: Inter and Playfair Display

The custom JavaScript includes graceful fallbacks for Bootstrap-dependent interactions, so the main learning experience still works if CDN scripts are slow or unavailable.

## Repository Structure

```text
.
├── CNAME                         # Custom domain for hosting
├── README.md                     # Project overview and setup notes
├── homeopathy_website_prompt.md  # Original generation prompt/spec
└── index.html                    # Complete single-file website
```

## Run Locally

Clone the repository, then serve the folder with any static file server.

```bash
python3 -m http.server 4174
```

Open:

```text
http://127.0.0.1:4174/index.html
```

You can also open `index.html` directly in a browser, but using a local server is closer to the hosted environment.

## Deployment Notes

The project is designed for static hosting. The `CNAME` file points the hosted site to:

```text
homeopathy.adityamahajan.in
```

For GitHub Pages or similar static hosts, publish the repository root so `index.html` is served as the homepage.

## Important Disclaimer

This website is for education and reference only. It is not medical advice, diagnosis, or a substitute for care from a qualified health professional. The site includes emergency red-flag guidance because urgent, severe, worsening, or unclear symptoms should be handled through appropriate medical care first.
