# 🚀 EV Charger Installation Near Me — Launch Guide
## evchargerinstallationnearme.co.uk

---

## 📦 What's In This Package

| File | Purpose |
|------|---------|
| `index.html` | The entire website (1,136 companies, all pages) |
| `sitemap.xml` | 1,165 URLs for Google Search Console |
| `robots.txt` | Tells search crawlers where to go |
| `404.html` | Custom not-found page with redirect |
| `_redirects` | Netlify routing rules |
| `netlify.toml` | Netlify security headers + caching |
| `_headers` | Cloudflare Pages headers |
| `LAUNCH-GUIDE.md` | This file |

---

## ✅ OPTION 1 — Netlify (RECOMMENDED, Free)

**Best for:** Easiest setup, free HTTPS, fastest for beginners.

### Step 1 — Sign up
1. Go to **netlify.com** and sign up (free)
2. Click **"Add new site"** → **"Deploy manually"**

### Step 2 — Deploy
1. Open this folder on your computer
2. **Drag the entire folder** into the Netlify deploy dropzone
3. Netlify will give you a temporary URL like `random-name.netlify.app` — your site is live instantly

### Step 3 — Connect your domain
1. In Netlify → **Site settings** → **Domain management** → **Add custom domain**
2. Enter: `evchargerinstallationnearme.co.uk`
3. Also add: `www.evchargerinstallationnearme.co.uk`

### Step 4 — Update your DNS
Log into your domain registrar (GoDaddy, 123-Reg, Namecheap, etc.) and update:

**Option A — Netlify nameservers (easiest):**
Change your nameservers to:
```
dns1.p01.nsone.net
dns2.p01.nsone.net
dns3.p01.nsone.net
dns4.p01.nsone.net
```

**Option B — DNS records (if you want to keep existing nameservers):**
```
Type    Name    Value                        TTL
A       @       75.2.60.5                   3600
CNAME   www     your-site-name.netlify.app  3600
```

### Step 5 — Enable HTTPS
1. Netlify → **Site settings** → **Domain management** → **HTTPS**
2. Click **"Verify DNS configuration"**
3. Click **"Provision certificate"** — free Let's Encrypt SSL in ~2 minutes

✅ **Done! Your site is live with HTTPS.**

---

## ✅ OPTION 2 — Cloudflare Pages (Fastest CDN)

**Best for:** Maximum speed worldwide, if you already use Cloudflare.

### Step 1 — Sign up
1. Go to **pages.cloudflare.com** and log in
2. Click **"Create a project"** → **"Direct Upload"**

### Step 2 — Deploy
1. Click **"Upload assets"**
2. Select all files from this folder
3. Give your project a name: `ev-charger-directory`
4. Click **"Deploy site"**

### Step 3 — Connect your domain
1. In Cloudflare Pages → your project → **Custom domains** → **Set up a custom domain**
2. Enter: `evchargerinstallationnearme.co.uk`
3. If your domain is already on Cloudflare, DNS is set automatically
4. If not, add these DNS records in your registrar:
```
Type    Name    Value
CNAME   @       your-project.pages.dev
CNAME   www     your-project.pages.dev
```

✅ **Done! Cloudflare automatically provides HTTPS.**

---

## ✅ OPTION 3 — Existing Web Host (cPanel / FTP)

**Best for:** You already have hosting at 123-Reg, GoDaddy, SiteGround, etc.

### Via cPanel File Manager:
1. Log into your hosting control panel
2. Open **File Manager** → navigate to `public_html` folder
3. **Delete** any existing files in `public_html`
4. Click **Upload** and upload all files from this folder
5. Ensure `index.html` is directly inside `public_html` (not in a subfolder)

### Via FTP (FileZilla):
1. Download FileZilla (free FTP client) from filezilla-project.org
2. Connect using your hosting FTP credentials:
   - Host: `ftp.evchargerinstallationnearme.co.uk`
   - Username: (from your host)
   - Password: (from your host)
   - Port: `21`
3. Navigate to `public_html` on the right panel
4. Drag all files from this folder into `public_html`

---

## 🔍 POST-LAUNCH: Submit to Search Engines

Do these immediately after your site goes live.

