# Digital Business Card — Hosting Guide

## Before you deploy

**Resumes (hosted with the card):** Keep these PDFs in the repo root next to `index.html` so links stay valid when you print/share the card as a PDF:

- `shaquille-comrie-ui-ux-resume.pdf` — UI/UX resume  
- `shaquille-comrie-resume.pdf` — general resume  

After you push, they are served at (GitHub default or custom domain):

- `https://card.secfreelance.com/shaquille-comrie-ui-ux-resume.pdf`  
- `https://card.secfreelance.com/shaquille-comrie-resume.pdf`  

(fallback: `https://elreyriquez.github.io/digital-card/…`)

## Custom domain (`card.secfreelance.com`)

1. **Namecheap → Advanced DNS:** **CNAME** · Host **`card`** → **`elreyriquez.github.io`**
2. **GitHub → repo → Settings → Pages:** **Custom domain:** `card.secfreelance.com` (matches the **`CNAME`** file in this repo). Enable **Enforce HTTPS** when ready.

The repo root **`CNAME`** file must contain exactly: `card.secfreelance.com`

```
digital-card/
├── index.html
├── profile.png
├── shaquille-comrie-ui-ux-resume.pdf
├── shaquille-comrie-resume.pdf
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
