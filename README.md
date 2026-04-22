🌐 Druxen - Unblocked Proxy

A fully functional web proxy powered by Ultraviolet with a beautiful space-themed interface.

Version Node License
✨ Features

    🔐 Ultraviolet Proxy - Access blocked websites (TikTok, Twitter, YouTube, Discord, etc.)
    🎮 50+ Unblocked Games - Built-in game library
    📱 12 Popular Apps - Quick access to useful web apps
    🎨 7 Color Themes - Customize your experience
    ⭐ Animated Starfield - Beautiful space background
    📱 Fully Responsive - Works on desktop, tablet, and mobile
    🚀 Fast & Secure - No logging, encrypted traffic

🚀 Quick Start
Prerequisites

    Node.js 18.0.0 or higher (Download)
    npm (comes with Node.js)

Installation

    Clone or download this repository

    git clone https://github.com/yourusername/druxen-proxy.git
    cd druxen-proxy

    Install dependencies

    npm install

    Start the server

    npm start

    Open in browser

    http://localhost:8080

That's it! Your proxy is now running locally.
📦 Project Structure

druxen-proxy/
├── server.js              # Express server with Ultraviolet
├── package.json           # Dependencies and scripts
├── public/
│   ├── index.html        # Main HTML (with Ultraviolet integration)
│   └── uv.config.js      # Ultraviolet configuration
└── README.md             # This file

🌍 Deployment
Deploy to Railway (Recommended - ~$5/month)

Railway provides the best performance and reliability.

    Sign up at Railway.app
    Click "New Project" → "Deploy from GitHub repo"
    Select this repository
    Railway auto-detects Node.js and deploys
    Get your URL (e.g., https://druxen.up.railway.app)

Environment Variables (Optional):

    PORT - Auto-set by Railway (default: 8080)

Deploy to Render (Free Tier Available)

    Sign up at Render.com
    Click "New +" → "Web Service"
    Connect your GitHub repository
    Settings:
        Build Command: npm install
        Start Command: npm start
    Click "Create Web Service"

Deploy to Replit (Free)

    Go to Replit.com
    Click "Create Repl" → "Import from GitHub"
    Paste repository URL
    Click "Run" - your proxy is live!

Deploy to Fly.io (~$3/month)

    Install Fly CLI

    curl -L https://fly.io/install.sh | sh

    Login and deploy

    fly auth login
    fly launch
    fly deploy

Deploy to Heroku

    Install Heroku CLI (Download)

    Create and deploy

    heroku login
    heroku create druxen-proxy
    git push heroku main
    heroku open

🛠️ Development
Run in development mode with auto-restart

npm run dev

This uses nodemon to automatically restart the server when you make changes.
Customize

Change themes: Edit CSS variables in public/index.html (lines 9-30)

Add games: Update the GAMES array in public/index.html (around line 750)

Add apps: Update the APPS array in public/index.html (around line 775)

Modify proxy settings: Edit public/uv.config.js
🔧 Configuration
Ultraviolet Config (public/uv.config.js)

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

Server Config (server.js)

Change the port by setting the PORT environment variable:

PORT=3000 npm start

🐛 Troubleshooting
Issue: "Cannot find module '@titaniumnetwork-dev/ultraviolet'"

Solution: Run npm install to install dependencies.
Issue: "Port 8080 already in use"

Solution: Kill the process using port 8080 or change the port:

PORT=3000 npm start

Issue: Service Worker not registering

Solution: Make sure you're accessing via http://localhost or https://. Service workers don't work on IP addresses without HTTPS.
Issue: Websites not loading through proxy

Possible causes:

    Service Worker not registered - check browser console
    Bare server not running - check server logs
    Website has aggressive anti-proxy measures

Issue: "npm install" fails

Solution: Make sure you have Node.js 18+ installed:

node --version  # Should be v18.0.0 or higher

📝 Scripts
Command 	Description
npm start 	Start production server
npm run dev 	Start development server with auto-reload
⚠️ Important Notes
Legal Considerations

    This proxy is for educational purposes only
    Some schools/workplaces prohibit proxy usage - check your organization's policies
    Respect website terms of service
    Don't use for illegal activities

Technical Limitations

    Some websites (Netflix, banking sites) have advanced anti-proxy measures
    YouTube may be slow due to video streaming through proxy
    Some sites may detect and block proxy traffic

Privacy

    This proxy does not log your browsing activity
    Traffic is encrypted between you and the proxy server
    The destination website can still see the proxy server's IP address

🤝 Contributing

Contributions are welcome! Here's how:

    Fork the repository
    Create a new branch (git checkout -b feature/amazing-feature)
    Commit your changes (git commit -m 'Add amazing feature')
    Push to the branch (git push origin feature/amazing-feature)
    Open a Pull Request

📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
🙏 Credits

    Ultraviolet - TitaniumNetwork-dev
    Bare Server - tomphttp
    Font - Orbitron & Exo 2 from Google Fonts

📧 Support

If you encounter issues:

    Check the Troubleshooting section
    Search existing GitHub Issues
    Create a new issue with:
        Your Node.js version (node --version)
        Error messages from console
        Steps to reproduce

🌟 Star This Repo

If you find this useful, please star the repository! It helps others discover the project.

Made with 💙 by the Druxen Team
