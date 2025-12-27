# Expired Solutions Website

Official website for Expired Solutions - AI-Powered Freshness Management.

**Live URL**: https://expiredsolutions.com

---

## 🚀 Quick Deploy to Vercel

### Option 1: One-Click Deploy (Easiest)

1. Push this repo to GitHub
2. Go to [vercel.com/new](https://vercel.com/new)
3. Import your GitHub repo
4. Click "Deploy"
5. Done! 🎉

### Option 2: Vercel CLI

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
cd ExpiredSolutionsWeb
vercel

# Follow prompts, then:
vercel --prod
```

---

## 📁 Project Structure

```
ExpiredSolutionsWeb/
├── public/             # Vercel output directory
│   ├── index.html      # Main website (single page)
│   ├── favicon.svg     # Site favicon
│   └── screenshots/    # Website images (logo, team, awards, mock screens)
├── package.json        # Project metadata
├── vercel.json         # Vercel configuration
└── README.md           # This file
```

---

## 🌐 Custom Domain Setup (expiredsolutions.com)

### Step 1: Add Domain in Vercel

1. Go to your Vercel project dashboard
2. Click **Settings** → **Domains**
3. Add `expiredsolutions.com`
4. Add `www.expiredsolutions.com`

### Step 2: Update DNS Records

At your domain registrar (GoDaddy, Namecheap, etc.), update DNS:

**DELETE these old Framer records:**
```
www    CNAME    sites.framer.app
@      A        31.43.160.6
@      A        31.43.161.6
asuid  TXT      617062BC248DC46BC82FBE1D442DB563E71CA6D5E3C31C55DD1CCDBD9008F86D
```

**ADD these Vercel records:**
```
@      A        76.76.21.21
www    CNAME    cname.vercel-dns.com
```

### Step 3: Wait for Propagation

- DNS changes take 5-30 minutes (sometimes up to 48 hours)
- Vercel auto-provisions SSL certificate
- Check status at: [dnschecker.org](https://dnschecker.org)

---

## 📸 Adding Screenshots

Replace placeholder images in `/screenshots/`:

| File | Size | Description |
|------|------|-------------|
| `hero-scan.png` | 390x844 | Main camera scanning view |
| `inventory.png` | 390x844 | Inventory grid with items |
| `detail.png` | 390x844 | Item detail with freshness score |

**To capture from iOS Simulator:**
1. Run app in iPhone 15 Pro simulator
2. Navigate to desired screen
3. Press `Cmd+S` to save screenshot
4. Rename and move to this folder

---

## 🔧 Local Development

```bash
# Option 1: Python
cd public && python3 -m http.server 3000

# Option 2: Node
npx serve public

# Then open http://localhost:3000
```

---

## ✨ Features

- **Responsive Design** - Works on mobile, tablet, desktop
- **Dark Theme** - Professional green/dark gradient
- **Feedback System** - Modal form submits to backend API
- **Contact Form** - Integrated with production API
- **App Store Link** - Direct download button
- **SEO Optimized** - Meta tags, Open Graph

---

## 🔗 Important Links

| Resource | URL |
|----------|-----|
| Production API | https://expiredsolutions-api-dcaqbggchqhrhkfe.eastus-01.azurewebsites.net |
| Privacy Policy | https://lively-forest-06c6b730f.3.azurestaticapps.net/privacy.html |
| Terms of Service | https://lively-forest-06c6b730f.3.azurestaticapps.net/terms.html |
| Support | https://lively-forest-06c6b730f.3.azurestaticapps.net/support.html |

---

## 📝 Updating Content

The website is a single `index.html` file. To update:

1. Edit `index.html`
2. Commit and push to GitHub
3. Vercel auto-deploys in ~30 seconds

---

## 🛠 Tech Stack

- **HTML5** - Semantic markup
- **Tailwind CSS** - Via CDN (no build step)
- **Vanilla JavaScript** - No frameworks
- **Vercel** - Hosting with edge CDN

---

*Last Updated: December 25, 2025*

