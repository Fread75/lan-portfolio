# Lan Nguyen — Portfolio Website

Astro static site. Single-page scrollable portfolio with 7 case studies.

## Stack

- **Framework**: [Astro](https://astro.build) v4
- **Styling**: Vanilla CSS (component-scoped) + Google Fonts
- **Hosting**: Netlify (recommended) or Vercel

---

## Getting Started

### 1. Install dependencies

```bash
npm install
```

### 2. Start dev server

```bash
npm run dev
```

Open [http://localhost:4321](http://localhost:4321)

### 3. Build for production

```bash
npm run build
```

Output goes to `/dist`.

---

## Customisation checklist

Before going live, update these placeholders:

| File | What to update |
|------|---------------|
| `src/components/Contact.astro` | Real email address + LinkedIn URL |
| `astro.config.mjs` | Real domain in `site:` field |
| `src/components/Projects.astro` | Add real external links for "Visit website", "Visit extranet", etc. |
| `public/` | Add a real profile photo (optional, create a hero image section) |

---

## Deployment to Netlify

### Option A — Git integration (recommended)

1. Push repo to GitHub
2. Go to [netlify.com](https://netlify.com) → **Add new site → Import from Git**
3. Connect your GitHub repo
4. Build settings:
   - **Build command**: `npm run build`
   - **Publish directory**: `dist`
5. Click **Deploy site**
6. Add custom domain in **Site settings → Domain management**

Every `git push` to `main` will auto-deploy. ✓

### Option B — Manual deploy

```bash
npm run build
npx netlify-cli deploy --prod --dir=dist
```

---

## Project structure

```
/
├── public/
│   └── favicon.svg
├── src/
│   ├── components/
│   │   ├── Nav.astro
│   │   ├── Hero.astro
│   │   ├── About.astro
│   │   ├── Projects.astro
│   │   ├── References.astro
│   │   └── Contact.astro
│   ├── layouts/
│   │   └── Base.astro
│   ├── styles/
│   │   └── global.css
│   └── pages/
│       └── index.astro
├── astro.config.mjs
└── package.json
```

---

## Design system

| Token | Value |
|-------|-------|
| `--c-orange` | `#E8630A` (primary accent) |
| `--c-dark` | `#1A1007` (backgrounds, text) |
| `--c-cream` | `#FAF6F0` (section bg) |
| `--font-display` | Playfair Display (headings) |
| `--font-body` | DM Sans (body text) |
| `--font-mono` | DM Mono (labels, tags) |
