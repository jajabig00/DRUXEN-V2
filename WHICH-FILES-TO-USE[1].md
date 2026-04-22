# 📌 WHICH FILES TO USE - Simple Guide

## 🎯 You Have TWO Deployment Options

---

## Option 1: NETLIFY (Simple - No Real Proxy)

### ✅ What You Get
- Beautiful interface ✅
- Games work ✅
- Apps work ✅
- Themes work ✅
- Cursor glow ✅
- Proxy opens sites in new tabs (not embedded) ⚠️

### 📁 File to Upload
**ONLY upload this ONE file:**
```
NETLIFY-druxen.html
```

### 🚀 How to Deploy
1. Go to [netlify.com](https://netlify.com) and sign up (free)
2. Drag and drop **NETLIFY-druxen.html** into Netlify
3. Done! Site is live

### ⚠️ Important
Sites won't load IN the interface - they'll open in new tabs.
This is because Netlify is static hosting (no backend server).

---

## Option 2: RAILWAY (Full Proxy - Sites Load Inside!)

### ✅ What You Get
- Beautiful interface ✅
- Games work ✅
- Apps work ✅
- Themes work ✅  
- Cursor glow ✅
- **Real proxy - sites load INSIDE the interface** ✅✅✅

### 📁 Files to Upload
Upload the **ENTIRE druxen-proxy folder** containing:

```
druxen-proxy/
├── server.js             ← Backend server (REQUIRED)
├── package.json          ← Dependencies (REQUIRED)
├── public/
│   ├── index.html       ← Frontend (REQUIRED)
│   └── uv.config.js     ← Proxy config (REQUIRED)
├── Procfile              ← Heroku config (optional)
├── README.md             ← Documentation
├── .gitignore            ← Git ignore
└── LICENSE               ← License
```

### 🚀 How to Deploy

#### Method A: Upload to GitHub First (Recommended)
1. Create GitHub account if you don't have one
2. Create new repository
3. Upload entire `druxen-proxy` folder to GitHub
4. Go to [railway.app](https://railway.app)
5. Click "New Project" → "Deploy from GitHub repo"
6. Select your repository
7. Wait 2-3 minutes
8. Click "Generate Domain"
9. Done! Full proxy is live 🎉

#### Method B: Railway CLI (Advanced)
1. Install Railway CLI
2. Run: `railway login`
3. Run: `railway init`
4. Run: `railway up`

### 💰 Cost
- Railway: $5/month (best performance)
- Render: Free tier available
- Heroku: ~$7/month

---

## 🤔 Which Should I Choose?

### Choose NETLIFY if:
- ✅ You just want it online quickly
- ✅ You don't care if sites open in new tabs
- ✅ You want FREE hosting
- ✅ You just want games and apps to work

### Choose RAILWAY if:
- ✅ You want the REAL proxy (sites load inside)
- ✅ You want TikTok, Twitter, YouTube to work IN the interface
- ✅ You're okay paying $5/month
- ✅ You want professional performance

---

## 📂 File Breakdown (What Each File Does)

### Files for NETLIFY
| File | Purpose |
|------|---------|
| **NETLIFY-druxen.html** | Single HTML file with everything. Opens sites in new tabs. |

### Files for RAILWAY (Full Proxy)

| File | Purpose | Required? |
|------|---------|-----------|
| **server.js** | Express server that runs the proxy backend | ✅ YES |
| **package.json** | Lists all the npm packages needed | ✅ YES |
| **public/index.html** | The beautiful frontend interface | ✅ YES |
| **public/uv.config.js** | Ultraviolet proxy configuration | ✅ YES |
| **Procfile** | Tells Heroku how to run the server | Only for Heroku |
| **README.md** | Documentation | No (but helpful) |
| **.gitignore** | Tells Git which files to ignore | No (but helpful) |
| **LICENSE** | MIT License | No |

---

## 🔍 How to Tell if Ultraviolet is Working

### NETLIFY Version (No Ultraviolet)
- Click "TikTok" → Opens in new browser tab
- Type "twitter.com" → Opens in new browser tab
- Console shows: "Druxen - Netlify Version"

### RAILWAY Version (Has Ultraviolet)
- Click "TikTok" → Loads INSIDE the interface
- Type "twitter.com" → Loads INSIDE embedded viewer
- Console shows: "✅ Ultraviolet Service Worker registered"

---

## 🚨 Common Mistakes

### ❌ WRONG: Uploading server.js to Netlify
**Problem:** Netlify can't run Node.js servers
**Solution:** Use NETLIFY-druxen.html instead

### ❌ WRONG: Uploading only index.html to Railway
**Problem:** Railway needs server.js and package.json
**Solution:** Upload entire druxen-proxy folder

### ❌ WRONG: Expecting proxy to work on Netlify
**Problem:** Static hosts can't run proxy backends
**Solution:** Use Railway for real proxy functionality

---

## ✅ Quick Decision Tree

```
Do you want sites to load INSIDE the interface?
│
├─ NO → Use NETLIFY
│        File: NETLIFY-druxen.html
│        Cost: FREE
│        Time: 2 minutes
│
└─ YES → Use RAILWAY
         Files: Entire druxen-proxy folder
         Cost: $5/month
         Time: 5 minutes
```

---

## 📊 Feature Comparison

| Feature | NETLIFY | RAILWAY |
|---------|---------|---------|
| Beautiful UI | ✅ | ✅ |
| Games | ✅ | ✅ |
| Apps | ✅ | ✅ |
| Themes | ✅ | ✅ |
| Cursor Glow | ✅ | ✅ |
| **Proxy (sites load inside)** | ❌ | ✅ |
| **Ultraviolet backend** | ❌ | ✅ |
| Cost | FREE | $5/mo |
| Speed | Fast | Faster |

---

## 🎯 Step-by-Step: What to Do RIGHT NOW

### For NETLIFY (Easy Way):
1. Download **NETLIFY-druxen.html** from outputs
2. Go to netlify.com
3. Drag & drop the file
4. Done!

### For RAILWAY (Full Proxy):
1. Download entire **druxen-proxy** folder from outputs
2. Upload to GitHub (create repo, upload folder)
3. Go to railway.app
4. "Deploy from GitHub repo"
5. Select your repo
6. Wait 3 minutes
7. Click "Generate Domain"
8. Done!

---

## 🆘 Still Confused?

**Question:** Which file is the "proxy"?
**Answer:** 
- NETLIFY version: Everything in one HTML file (no real proxy)
- RAILWAY version: `server.js` is the proxy backend + Ultraviolet in `node_modules`

**Question:** Where is Ultraviolet?
**Answer:** 
- It's installed automatically when Railway runs `npm install`
- The package `@titaniumnetwork-dev/ultraviolet` downloads it
- You don't see the files until deployment

**Question:** Can I just upload everything to Netlify?
**Answer:** No - Netlify can't run the server. Use Railway for full version.

---

## ✨ Summary

**NETLIFY** = One file (`NETLIFY-druxen.html`) = Free = Sites open in new tabs
**RAILWAY** = Full folder (`druxen-proxy/`) = $5/month = Real proxy = Sites load inside

Choose based on what you need! 🚀
