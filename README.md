# CardioViz — 3D Heart Education Tool

> **Best Tech Talk** · WiCHacks @ RIT · Major League Hacking · March 2025

An interactive 3D cardiac anatomy explorer that lets users click through heart structures, learn about rare cardiac diseases, and test their knowledge with an AI-powered adaptive quiz tutor.

## Features

- **3D Interactive Heart** — full Three.js model with 7 labeled anatomical structures, heartbeat animation, and drag-to-rotate
- **Rare Disease Database** — each structure links to a rare cardiac condition with clinical facts
  - Left Ventricle → Hypertrophic Cardiomyopathy (HCM)
  - Right Ventricle → Arrhythmogenic Right Ventricular Cardiomyopathy (ARVC)
  - Left Atrium → Cor Triatriatum Sinister
  - Right Atrium & Septum → Atrial Septal Defect (ASD)
  - Aorta → Marfan Syndrome & Aortic Dissection
  - Pulmonary Artery → Pulmonary Arterial Hypertension (PAH)
  - Pericardium → Constrictive Pericarditis
- **AI Tutor** — powered by Claude (Anthropic API), generates adaptive multiple-choice questions based on what you've gotten wrong
- **Touch Support** — works on mobile and tablet

## Stack

- **Three.js r128** — 3D rendering, raycasting, custom geometry
- **Vanilla JS** — no build step, runs directly in the browser
- **Python + NLTK** (original hackathon version) — NLP quiz generation
- **Anthropic Claude API** — adaptive quiz engine in the web version

## Run Locally

```bash
# No build step needed — just open index.html in any browser
open index.html

# Or serve with any static server
python3 -m http.server 8080
```

## AI Tutor Setup

1. Get an Anthropic API key at [console.anthropic.com](https://console.anthropic.com)
2. Paste it into the API key field in the top-right corner
3. The quiz will generate adaptive questions using Claude, focusing on areas where you've made mistakes

Without a key, the app still works with a built-in question bank.

## Deploy to GitHub Pages

```bash
git init
git add .
git commit -m "initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/CardioViz.git
git push -u origin main
# Then enable GitHub Pages in repo Settings > Pages > Deploy from main branch
```

## Project Structure

```
CardioViz/
└── index.html    # Complete single-file app (Three.js + UI + quiz logic)
```

## Background

Built at WiCHacks 2025 (Rochester Institute of Technology) in 24 hours by a team using Three.js for 3D visualization and Python/NLTK for the original quiz NLP backend. Won **Best Tech Talk** out of 12 competing teams.

The web version replaces the Python/NLTK backend with direct Anthropic API calls, making it fully browser-deployable without a server.

---

*Built by Veronika Atyeva · Le Moyne College CS '26 · [linkedin.com/in/veronika-atyeva](https://linkedin.com/in/veronika-atyeva)*
