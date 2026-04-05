# 🏰 Fortress Properties LLC – Website Setup Guide

## 📁 Folder Structure
```
fortress-properties-website/
├── index.html              ← Main website
├── admin/
│   ├── index.html          ← CMS dashboard (login page)
│   └── config.yml          ← CMS settings (DO NOT DELETE)
├── _data/
│   ├── general.json        ← Company info, phone, email, hero text
│   ├── stats.json          ← Hero stats bar numbers
│   ├── about.json          ← About Us content
│   ├── why.json            ← Why Choose Us cards
│   ├── properties/         ← One JSON file per property listing
│   ├── team/               ← One JSON file per team member
│   ├── developers/         ← One JSON file per developer partner
│   └── testimonials/       ← One JSON file per review
├── uploads/                ← All photos you upload via CMS go here
└── images/
    └── logo.png            ← Your logo
```

---

## 🚀 STEP 1 — Upload to GitHub

1. Go to **github.com** and log in as **fortresspropertyauh-rgb**
2. Click **"New repository"** (green button top right)
3. Name it: `fortress-properties-website`
4. Set to **Public**
5. Click **"Create repository"**
6. Click **"uploading an existing file"** link
7. Drag and drop **ALL files and folders** from this zip
8. Click **"Commit changes"**

---

## 🌐 STEP 2 — Connect to Cloudflare Pages

1. Go to **dash.cloudflare.com** → your account
2. Click **"Workers & Pages"** on the left
3. Click **"Create application"** → **"Pages"** tab
4. Click **"Connect to Git"**
5. Select **GitHub** → authorize → choose `fortress-properties-website`
6. Settings:
   - **Framework preset:** None
   - **Build command:** (leave empty)
   - **Build output directory:** `/` (just a slash)
7. Click **"Save and Deploy"**
8. Wait 1 minute → your site is live at a `.pages.dev` URL

### Connect Your Domain:
1. In Cloudflare Pages → your project → **"Custom domains"**
2. Add: `fortresspropertiesllc.com` and `www.fortresspropertiesllc.com`
3. Cloudflare auto-configures DNS (since you're already on Cloudflare!) ✅

---

## ✏️ STEP 3 — Set Up CMS (Decap CMS)

### A) Enable GitHub OAuth on Cloudflare Pages:
1. Go to **github.com/settings/applications** → **"OAuth Apps"** → **"New OAuth App"**
2. Fill in:
   - **App name:** Fortress Properties CMS
   - **Homepage URL:** `https://fortresspropertiesllc.com`
   - **Authorization callback URL:** `https://api.decapcms.org/callback`
3. Click **"Register application"**
4. Copy your **Client ID** and generate a **Client Secret**
5. Go back to Cloudflare Pages → your project → **"Settings"** → **"Environment variables"**
6. Add:
   - `GITHUB_CLIENT_ID` = (your Client ID)
   - `GITHUB_CLIENT_SECRET` = (your Client Secret)

### B) Access Your CMS:
- Go to: `https://fortresspropertiesllc.com/admin`
- Click **"Login with GitHub"**
- You're in! ✅

---

## 📧 STEP 4 — Connect Contact Form (Formspree)

1. Go to **formspree.io** → Sign up free (use your info@fortresspropertiesllc.com)
2. Click **"New Form"**
3. Name it: "Fortress Properties Contact Form"
4. Copy your **Form ID** (looks like: `xbjvkpqr`)
5. In your CMS: Go to **⚙️ Site Settings** → **"Company Info & Contact"**
6. Paste the Form ID in the **"Formspree Form ID"** field
7. Save → all contact form submissions now go to your Zoho email ✅

**That's it — no backend needed, no coding, 100% free!**

---

## 🖥️ HOW TO USE THE CMS

### Access: `https://fortresspropertiesllc.com/admin`

### Adding a New Property:
1. Click **"🏠 Property Listings"** in left sidebar
2. Click **"New Property"**
3. Fill in: Title, Status, Type, Price, Location, Beds, Baths, Size
4. Upload a photo
5. Click **"Publish"** → live on site in ~60 seconds ✅

### Adding a Team Member:
1. Click **"👥 Team Members"**
2. Click **"New Team Member"**
3. Fill in name, role, upload photo, add WhatsApp number
4. Publish ✅

### Changing Phone Number / Email:
1. Click **"⚙️ Site Settings"** → **"Company Info & Contact"**
2. Update any field
3. Click **"Save"** ✅

### Changing Hero Background Photo:
1. Click **"⚙️ Site Settings"** → **"Company Info & Contact"**
2. Upload a photo in the **"Hero Background Image"** field
3. Save ✅

---

## 📞 SUPPORT
**Website:** fortresspropertiesllc.com
**Email:** info@fortresspropertiesllc.com
**WhatsApp:** +971 50 700 2904
