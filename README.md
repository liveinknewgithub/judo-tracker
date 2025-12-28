# Randori Tracker 🥋

A beautiful, offline-first Progressive Web App for judo athletes to track throws, combos, and ground techniques during training sessions.

[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen?style=flat-square)](https://liveinknewgithub.github.io/judo-tracker/)
[![GitHub Pages](https://img.shields.io/badge/hosted%20on-GitHub%20Pages-blue?style=flat-square)](https://liveinknewgithub.github.io/judo-tracker/)
[![PWA Ready](https://img.shields.io/badge/PWA-ready-purple?style=flat-square)](https://liveinknewgithub.github.io/judo-tracker/)

---

## What is Randori Tracker?

**Randori** (乱取り) is the Japanese term for free-practice sparring in judo. This app helps practitioners systematically log and analyze their training, tracking every throw, combination, and ground technique over time.

### Why use it?

- **Quick logging**: One-tap to record techniques with haptic feedback
- **Works offline**: Install as a PWA and track anywhere—no internet required
- **Privacy first**: All data stays on your device in local storage
- **Rich analytics**: See trends, streaks, category breakdowns, and personal records

---

## Features

### 🎯 Technique Tracking

| Category | Techniques |
|----------|------------|
| **Throws** | 35 techniques across Te-waza, Koshi-waza, Ashi-waza, and Sutemi-waza |
| **Combos** | 15 pre-defined combinations including 2-throw, 3-throw chains, and throw-to-newaza transitions |
| **Newaza** | 14 ground techniques: pins, chokes, and armlocks |

### 📊 Analytics Dashboard

- **Weekly bar charts** showing daily activity
- **12-week heatmap** (GitHub-style activity visualization)
- **Category breakdown** with percentage by technique type
- **Training streaks** and personal records
- **Week-over-week trends**
- **Shareable monthly summaries**

### ⏱️ Session Management

- Start/stop training sessions with a timer
- Track techniques logged per session
- Session history with duration and counts
- Sessions persist across page reloads

### 🛠️ User Controls

- **Undo**: 5-second window to undo any action
- **Search & Filter**: Find throws by name or category
- **Favorites**: Star your go-to techniques
- **Export/Import**: JSON backup and restore
- **Reset**: Clear all data with double confirmation

---

## Quick Start

### Use Online

Visit **[liveinknewgithub.github.io/judo-tracker](https://liveinknewgithub.github.io/judo-tracker/)** and start tracking immediately.

### Install as App (PWA)

1. Open the link above in Chrome, Safari, or Edge
2. Click "Install" or "Add to Home Screen" when prompted
3. The app will work offline like a native application

---

## Running Locally

Clone and serve the static files:

```bash
# Clone the repository
git clone https://github.com/liveinknewgithub/judo-tracker.git
cd judo-tracker

# Serve with any static file server (required for Service Worker)
python3 -m http.server 8000
# or
npx http-server
# or
php -S localhost:8000
```

Open [http://localhost:8000](http://localhost:8000) in your browser.

---

## Project Structure

```
judo-tracker/
├── index.html        # Single-file application (HTML + CSS + JS)
├── sw.js             # Service Worker for offline caching
├── manifest.json     # PWA manifest for app installation
├── og-image.png      # Social sharing preview image
└── README.md         # This file
```

This is a **zero-build** project—no bundlers, no dependencies, no Node.js required. Just static files served directly to the browser.

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | Vanilla JavaScript (ES6+) |
| Styling | Pure CSS with CSS Variables |
| Storage | Browser localStorage |
| PWA | Service Worker + Web Manifest |
| Analytics | PostHog (privacy-respecting) |
| Hosting | GitHub Pages |

---

## Contributing

Contributions are welcome! Here's how to get started:

### Reporting Bugs

1. Check [existing issues](https://github.com/liveinknewgithub/judo-tracker/issues) first
2. Open a new issue with:
   - Clear description of the bug
   - Steps to reproduce
   - Expected vs actual behavior
   - Browser/device information

### Suggesting Features

Open an issue with the `enhancement` label describing:
- The problem you're trying to solve
- Your proposed solution
- Any alternatives you've considered

### Submitting Code

1. **Fork** the repository
2. **Clone** your fork:
   ```bash
   git clone https://github.com/YOUR-USERNAME/judo-tracker.git
   ```
3. **Create a branch** for your feature:
   ```bash
   git checkout -b feature/your-feature-name
   ```
4. **Make your changes** to `index.html` (all app code lives here)
5. **Test locally** using a static file server
6. **Commit** with a clear message:
   ```bash
   git commit -m "Add: brief description of your change"
   ```
7. **Push** to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```
8. **Open a Pull Request** against the `main` branch

### Code Style Guidelines

- Keep all application code in `index.html` (single-file architecture)
- Use descriptive function and variable names
- Add comments for complex logic
- Test on mobile devices (primary target platform)
- Update the Service Worker cache version (`sw.js`) when making changes

### After Merging

Remember to bump the cache version in `sw.js` so users get the latest version:

```javascript
const CACHE_NAME = 'randori-tracker-v5'; // Increment this
```

---

## Data & Privacy

- **100% client-side**: Your data never leaves your device
- **localStorage only**: No accounts, no cloud sync, no tracking of personal data
- **Export anytime**: Download your complete history as JSON
- **You own your data**: Delete everything with a single reset

---

## Browser Support

| Browser | Support |
|---------|---------|
| Chrome / Edge | ✅ Full support |
| Safari (iOS/macOS) | ✅ Full support |
| Firefox | ✅ Full support |
| Samsung Internet | ✅ Full support |

Requires a modern browser with ES6, localStorage, and Service Worker support.

---

## License

This project is open source. Feel free to use, modify, and distribute.

---

## Acknowledgments

- Judo technique names follow official [Kodokan](http://kodokanjudoinstitute.org/) nomenclature
- Designed for practitioners training under IJF (International Judo Federation) rules

---

<p align="center">
  <strong>Happy training! 🥋</strong><br>
  <em>一本 (Ippon!)</em>
</p>
