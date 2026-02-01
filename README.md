# SecondLook Retire — Teaser Landing Page

A beautiful coming soon page for the Retirement Readiness Checkup SaaS.

## Quick Deploy

### Option 1: GitHub Pages (Free)

1. Create a new repo on GitHub (e.g., `secondlookretire-site`)
2. Push this folder:
   ```bash
   cd /home/jason/clawd/saas-ideas/retirement-checkup-site
   git init
   git add .
   git commit -m "Initial teaser site"
   git remote add origin git@github.com:YOUR_USERNAME/secondlookretire-site.git
   git push -u origin main
   ```
3. Go to repo **Settings → Pages**
4. Set Source to "Deploy from a branch" → `main` / `root`
5. Your site will be live at `https://YOUR_USERNAME.github.io/secondlookretire-site`

**Custom domain:**
- Add a `CNAME` file with your domain (e.g., `secondlookretire.com`)
- Configure DNS: CNAME `www` → `YOUR_USERNAME.github.io`
- In GitHub Pages settings, add your custom domain

### Option 2: Cloudflare Pages (Free, Faster)

1. Push to GitHub (or connect directly)
2. Go to [Cloudflare Dashboard](https://dash.cloudflare.com/) → Pages
3. Click "Create a project" → "Connect to Git"
4. Select your repo
5. Build settings:
   - Build command: (leave empty)
   - Build output directory: `/` or `.`
6. Deploy!

**Custom domain:**
- In Cloudflare Pages, go to your project → Custom domains
- Add `secondlookretire.com`
- If domain is already on Cloudflare DNS, it auto-configures

## Customization

### Change the name/branding
Search and replace in `index.html`:
- `SecondLook Retire` → Your brand name
- `secondlookretire.com` → Your domain

### Add email signup (Formspree)
1. Create free account at [formspree.io](https://formspree.io)
2. Create a form, get your form ID
3. In `index.html`, uncomment the fetch code in the `<script>` section
4. Replace `YOUR_FORM_ID` with your actual form ID

### Add email signup (ConvertKit)
Replace the form with ConvertKit's embed code, or use their API.

### Colors
Edit the CSS variables at the top of `<style>`:
```css
:root {
  --primary: #4F46E5;      /* Purple */
  --secondary: #10B981;    /* Green accent */
  --dark: #1F2937;
  --light: #F9FAFB;
}
```

### Add analytics
Add before `</head>`:
```html
<!-- Plausible (privacy-friendly) -->
<script defer data-domain="secondlookretire.com" src="https://plausible.io/js/script.js"></script>

<!-- Or Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXX"></script>
```

## Files

```
├── index.html    # The entire site (single file, no dependencies)
└── README.md     # This file
```

## Features

- ✅ Fully responsive (mobile-first)
- ✅ No external dependencies (pure HTML/CSS/JS)
- ✅ Animated background shapes
- ✅ Email signup form (ready for Formspree/ConvertKit)
- ✅ SEO meta tags + Open Graph
- ✅ Fast loading (< 15KB)
- ✅ Works offline after first load

## Preview Locally

Just open `index.html` in a browser, or:
```bash
cd /home/jason/clawd/saas-ideas/retirement-checkup-site
python3 -m http.server 8000
# Open http://localhost:8000
```

---

Made with 🛸 by Rowebot
