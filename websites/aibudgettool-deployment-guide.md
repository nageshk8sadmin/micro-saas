# aibudgettool.com — Complete Hosting & Deployment Documentation

**Domain:** aibudgettool.com  
**Stack:** Static frontend (HTML / CSS / JS)  
**Tools used to build:** Lovable, Claude  
**Hosting platform:** Vercel (free) + GitHub (free)  
**Date:** April 2026

---

## 1. Platform Decision Summary

### Recommendation: Vercel (Free) — Not Hostinger

| Feature | Vercel (Free) | Netlify (Free) | Hostinger Horizon |
|---|---|---|---|
| Cost | ₹0 forever | ₹0 forever | ~₹200–400/month |
| Custom domain | Yes, free | Yes, free | 1 year free then paid |
| HTTPS / SSL | Auto, free | Auto, free | Included |
| Bandwidth | 100 GB/month | 100 GB/month | Varies by plan |
| Projects | Unlimited | 500 sites | Limited by plan |
| Deploy from | GitHub (auto) | GitHub / drag-drop | FTP / File Manager |
| Global CDN | Yes | Yes | Add-on cost |
| AdSense ready | Yes | Yes | Yes |

**Conclusion:** Hostinger is not needed for static frontend sites. Vercel is purpose-built for exactly your use case and is free indefinitely.

---

## 2. One-Time Setup: GitHub + Vercel

### Step 1 — Create GitHub Account
- Go to: https://github.com
- Sign up with your email (free)
- Already have one? Skip to Step 2.

### Step 2 — Create a Repository for Each Site
- Click "+" icon → New repository
- Name it (e.g. `aibudgettool`, `age-calculator`, etc.)
- Set to **Public**
- Click "Create repository"
- **One repo per website.**

### Step 3 — Upload Your Website Files
- On the repo page → "Add file" → "Upload files"
- Drag in your HTML/CSS/JS files
- Click "Commit changes"
- **Critical:** Your main file must be named `index.html`

### Step 4 — Create a Vercel Account
- Go to: https://vercel.com
- Click "Sign up" → "Continue with GitHub"
- This links your GitHub account automatically.

### Step 5 — Import and Deploy Project
- Vercel dashboard → "Add New Project"
- "Import Git Repository" → select your repo
- Click **Deploy**
- Vercel auto-detects static HTML sites — no configuration needed.
- Your site is live in ~30 seconds at `yoursite.vercel.app`

---

## 3. Connecting aibudgettool.com Domain (Free)

### Step 6 — Add Domain in Vercel
1. Vercel dashboard → select your project
2. Go to **Settings → Domains**
3. Type `aibudgettool.com` → click Add
4. Vercel shows you two DNS records, for example:

```
A record:      @    →  76.76.19.19
CNAME record:  www  →  cname.vercel-dns.com
```

### Step 7 — Add DNS Records at Your Registrar
1. Log in to wherever you bought the domain (GoDaddy / Namecheap / Google Domains)
2. Go to DNS Settings
3. Delete any existing A records
4. Add the two records Vercel provided above
5. Save changes

> **Note:** DNS propagation takes 10 minutes to 24 hours. This is normal — just wait.

