# Zapienz Website — Instructions for Claude Code

You are building the public website for **Zapienz** by **Socrates AI**.
Read `README.md` for the full spec. This file gives you the quick-start directives.

## Your Job

Build a clean, fast, professional multi-page website using plain HTML + Tailwind CSS (CDN).
No npm, no build step. Every page must work by opening the HTML file directly or via Netlify.

## Brand

| Token | Value |
|---|---|
| Primary (navy) | `#1B2F6E` |
| Accent (red) | `#E8323C` |
| Secondary (sky blue) | `#6BB8E8` |
| Background light | `#F5F7FB` |
| Body text | `#2D2D2D` |
| Font headings | Poppins (Google Fonts) |
| Font body | Inter (Google Fonts) |

Add this to every `<head>`:
```html
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@600;700&family=Inter:wght@400;500&display=swap" rel="stylesheet">
<script src="https://cdn.tailwindcss.com"></script>
<script>
  tailwind.config = {
    theme: {
      extend: {
        colors: {
          navy: '#1B2F6E',
          brand: '#E8323C',
          sky: '#6BB8E8',
        },
        fontFamily: {
          heading: ['Poppins', 'sans-serif'],
          body: ['Inter', 'sans-serif'],
        }
      }
    }
  }
</script>
```

## Pages to Build

| File | Purpose |
|---|---|
| `index.html` | Hero + features + traction + CTA |
| `about.html` | Company story, mission, vision, market |
| `features.html` | Full product breakdown + screenshots |
| `team.html` | 6 founder cards with photos and bios |
| `contact.html` | Contact form + info |

Use `content/about-us.md` as the content source for all pages.

## Shared Nav (every page)

```
Logo | Home  About  Features  Team  Contact  [Contact Us button]
```
- Logo: `assets/images/logo.png`
- Active page link gets navy underline
- Mobile: hamburger menu

## Shared Footer (every page)

```
Logo + tagline | Nav links | Contact info | © 2025 Socrates AI
```

## Key Sections — index.html

1. **Hero** — Full-width, navy background. Headline: "AI Made Safe for Kids." Subheadline from mission. Two buttons: "Learn More" (→ features.html) and "Contact Us" (→ contact.html). Show logo.
2. **Why Zapienz** — 3 cards: Peace of Mind / Learning / Skills (from deck).
3. **How it Works** — Two columns: Child Interface + Parent Interface. Use `screenshots/app-chat.png` and `screenshots/app-parental-controls.png`.
4. **Red Flags** — Dark navy band. Bold headline about the alert system. Show `screenshots/app-alerts-full-slide.png` or description cards.
5. **Traction** — 3 partner logos/badges: Telecentro · Ministry of Education Buenos Aires · Schools. Plus "$40K seed funded".
6. **App Download** — Two badges (App Store + Google Play). Use placeholder `#` links with `<!-- TODO: add real links -->` comment.
7. **Footer**

## Images Available

```
assets/images/logo.png
assets/images/team/team-adrian-fernandez.png
assets/images/team/team-agustin-mailing.png
assets/images/team/team-antonio-dell-ossa.png
assets/images/team/team-pablo-chehade.png
assets/images/team/team-german-mailing.png
assets/images/team/team-gladys-damsky.png
assets/images/screenshots/app-chat.png
assets/images/screenshots/app-profiles.png
assets/images/screenshots/app-parental-controls.png
assets/images/screenshots/app-alerts-full-slide.png
```

## Domain & Contact

| Item | Value |
|---|---|
| Website | `https://www.zapienz.app` |
| Corporate email | `info@zapienz.app` |
| Founder email | `adrian@zapienz.app` |
| Phone / WhatsApp | `+54 9 11 6111 2369` |
| Address | Virrey del Pino 2166, C.A.B.A., Buenos Aires, Argentina |

Use these exact values everywhere in the site. No placeholders.

## Deployment

Push to GitHub → Netlify auto-deploys. Config is in `netlify.toml`.
See `README.md` → Deployment section for full steps.
