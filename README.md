# ✨ Yassa Halim — Personal Portfolio Website

A sleek, modern, production-ready personal portfolio website for **Yassa Halim** (Flutter Developer & UI/UX Designer). Designed with a **light, elegant, and chic** visual identity, native **Arabic & English (RTL/LTR)** bilingual support, smooth micro-interactions, responsive CSS/SVG phone mockup, and zero external build tool requirements.

Hosted with zero configuration on **GitHub Pages**.

---

## 🌟 Highlights & Features

- **Chic, Light Visual Identity**: Soft pastel mesh background (`#FAFAF7`), translucent glassmorphism cards, Flutter sky-blue primary accent (`#4C9BF5 → #7BC4FF`), and subtle floating ambient orbs.
- **Full Bilingual Support (EN & AR)**:
  - Dynamic language toggle (`AR | EN`) in the navbar.
  - Automatically mirrors layout (`dir="rtl"` vs `dir="ltr"`) using CSS logical properties (`margin-inline`, `padding-inline`, `text-align: start`).
  - Native typography: **Plus Jakarta Sans** for English and **Cairo** for Arabic via Google Fonts.
  - Preference persistence in `localStorage` with automatic fallback to browser language.
  - Single centralized JavaScript translation dictionary (`PORTFOLIO_DATA.translations`).
- **Stylized Phone Mockup & Orbiting Badges**: Built entirely with pure CSS and vector SVGs showcasing a live vehicle tracking app UI (*Arabeety GPS*), telemetry stats, clean code preview, and floating achievement badges.
- **Animated Typewriter Subtitle**: Rotating titles in both languages (*"Flutter Developer"*, *"UI/UX Enthusiast"*, *"AI & Big Data Learner"*).
- **Featured Projects Grid**: Pre-populated with realistic details for:
  1. **Arabeety (عربيتي)** — Smart automotive telemetry app with custom UI/UX design system.
  2. **Flutter Dev AI Personal Assistant** — n8n autonomous agent with Telegram bot, CV screening, job alerts, and Gmail digest.
  3. **Hospital Knowledge Management System** — Comprehensive Python clinical records and search platform.
  4. **Next-Gen Mobile AI Experience** — Innovative upcoming Flutter + edge-AI application.
- **Vertical Education Timeline**: Route Academy Diploma, NTI UI/UX Training, and Huawei ICT Academy Certifications.
- **Highlighted Trophy Achievement**: Soft gold-tinted showcase for the **Huawei ICT Competition 2025–2026 Third Prize** (Innovation Track, Regional Phase).
- **Interactive Contact Section**: Direct email with instant copy-to-clipboard toast feedback, LinkedIn, GitHub, and a pre-configured contact form that prepares drafts via `mailto:` or integrates with Formspree.
- **Zero Build Tools & Zero Heavy Dependencies**: A single self-contained `index.html` file with vanilla HTML5, CSS3, and JavaScript. Zero npm packages, zero Node build steps, 100% fast and reliable.

---

## 🚀 5-Step Guide to Publish on GitHub Pages

### Step 1: Choose Your Repository Name
You have two hosting choices on GitHub:
- **User Site (`https://<username>.github.io`)**: Name your repository exactly `<username>.github.io` (e.g., `yassa-halim.github.io`).
- **Project Site (`https://<username>.github.io/<repo-name>`)**: You can also use your existing repository `yassa-halim` or create a new repository such as `portfolio`.

### Step 2: Push the Files to GitHub
Make sure `index.html` is in the root directory of your repository on the `main` branch:
```bash
git add index.html README.md
git commit -m "Deploy production portfolio website"
git push origin main
```

### Step 3: Enable GitHub Pages
1. Open your repository on GitHub (`https://github.com/<username>/<repo-name>`).
2. Click **Settings** (tab at the top right).
3. In the left sidebar, click **Pages** (under the "Code and automation" section).
4. Under **Build and deployment**:
   - **Source**: Select `Deploy from a branch`.
   - **Branch**: Select `main` and set the folder to `/ (root)`.
5. Click **Save**.

### Step 4: Wait for Deployment & Visit Your Site
- GitHub will start an automated GitHub Pages deployment action.
- Within 1–2 minutes, a banner will appear at the top of the Pages settings page showing:
  > **Your site is live at `https://<username>.github.io/`**
- Click the link to open your live portfolio!

### Step 5: (Optional) Add a Custom Domain
If you have your own domain (e.g. `yassahalim.com`):
1. In repository **Settings** → **Pages** → **Custom domain**, type your domain name and click **Save**.
2. Add a `CNAME` record in your DNS provider (e.g., Cloudflare, Namecheap, GoDaddy):
   - **Type**: `CNAME`
   - **Host / Name**: `@` or `www`
   - **Value / Target**: `<username>.github.io`
3. Check the **Enforce HTTPS** box once the DNS propagates.

---

## ✏️ Where to Customize Your Data

Everything in `index.html` is centralized in a clearly marked configuration object at line ~2860:

```javascript
/* ===================================================================== */
/* EDIT HERE: PERSONAL DATA & BILINGUAL TRANSLATIONS                     */
/* ===================================================================== */
const PORTFOLIO_DATA = {
  profile: {
    name: "Yassa Halim",
    email: "yassahalim18@gmail.com",
    github: "https://github.com/yassa-halim",
    linkedin: "https://www.linkedin.com/in/yassa-halim/"
  },
  translations: {
    en: { ... },
    ar: { ... }
  }
};
```

### 1. Social & Contact Links
- **Email**: Update `profile.email` in `PORTFOLIO_DATA` and the `href="mailto:..."` links in the HTML.
- **GitHub**: Update `profile.github` and the `<a href="https://github.com/yassa-halim">` tags in the Hero, Contact, and Footer sections.
- **LinkedIn**: Update `profile.linkedin` and the LinkedIn anchor tags.

### 2. Project Repositories & Demos
In the `#projects` section of `index.html`:
- Update the `<a href="...">` buttons on each project card with your actual GitHub repository URL or live preview links.

### 3. Contact Form (Optional Formspree Integration)
Currently, the contact form automatically composes a pre-filled `mailto:` draft. If you prefer to receive submissions directly to your inbox without opening the user's email client, sign up for free at [Formspree](https://formspree.io) and replace the form tag in `index.html`:
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

---

## 💻 Local Preview

To preview the portfolio locally on your computer, run Python's built-in HTTP server:

```bash
# From the project root:
python3 -m http.server 8080
```
Then open `http://localhost:8080` in any web browser.

---

## 📄 License
Created with ❤️ for Yassa Halim. Clean code, high performance, and responsive design.