### Step 8 — HTTPS is Automatic
- Vercel generates a free HTTPS/SSL certificate (Let's Encrypt) automatically.
- No setup needed.
- Your site is now live at https://aibudgettool.com with HTTPS + CDN.

---

## 4. Ongoing Update Workflow (30 Seconds)

Every time you update your site:

1. Edit in Lovable or Claude → download updated files
2. Go to your GitHub repo → "Add file" → "Upload files"
3. Replace the old file → click "Commit changes"
4. Vercel detects the change and redeploys automatically in ~30 seconds

**That's the entire workflow.** No FTP, no control panels, no manual deployment steps.

---

## 5. Hosting Multiple Sites

You can host unlimited projects on one Vercel free account:

- Create a new GitHub repo for each site
- Import each repo into Vercel
- Connect a custom domain (or subdomain) to each
- All free, all on the same Vercel account

**Examples:**
- `aibudgettool.com` → aibudgettool GitHub repo
- `worldclocknow.com` → worldclock GitHub repo
- `jpgconvert.tools` → jpgconverter GitHub repo

---

## 6. Traffic and Scaling

| Monthly Visitors | Bandwidth Used | Vercel Free Tier |
|---|---|---|
| 10,000 | ~1–2 GB | Well within free |
| 50,000 | ~5–10 GB | Well within free |
| 100,000 | ~10–20 GB | Well within free |
| 500,000 | ~50–80 GB | Within free (100 GB limit) |
| 1,000,000+ | 100+ GB | May need Vercel Pro (~$20/mo) |

Static files served via CDN are extremely efficient. You're unlikely to hit limits before earning significant AdSense revenue.

---

## 7. Google AdSense Readiness

To qualify for Google AdSense, your site needs:

- [x] Real custom domain (not .vercel.app) — ✅ aibudgettool.com
- [x] HTTPS — ✅ Vercel provides free SSL
- [x] Original content — ✅ your tools provide value
- [ ] Privacy Policy page — add `/privacy.html`
- [ ] About page — add `/about.html`
- [ ] Minimum content — 15–20 pages or a functional tool with content around it

**Site structure recommended for AdSense:**
```
index.html         — main tool / homepage
about.html         — about the tool and site
privacy.html       — privacy policy (required)
contact.html       — contact form or email
blog/              — optional: articles for more content
```

---

## 8. Website Ideas (from your notes)

### Build First — Easy Wins (₹0 cost)
| Tool | Difficulty | Traffic Potential |
|---|---|---|
| World clock / digital clock | Easy | High |
| JPG → PNG converter | Easy | High |
| JPG → PDF converter | Easy | High |
| Age calculator | Easy | High |
| IP address finder | Easy | Medium |
| Unit conversion calculator | Easy | Medium |
| Motivational quotes | Easy | Medium |

### Medium Effort — Good Traffic
| Tool | Notes |
|---|---|
| AI tool comparison / directory | Highest long-term traffic potential |
| To-Do list app | Evergreen, works offline |
| Internet speed test | Needs LibreSpeed + server bandwidth |
| Cloud / construction price calculator | Low competition, good India SEO |
| Web traffic / profit calculator | Business audience = premium AdSense rates |

### Build Later — Complex
| Tool | Why Complex |
|---|---|
| Financial planner + AI advice | Needs AI API (paid per request) |
| Ticketing tool | Needs backend + database |
| Kids website game → Android | Complex; use Capacitor to wrap for Play Store |

---

## 9. Migration to Hostinger — Do You Need It?

**Short answer: No. You will likely never need to migrate.**

Hostinger is the right choice only if you need:
- PHP (server-side scripting)
- MySQL database
- WordPress / CMS
- Email hosting (yourname@aibudgettool.com)
- cPanel for client work

For pure frontend tool sites + AdSense, Vercel is the better platform permanently.

### If You Ever Do Migrate (Simple Process)

1. Download all files from your GitHub repos
2. Log into Hostinger → File Manager
3. Upload files to `public_html`
4. Update DNS records to point to Hostinger's servers
5. Done. Estimated time: under 1 hour per site.

**Hostinger plan to use if migrating:**
- Premium Shared Hosting (~₹200/mo) for up to 100 websites
- Comes with free domain for year 1, free SSL, and email hosting

---

## 10. Cost Summary

| Item | Provider | Cost |
|---|---|---|
| Domain (aibudgettool.com) | Already purchased | ₹0 now |
| Hosting (all sites) | Vercel | ₹0 |
| SSL certificates | Vercel (auto) | ₹0 |
| CDN | Vercel (global) | ₹0 |
| GitHub repos | GitHub | ₹0 |
| **Total monthly cost** | | **₹0** |

---

## 11. Quick Reference Commands

### Lovable → Vercel workflow
```
1. Build in Lovable → Export code (download ZIP)
2. Extract ZIP → ensure main file is index.html
3. GitHub repo → Upload files → Commit
4. Vercel auto-deploys within 30 seconds
```

### Domain DNS records for Vercel
```
Type    Name    Value
A       @       76.76.19.19
CNAME   www     cname.vercel-dns.com
```

### Folder structure for each site
```
my-site/
├── index.html       ← required, this is your homepage
├── about.html
├── privacy.html
├── style.css        ← optional if using inline CSS
└── script.js        ← optional if using inline JS
```

---

## 12. Useful Links

| Resource | URL |
|---|---|
| GitHub | https://github.com |
| Vercel | https://vercel.com |
| Vercel Docs | https://vercel.com/docs |
| Vercel Domain Guide | https://vercel.com/docs/projects/domains |
| Google AdSense | https://adsense.google.com |
| Lovable | https://lovable.dev |
| Free Privacy Policy Generator | https://privacypolicygenerator.info |

---

*Documentation prepared April 2026. All pricing and limits accurate as of this date.*
