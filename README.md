PathFinder
===========

A simple static web app that helps +2 students explore career paths, take a quick interest quiz, browse courses, and find answers in FAQs.

Features
 - Modern landing page with hero, benefits, and a polished Contacts section
 - Quiz that suggests an ideal course stream
 - Courses page with stream filters
 - FAQs page with expandable items
 - Contact form wired to EmailJS with a mailto fallback

Folder Structure
```
C:\code\path
├─ assets
│  ├─ css
│  │  ├─ imageslid.css
│  │  └─ style.css
│  └─ images

│     └─ image.png
├─ pages
│  ├─ courses.html
│  ├─ faq.html
│  └─ quiz.html
├─ index.html
├─ README.md
├─ package-lock.json
└─ node_modules/ (optional, not required for static hosting)
```

Getting Started
 - Option 1: Open `index.html` directly in your browser (double‑click)
 - Option 2: Use a local dev server for correct relative links:
   - VS Code: install the Live Server extension, then "Open with Live Server"
   - Node (no install):
     - `npx serve .` (or)
     - `npx http-server -p 5173`
   - Then open the printed URL (for http-server: `http://localhost:5173`)

Contact Form Email Setup (EmailJS)
The contact form uses EmailJS if configured, otherwise it falls back to opening your email client via `mailto:`.

1. Create a free account at https://www.emailjs.com/
2. Create a Service and a Template in your EmailJS dashboard
3. Get your Public Key, Service ID, and Template ID
4. In `index.html`, replace the placeholders:
   - `YOUR_EMAILJS_PUBLIC_KEY`
   - `YOUR_SERVICE_ID`
   - `YOUR_TEMPLATE_ID`
5. Make sure your template expects fields similar to:
   - `from_name`
   - `from_email`
   - `subject`
   - `message`

After configuring, submissions will be sent to the email tied to your EmailJS service. If EmailJS is not set or fails, users’ mail apps will open with a prefilled message to `support@pathfinder.com`.

Customization
 - Branding: Update the logo text and colors in `index.html`
 - Images: Replace `assets/images/image.png` and adjust the `alt` text
 - Styles: Edit `assets/css/style.css` and `assets/css/imageslid.css`
 - Copy: Update content in `pages/*.html` and the landing sections in `index.html`

Deployment
This is a static site. You can host it on Netlify, Vercel, GitHub Pages, or any static server:
 - Upload the entire folder ensuring the structure under `assets/` and `pages/` remains intact
 - Set the site entry to `index.html`

Notes
 - Some inline styles are present in `index.html` for the navbar/hero/contacts. You can move them to `assets/css/style.css` if you prefer fully external CSS.
 - If you need server-side email (SMTP) instead of EmailJS, add a small backend and point the form submission to it.

License
MIT


