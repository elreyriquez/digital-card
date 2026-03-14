# Digital Business Card — Hosting Guide

## Before you deploy

**Add your resume:** Place your resume PDF in this folder and name it `resume.pdf`. The download link in your card will point to it automatically.

```
digital-card/
├── index.html
├── profile.png
├── resume.pdf    ← Add your resume here (rename if needed)
└── DEPLOY.md
```

---

## Option 1: GitHub Pages (free, recommended)

1. **Create a new GitHub repo** (e.g. `shaquille-comrie` or `digital-card`)

2. **Push this folder** to the repo:
   ```bash
   cd /Users/shaq/Documents/Projects/digital-card
   git init
   git add .
   git commit -m "Digital business card"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git push -u origin main
   ```

3. **Enable GitHub Pages:**  
   Repo → Settings → Pages → Source: **Deploy from branch** → Branch: `main` → Save

4. **Your card will live at:**  
   `https://YOUR_USERNAME.github.io/YOUR_REPO/`

---

## Option 2: Netlify (free, drag & drop)

1. Go to [netlify.com](https://netlify.com) and sign up
2. Drag the entire `digital-card` folder onto the Netlify dashboard
3. You’ll get a URL like `random-name-123.netlify.app`
4. In Site settings → Domain management you can add a custom domain

---

## Option 3: Vercel (free)

1. Install Vercel CLI: `npm i -g vercel`
2. In the `digital-card` folder, run `vercel`
3. Follow the prompts — you’ll get a live URL right away

---

## Quick share at the hackathon

- **QR code:** Use [qr-code-generator.com](https://www.qr-code-generator.com/) or similar with your live URL
- **Short link:** Use [bit.ly](https://bit.ly) or [t.ly](https://t.ly) to create a short link like `bit.ly/shaq-card`
