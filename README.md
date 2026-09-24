# Jason Lin's Personal Website

Author: Jason Lin

This repository is based on https://github.com/varadbhogayata/varadbhogayata.github.io.

## About

A personal portfolio site built for ECE444 PRA2 (Front End Design), covering my background,
work experience, projects, skills, education, and an interactive map of places I've travelled.

Live site: https://saltyfishqaqq.github.io

## Tech stack

- HTML, CSS, vanilla JavaScript (no frontend framework)
- [Materialize CSS](https://materializecss.com/) for base layout/components (loaded via CDN)
- Google Maps embed (no API key required)
- Hand-generated SVG world map (country outlines projected from a public GeoJSON dataset)
- GitHub Pages for deployment

## Features

- **About / Experience / Projects / Skills / Education** — personal content, each experience
  entry with its own company logo
- **Custom purple theme** — defined via CSS variables in `assets/css/style.css`, applied
  consistently across nav, section headers, links, and buttons
- **Places Travelled** — an interactive SVG world map (`assets/js/world-map-data.js`) with
  clickable pins per city; hovering a pin shows the city and country, clicking it reveals a
  photo gallery below the map. Supports scroll-to-zoom and drag-to-pan. Pins with no photos
  yet are visually disabled.
- **Dynamic project cards** — project data lives in a JS array (`projectsData` in
  `index.html`); a render function builds the project cards from that array, initially
  showing 2 with a "Load More" button that reveals the rest without reloading the page
- **Custom cursor** — a small badminton-shuttlecock cursor across the site
- Responsive layout with a mobile nav menu

## Project structure

```
index.html                 Main page markup + inline data/JS for projects and the world map
assets/css/style.css       All custom styling (theme, layout, components)
assets/js/world-map-data.js  World map SVG path data + travelled-places data
assets/img/                Images, including assets/img/travel/<city>/ photo galleries
assets/vendor/              Third-party JS (typed.js)
```

## Running locally

This is a static site — no build step required.

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.