### Google Search Console
1. Go to **search.google.com/search-console**
2. Click **"Add property"** → enter `https://evchargerinstallationnearme.co.uk`
3. Verify ownership (HTML file method or DNS TXT record)
4. Go to **Sitemaps** → enter `sitemap.xml` → click **Submit**
5. Go to **URL Inspection** → enter `/` → click **"Request indexing"**

### Bing Webmaster Tools
1. Go to **bing.com/webmasters**
2. Add your site and verify
3. Submit sitemap: `https://evchargerinstallationnearme.co.uk/sitemap.xml`

### Google Business Profile (optional but valuable)
1. Go to **business.google.com**
2. Create a listing for your directory business
3. Link to your website

---

## 📊 Analytics Setup (Recommended)

### Google Analytics 4
1. Go to **analytics.google.com** → create account
2. Create a **Web** property for `evchargerinstallationnearme.co.uk`
3. Copy your **Measurement ID** (format: `G-XXXXXXXXXX`)
4. Add this code just before `</head>` in `index.html`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```
*(Replace `G-XXXXXXXXXX` with your actual ID)*

### Setting Up Lead Tracking Goals
In GA4, create conversion events for:
- `form_submit` — when quote forms are submitted
- `phone_click` — when phone numbers are clicked
- `email_click` — when email links are clicked

---

## 📧 Lead Notifications Setup

Currently form submissions show a success message but don't email you. To receive leads by email, choose one of these:

### Option A — Netlify Forms (Free, if using Netlify)
Add `netlify` attribute to your form tags and Netlify captures all submissions in your dashboard + emails you.

### Option B — Formspree (Free up to 50/month)
1. Sign up at **formspree.io**
2. Create a form and get your endpoint URL
3. Set form `action` to `https://formspree.io/f/YOUR_ID`

### Option C — EmailJS (Free up to 200/month)
1. Sign up at **emailjs.com**
2. Add their SDK and send emails directly from the browser

### Option D — Make.com / Zapier
Connect form submissions to email, CRM (HubSpot, Salesforce), or Slack notifications.

---

## 🔒 HTTPS Checklist

Before launch, confirm:
- [ ] `https://evchargerinstallationnearme.co.uk` loads correctly
- [ ] `http://` automatically redirects to `https://`
- [ ] `www.` version redirects to non-www (or vice versa) — no duplicate content
- [ ] No mixed content warnings in browser console

---

## 📈 SEO Quick-Start Checklist

- [ ] Site submitted to Google Search Console
- [ ] Sitemap submitted (`sitemap.xml`)
- [ ] Google Analytics installed
- [ ] Site loads in under 3 seconds (test at **pagespeed.web.dev**)
- [ ] Mobile-friendly test passes at **search.google.com/test/mobile-friendly**
- [ ] Schema markup validates at **validator.schema.org**
- [ ] Register on Google Business Profile
- [ ] Build first backlinks: list on Yell.com, Thomson Local, Free Index

---

## 🗓️ First 30 Days After Launch

| Week | Action |
|------|--------|
| Week 1 | Submit to Google + Bing. Install analytics. Test all forms. |
| Week 2 | Publish first blog post. Share on LinkedIn. |
| Week 3 | Submit to 5 UK business directories (Yell, Thomson, FreeIndex, Scoot, Yelp UK). |
| Week 4 | Review analytics. Check Search Console for crawl errors. Start link building. |

---

## 🛠️ Technical Specs

- **Type:** Static single-page application (SPA)
- **Size:** ~800KB (all-in-one file)
- **No server required:** Runs entirely in the browser
- **No database:** All 1,136 company records are embedded in the HTML
- **No build tools:** No Node.js, npm, or compilation needed
- **Browser support:** All modern browsers (Chrome, Firefox, Safari, Edge)

---

## 📞 Need Help?

If you need assistance with deployment, domain setup, or customisation, the key files to work with are:
- `index.html` — edit the companies array to add/update listings
- `sitemap.xml` — update when adding new pages
- `robots.txt` — no changes normally needed

---

*Package prepared: March 2026*
*Domain: evchargerinstallationnearme.co.uk*
*Listings: 1,136 OZEV-approved companies*
