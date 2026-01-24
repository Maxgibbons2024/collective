# Marbella Collective — Deployment Guide

## Deploy to Vercel (Recommended - Free & Easy)

### Option 1: Drag & Drop (Easiest)

1. Go to [vercel.com](https://vercel.com)
2. Sign up/login (use GitHub, GitLab, or email)
3. Click "Add New Project"
4. Drag the entire `marbella-site-v2` folder onto the upload area
5. Click "Deploy"
6. Done! Your site is live in ~30 seconds

**Your site URL will be:** `your-project-name.vercel.app`

### Option 2: GitHub (Recommended for updates)

1. Create GitHub account if you don't have one
2. Create new repository
3. Upload all files from `marbella-site-v2` folder
4. Go to [vercel.com](https://vercel.com)
5. Click "New Project"
6. Import your GitHub repository
7. Click "Deploy"

**Benefit:** Every time you update files in GitHub, Vercel auto-deploys.

### Option 3: Vercel CLI

```bash
# Install Vercel CLI
npm install -g vercel

# Navigate to folder
cd marbella-site-v2

# Deploy
vercel
```

---

## Custom Domain Setup

Once deployed:

1. Go to your Vercel project dashboard
2. Click "Settings" → "Domains"
3. Add your domain (e.g., `marbellacollective.com`)
4. Follow DNS instructions (add A record or CNAME)
5. Wait 5-60 minutes for DNS propagation

**DNS Settings (if using Vercel):**
- **Type:** CNAME
- **Name:** www (or @)
- **Value:** cname.vercel-dns.com

---

## Before You Deploy - Update These:

### 1. Phone Number (IMPORTANT)
Find and replace `34604497118` with your actual number across all files.

### 2. Pricing
Update placeholder prices in villa pages:
- Villa Monterray: Currently €10,500
- Villa Vanilla: Currently €12,000
- Villa Sierra: Currently €9,500
- Villa Ampola: Currently €8,500

### 3. Villa Details
Add actual bedroom counts, amenities, and descriptions when available.

### 4. Connect Forms (Later)
The "For Owners" page (when built) will need form connection:
- Formspree (easiest)
- Netlify Forms
- Custom backend

---

## File Structure

```
marbella-site-v2/
├── index.html              # Homepage
├── villa-monterray.html    # Villa 1
├── villa-vanilla.html      # Villa 2
├── villa-sierra.html       # Villa 3
├── villa-ampola.html       # Villa 4
├── css/
│   └── styles.css         # All styles
├── edited-photos/         # All images (optimized)
└── vercel.json            # Vercel config
```

---

## Testing Locally

Open `index.html` in your browser to test before deploying.

**Or use a local server:**

```bash
# Python 3
python3 -m http.server 8000

# Node.js (if you have it)
npx serve
```

Then visit: `http://localhost:8000`

---

## Post-Deployment Checklist

- [ ] Test all villa pages load
- [ ] Click WhatsApp links (should open WhatsApp)
- [ ] Click phone links (should prompt to call)
- [ ] Test on mobile
- [ ] Share with friend to test externally

---

## What's NOT Included Yet

- For Owners page
- Privacy & Terms pages
- Form submission handling
- Analytics tracking
- Cookie consent

These can be added after launch.

---

## Support

If deployment fails:
1. Check all files are in the folder
2. Verify image paths (should be `edited-photos/filename.jpg`)
3. Check Vercel build logs for errors
4. Make sure `vercel.json` is present

**Vercel is free for:**
- Static sites (like this)
- Custom domains
- Automatic HTTPS
- Global CDN
- Unlimited bandwidth

Perfect for your needs.

---

## Next Steps After Launch

1. **Analytics:** Add Google Analytics or Plausible
2. **SEO:** Submit sitemap to Google Search Console
3. **Forms:** Connect owner submission form
4. **Content:** Add more villa details as available
5. **Photography:** Replace with professional photos when budget allows

Your site is production-ready as-is. Launch it and start getting bookings!
