# 🚀 GitHub Pages Deployment Guide

A step-by-step guide to hosting and deploying the portfolio website on **GitHub Pages**.

---

## 1. Fast Setup on GitHub Pages (1 Minute)

1. Open your repository on GitHub:
   👉 **https://github.com/yassa-halim/yassa-halim**
2. Click **Settings** (gear icon ⚙️ in the top navigation bar).
3. In the left sidebar, click **Pages** (under the **Code and automation** section).
4. Under **Build and deployment**:
   - **Source**: Select `Deploy from a branch`
   - **Branch**: Select `main`
   - **Folder**: Select `/ (root)`
5. Click **Save**.

Within 30–60 seconds, GitHub Actions will publish the website. Your live portfolio will be accessible at:
🌟 **https://yassa-halim.github.io/yassa-halim/**

---

## 2. (Optional) Hosting at Root URL (`https://yassa-halim.github.io`)

If you want your portfolio to load directly at `https://yassa-halim.github.io` (without `/yassa-halim/` in the URL path):
1. Create a new public repository named exactly:  
   **`yassa-halim.github.io`**
2. Push `index.html` to that repository:
   ```bash
   git remote add pages https://github.com/yassa-halim/yassa-halim.github.io.git
   git push pages main
   ```
3. GitHub automatically treats `<username>.github.io` as your primary user site and deploys it immediately!

---

## 3. (Optional) Setting Up a Custom Domain

To link your own custom domain (e.g., `yassahalim.dev` or `yassahalim.com`):
1. In repository **Settings** → **Pages** → **Custom domain**, enter your domain name and click **Save**.
2. Go to your domain registrar (e.g., Namecheap, Cloudflare, GoDaddy) and add DNS records:
   - **Type**: `CNAME`
   - **Name**: `@` or `www`
   - **Value / Target**: `yassa-halim.github.io`
3. Once DNS propagates, check **Enforce HTTPS** in GitHub Pages settings.

---

## 4. Local Preview

To test and preview the website locally on your machine:
```bash
python3 -m http.server 8080
```
Then visit `http://localhost:8080` in your web browser.
