# 🌐 Druxen - Unblocked Proxy

A fully functional web proxy powered by [Ultraviolet](https://github.com/titaniumnetwork-dev/Ultraviolet) with a beautiful space-themed interface.

![Version](https://img.shields.io/badge/version-2.1.0-blue)
![Node](https://img.shields.io/badge/node-%3E%3D18.0.0-brightgreen)
![License](https://img.shields.io/badge/license-MIT-green)

## ✨ Features

- 🔐 **Ultraviolet Proxy** - Access blocked websites (TikTok, Twitter, YouTube, Discord, etc.)
- 🎮 **50+ Unblocked Games** - Built-in game library
- 📱 **12 Popular Apps** - Quick access to useful web apps
- 🎨 **7 Color Themes** - Customize your experience
- ⭐ **Animated Starfield** - Beautiful space background
- 📱 **Fully Responsive** - Works on desktop, tablet, and mobile
- 🚀 **Fast & Secure** - No logging, encrypted traffic

## 🚀 Quick Start

### Prerequisites

- Node.js 18.0.0 or higher ([Download](https://nodejs.org/))
- npm (comes with Node.js)

### Installation

1. **Clone or download this repository**
   ```bash
   git clone https://github.com/yourusername/druxen-proxy.git
   cd druxen-proxy
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the server**
   ```bash
   npm start
   ```

4. **Open in browser**
   ```
   http://localhost:8080
   ```

That's it! Your proxy is now running locally.

## 📦 Project Structure

```
druxen-proxy/
├── server.js              # Express server with Ultraviolet
├── package.json           # Dependencies and scripts
├── public/
│   ├── index.html        # Main HTML (with Ultraviolet integration)
│   └── uv.config.js      # Ultraviolet configuration
└── README.md             # This file
```

## 🌍 Deployment

### Deploy to Railway (Recommended - ~$5/month)

Railway provides the best performance and reliability.

1. **Sign up at [Railway.app](https://railway.app)**
2. **Click "New Project" → "Deploy from GitHub repo"**
3. **Select this repository**
4. Railway auto-detects Node.js and deploys
5. **Get your URL** (e.g., `https://druxen.up.railway.app`)

**Environment Variables (Optional):**
- `PORT` - Auto-set by Railway (default: 8080)

### Deploy to Render (Free Tier Available)

1. **Sign up at [Render.com](https://render.com)**
2. **Click "New +" → "Web Service"**
3. **Connect your GitHub repository**
4. **Settings:**
   - Build Command: `npm install`
   - Start Command: `npm start`
5. Click **"Create Web Service"**

### Deploy to Replit (Free)

1. **Go to [Replit.com](https://replit.com)**
2. **Click "Create Repl" → "Import from GitHub"**
3. **Paste repository URL**
4. Click **"Run"** - your proxy is live!

### Deploy to Fly.io (~$3/month)

1. **Install Fly CLI**
   ```bash
   curl -L https://fly.io/install.sh | sh
   ```

2. **Login and deploy**
   ```bash
   fly auth login
   fly launch
   fly deploy
   ```

### Deploy to Heroku

1. **Install Heroku CLI** ([Download](https://devcenter.heroku.com/articles/heroku-cli))

2. **Create and deploy**
   ```bash
   heroku login
   heroku create druxen-proxy
   git push heroku main
   heroku open
   ```

## 🛠️ Development

### Run in development mode with auto-restart

```bash
npm run dev
```

This uses `nodemon` to automatically restart the server when you make changes.

### Customize

**Change themes:** Edit CSS variables in `public/index.html` (lines 9-30)

**Add games:** Update the `GAMES` array in `public/index.html` (around line 750)

**Add apps:** Update the `APPS` array in `public/index.html` (around line 775)

**Modify proxy settings:** Edit `public/uv.config.js`

## 🔧 Configuration

### Ultraviolet Config (`public/uv.config.js`)

```javascript
self.__uv$config = {
  prefix: '/service/',      // Proxy URL prefix
  bare: '/bare/',           // Bare server endpoint
  encodeUrl: Ultraviolet.codec.xor.encode,
  decodeUrl: Ultraviolet.codec.xor.decode,
  handler: '/uv/uv.handler.js',
  bundle: '/uv/uv.bundle.js',
  config: '/uv/uv.config.js',
  sw: '/uv/uv.sw.js',
};
```

### Server Config (`server.js`)

Change the port by setting the `PORT` environment variable:

```bash
PORT=3000 npm start
```

## 🐛 Troubleshooting

### Issue: "Cannot find module '@titaniumnetwork-dev/ultraviolet'"

**Solution:** Run `npm install` to install dependencies.

### Issue: "Port 8080 already in use"

**Solution:** Kill the process using port 8080 or change the port:
```bash
PORT=3000 npm start
```

### Issue: Service Worker not registering

**Solution:** Make sure you're accessing via `http://localhost` or `https://`. Service workers don't work on IP addresses without HTTPS.

### Issue: Websites not loading through proxy

**Possible causes:**
1. Service Worker not registered - check browser console
2. Bare server not running - check server logs
3. Website has aggressive anti-proxy measures

### Issue: "npm install" fails

**Solution:** Make sure you have Node.js 18+ installed:
```bash
node --version  # Should be v18.0.0 or higher
```

## 📝 Scripts

| Command | Description |
|---------|-------------|
| `npm start` | Start production server |
| `npm run dev` | Start development server with auto-reload |

## ⚠️ Important Notes

### Legal Considerations
- This proxy is for **educational purposes** only
- Some schools/workplaces prohibit proxy usage - check your organization's policies
- Respect website terms of service
- Don't use for illegal activities

### Technical Limitations
- Some websites (Netflix, banking sites) have advanced anti-proxy measures
- YouTube may be slow due to video streaming through proxy
- Some sites may detect and block proxy traffic

### Privacy
- This proxy **does not log** your browsing activity
- Traffic is encrypted between you and the proxy server
- The destination website can still see the proxy server's IP address

## 🤝 Contributing

Contributions are welcome! Here's how:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Credits

- **Ultraviolet** - [TitaniumNetwork-dev](https://github.com/titaniumnetwork-dev/Ultraviolet)
- **Bare Server** - [tomphttp](https://github.com/tomphttp/bare-server-node)
- **Font** - Orbitron & Exo 2 from Google Fonts

## 📧 Support

If you encounter issues:

1. Check the [Troubleshooting](#-troubleshooting) section
2. Search existing [GitHub Issues](https://github.com/yourusername/druxen-proxy/issues)
3. Create a new issue with:
   - Your Node.js version (`node --version`)
   - Error messages from console
   - Steps to reproduce

## 🌟 Star This Repo

If you find this useful, please star the repository! It helps others discover the project.

---

Made with 💙 by the Druxen Team
