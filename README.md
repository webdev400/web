# Zapienz — Company Website

**Company:** Socrates AI | **Product:** Zapienz — Artificial intelligence for kids  
**Website domain:** `https://www.zapienz.app`  
**Deploy target:** Netlify (connected to this GitHub repo)  
**Contact email:** info@zapienz.app

---

## Purpose

This website is the public-facing presence for Zapienz. It serves two goals:
1. Establish company legitimacy for the **Google Cloud for Startups** application (Scale Tier AI — up to $350K in credits)
2. Communicate Zapienz's mission, product, and team to parents, schools, and institutional partners

The website domain and email must match for the Google Cloud application. See `../Grants/Google/CHECKLIST_Google_Cloud_for_Startups.md`.

---

## Tech Stack

- **HTML5 + CSS3 + Vanilla JS** — no build step, deploys directly to Netlify
- **Tailwind CSS** via CDN — utility-first styling, no npm required
- **Google Fonts** — Inter (body) + Poppins (headings)
- **Multi-page** — one HTML file per page

---

## Site Structure

```
Website/
├── index.html              ← Home: hero, features summary, traction, CTA
├── about.html              ← About: company story, mission, vision, problem
├── features.html           ← Product: full feature breakdown + app screenshots
├── team.html               ← Team: 6 founders with photos and bios
├── contact.html            ← Contact: form + email + address
├── assets/
│   ├── css/
│   │   └── styles.css      ← Custom styles (animations, brand overrides)
│   ├── js/
│   │   └── main.js         ← Mobile nav, scroll effects, smooth scroll
│   └── images/
│       ├── logo.png        ← Zapienz logo (copy from ../Branding/)
│       ├── team/           ← Team photos (extract from pitch deck as PNG)
│       │   ├── team-adrian-fernandez.png
│       │   ├── team-agustin-mailing.png
│       │   ├── team-antonio-dell-ossa.png
│       │   ├── team-pablo-chehade.png
│       │   ├── team-german-mailing.png
│       │   └── team-gladys-damsky.png
│       └── screenshots/    ← App screenshots (extract from pitch deck as PNG)
│           ├── app-chat.png
│           ├── app-profiles.png
│           └── app-alerts.png
├── content/
│   └── about-us.md         ← ✅ Full company content reference (already written)
└── netlify.toml            ← ✅ Netlify deploy config (already written)
```

---

## Brand Colors

| Name | Hex | Usage |
|---|---|---|
| Navy Blue | `#1B2F6E` | Primary text, nav, headings, buttons |
| Red | `#E8323C` | Accent, highlights, CTA hover |
| Light Blue | `#6BB8E8` | Secondary elements, icons, owl |
| White | `#FFFFFF` | Backgrounds, card surfaces |
| Light Gray | `#F5F7FB` | Section backgrounds |
| Dark Gray | `#2D2D2D` | Body text |

---

## Pages — Content Summary

### `index.html` — Home
- **Hero:** "Artificial Intelligence for Kids" — tagline, 2 CTAs (Learn More + Contact)
- **Why Zapienz:** 3-card row (Safety, Learning, Skills)
- **How it works:** Brief dual-interface explanation with screenshot
- **Traction:** Telecentro, Ministry of Education Buenos Aires, schools signing up
- **App download:** Placeholder badges (App Store + Google Play — links TBD)
- **Footer:** Logo, nav links, email, address

### `about.html` — About Us
- Company story + founding context
- Mission & Vision
- The problem we solve
- Market opportunity (Argentina 1.9M, Global 570M, US$230M market)
- Business model (Freemium + B2B)
- Full content in `content/about-us.md`

### `features.html` — Features
- Feature cards: Adapted Content, Security, Dual Interface, Red Flags System, Education
- App screenshots with captions
- Safety features for parents breakdown
- Benefits: Peace of Mind, Learning, Skills

### `team.html` — Our Team
- Intro: "A team passionate about innovation and technology"
- 6 team member cards with photo, name, role, bio
- Contact info for Adrian (Founder)

### `contact.html` — Contact
- Contact form (name, email, message, submit)
- Corporate email: info@zapienz.app
- Address: Virrey del Pino 2166, C.A.B.A., Buenos Aires, Argentina
- Phone/WhatsApp: +54 9 11 6111 2369
- LinkedIn link for Adrian Fernandez

---

## Instructions for Claude Code

1. **Build each HTML page** based on the page summaries above and `content/about-us.md`
2. **Use Tailwind CSS via CDN** — add this to every `<head>`:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```
3. **Configure Tailwind brand colors** in a `<script>` block in each page:
   ```js
   tailwind.config = {
     theme: {
       extend: {
         colors: {
           navy: '#1B2F6E',
           red: '#E8323C',
           sky: '#6BB8E8',
         }
       }
     }
   }
   ```
4. **Shared components** — keep the nav and footer consistent across all pages
5. **Mobile responsive** — use Tailwind's responsive prefixes (`sm:`, `md:`, `lg:`)
6. **Image placeholders** — if images are not yet in `assets/images/`, use a placeholder div with the correct aspect ratio and a comment marking what goes there
7. **App store buttons** — include Apple App Store and Google Play badge placeholders. Add a `<!-- TODO: add real links when app is published -->` comment
8. **Domain placeholder** — search for `[YOUR-DOMAIN]` across files and replace when the domain is decided

---

## Deployment (Netlify)

1. Push this `Website/` folder contents to a **separate GitHub repo** (e.g., `zapienz-website`)
2. Connect that repo to Netlify
3. Set publish directory to `/` (root)
4. Point `zapienz.app` to the Netlify site via DNS
5. Verify the domain matches the email used in the Google Cloud billing account

---

## Google Cloud Application Checklist

Before submitting, verify:
- [ ] Website is live at the chosen domain
- [ ] Corporate email (`info@zapienz.app`) matches the website domain
- [ ] Google Cloud billing account uses the same email domain
- [ ] Website clearly describes the company, product, and team
- [ ] No password protection or "coming soon" pages
