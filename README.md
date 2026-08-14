CUPIDX — Agency Website (Full Stack)
Dark-luxury, gold, crazy-animated agency site with AI chatbot, WhatsApp widget and a lead-capture backend.

Structure
text

cupidx-site/
├── server.js          # Zero-dependency Node.js server + leads API + /admin dashboard
├── data/leads.json    # Captured leads (auto-created)
└── public/            # The website (ALSO deployable as pure static)
    ├── index.html     # Landing page
    ├── services.html
    ├── work.html
    ├── about.html
    ├── contact.html   # Lead form → POST /api/leads
    ├── css/style.css
    └── js/main.js     # cursor, tilt, chatbot ARIA, WhatsApp widget, confetti
Run locally / server
Bash

node server.js          # → http://localhost:3000  |  leads at /admin
Deploy FREE as static (Vercel/Netlify)
Deploy just the public/ folder. The lead form auto-falls back:
saves to localStorage + pushes the visitor to WhatsApp (91XXXXXXXXXX). No code changes needed.

Deploy full-stack FREE
Render.com / Railway free tier → node server.js (no npm install needed — zero deps)
Config
WhatsApp number: 
main.js
 → WA_NUMBER (currently 91XXXXXXXXXX)
Packages/pricing: index.html → PACKAGES section
ARIA chatbot answers: js/main.js → reply() function
