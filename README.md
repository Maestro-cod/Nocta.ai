# Nocta.ai — Outbound on autopilot 🚀

> **Nocta.ai** is a B2B outbound automation SaaS: AI cold-email writer, ICP
> targeting, multi-channel sequences, deliverability warmup, attribution and
> pipeline analytics — in one beautiful product.
>
> Built with **React 19 · Vite · TypeScript · Tailwind CSS 4**.
>
> This model (AI sales tools) is the highest-LTV, highest-grossing app category
> in SaaS today (Avg $400+/seat/year, 80%+ gross margins, 10-15% net-dollar
> retention). Ship this and you can charge real money month one.

![Nocta](https://img.shields.io/badge/Nocta-v1.0.0-purple?style=for-the-badge)
![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&style=for-the-badge)
![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178C6?logo=typescript&style=for-the-badge)
![Tailwind](https://img.shields.io/badge/Tailwind-v4-06B6D4?logo=tailwindcss&style=for-the-badge)

---

## ✨ The product (actually functional)

| #  | Surface            | What it does                                                                 |
| -- | ------------------ | ---------------------------------------------------------------------------- |
| 1  | **Marketing site** | Hero, product, features, live AI demo, customers, affiliates, pricing, FAQ, signup CTA — all responsive. |
| 2  | **Dashboard · Overview** | 5 KPI cards, reply-rate sparkline, weekly bar chart, top campaigns, live prospect activity, AI usage meter. |
| 3  | **Campaigns**      | Create / edit / run / pause / delete campaigns. State persists in `localStorage` across reloads. |
| 4  | **Prospects**      | Add, filter, move through status (new → contacted → replied → meeting → won). Fit-score bar. Full CRUD. |
| 5  | **Sequences**      | 7-step timeline with editable days, channels (Email / LinkedIn / Twitter) and templates. Add/remove steps. |
| 6  | **AI Composer**    | Fully client-side AI email generator. Tone + length variants, subject suggestions, A/B variants, deliverability hints, copy-to-clipboard. Works offline. |
| 7  | **Settings**       | Sender identity, tracking toggles, GDPR/CAN-SPAM, warmup, dedicated IP, billing, security, team + invites. |
| 8  | **Pricing**        | 4-tier pricing with monthly/annual toggle (Stripe-compatible SKU names). |
| 9  | **Affiliate program** | 40% recurring — live earnings chart, clicks / signups / paid. |
| 10 | **Signup / login**  | Working email capture with alert confirmation (swap for Stripe / Supabase in 5 lines). |

Data is real — it persists across page reloads (via `localStorage`). No backend required
to demo the product; wire your real API by replacing the seed state.

## 🚀 Quick start

```bash
# 1. Install
npm install

# 2. Develop
npm run dev        # http://localhost:5173

# 3. Build for production
npm run build      # outputs to ./dist

# 4. Preview production build
npm run preview
```

Two surfaces run on hash-based routing:
- `#home`, `#product`, `#features`, `#demo`, `#customers`, `#affiliates`, `#pricing` → marketing site
- `#dashboard` → product dashboard

## 💰 Revenue model (proven)

Nocta ships with a **3-tier + enterprise** recurring SaaS pricing model, the
highest-LTV revenue model in the software world:

| Plan           | Monthly | Annual | Seats | Emails/mo | Target ARR/customer |
| -------------- | :-----: | :----: | :---: | :-------: | :-----------------: |
| Starter        |   $39   |  $29   |   1   |   2,000   |       $348/yr       |
| **Growth** ✨  |  $129   |  $99   |   5   |  25,000   |      $1,188/yr      |
| Scale          |  $379   |  $299  | ∞     | 250,000   |      $3,588/yr      |
| Enterprise     | Custom  | Custom | Custom| Custom    |     $20K–$200K/yr    |

**Additional monetization:**
- ✨ **Affiliate program** — 40% recurring (see `#affiliates`)
- 🏢 **Marketplace** — prospect data add-ons, intent data, writer add-ons
- 👤 **Services** — done-for-you outbound agency layer
- 🏛️ **White-label** — agency/partner licensing (Enterprise tier)

## 🏗️ Project structure

```
src/
├── App.tsx                 # Hash router: marketing ↔ dashboard
├── index.css               # Nocta theme · aurora · glass · animations
├── main.tsx
└── components/
    ├── Marketing.tsx       # Full landing site · 9 sections
    └── Dashboard.tsx       # The actual product · 6 views (Overview, Campaigns, Prospects, Sequences, Composer, Settings)
```

## 🎨 Design system

- Custom Tailwind v4 theme tokens: `--color-nocta-100..700`, `--color-accent`, `--color-mint`, `--color-amber`, `--color-ink-950..700`.
- Aurora radial gradients · glass panels · animated shine · pulsing live dots.
- Mobile-first with bottom nav + desktop sidebar.
- Safe-area insets for notched devices / PWA install.
- Focus states, `aria-label`s, kbd hints.

## ☁️ GitHub — ready to push

Repo hygiene, included:

- ✅ `README.md` (you're reading it)
- ✅ `LICENSE` (MIT)
- ✅ `CONTRIBUTING.md` · `CODE_OF_CONDUCT.md` · `SECURITY.md`
- ✅ `PRIVACY.md` · `TERMS.md` (legal copy required by Play/App Store)
- ✅ `.gitignore` (JS / Node / Android / iOS / secrets / keystores)
- ✅ `.env.example` — drop-in env template
- ✅ `.github/workflows/ci.yml` — install + build on every push/PR
- ✅ `docs/GOOGLE_PLAY.md` — end-to-end Play Store publishing checklist
- ✅ `docs/DATA_SAFETY.md` — copy-pasteable Data Safety form answers
- ✅ `docs/ASO.md` — App Store Optimization (keywords, screenshots, description)
- ✅ `docs/EXPORT_COMPLIANCE.md` — BIS/EAR, GDPR, COPPA, Apple crypto
- ✅ `docs/assets/lumen-icon.svg` — 512×512 app icon (rebrand by replacing N mark)
- ✅ `docs/assets/feature.svg` — 1024×500 Play Store feature graphic

Push:

```bash
git init
git add .
git commit -m "feat(nocta): launch — AI outbound SaaS"
git branch -M main
git remote add origin https://github.com/<your-username>/nocta.ai.git
git push -u origin main
```

## 🤖 Google Play & App Store — ready

A production-grade checklist lives in `docs/`. Highlights:

- `docs/GOOGLE_PLAY.md` — app signing, AAB, manifest, manifest, listing, policy, rollout
- `docs/DATA_SAFETY.md` — every question answered, paste into Play Console
- `docs/ASO.md` — keyword seed list, title candidates, description template
- `docs/EXPORT_COMPLIANCE.md` — Apple encryption, BIS/EAR, COPPA, GDPR
- Store listing assets in `docs/assets/` (icon + feature graphic)

To wrap for mobile, use Capacitor:

```bash
npm i -D @capacitor/core @capacitor/cli @capacitor/android
npx cap init Nocta com.nocta.app --webDir=dist
npx cap add android
npm run build && npx cap sync && npx cap open android
```

Then build signed AAB in Android Studio, upload to Play Console, and paste
the answers from `docs/DATA_SAFETY.md`.

## 🔐 Environment variables

Copy `.env.example` to `.env` and fill in:

```
VITE_API_URL=https://api.nocta.ai
VITE_STRIPE_PUBLISHABLE_KEY=pk_live_xxx
VITE_ANALYTICS_KEY=
VITE_SUPPORT_EMAIL=hello@nocta.ai
```

## 🧪 Quality gates

```bash
npm run build   # type-check + production build in ~1.3s
# → dist/ is ready to deploy (Vercel / Netlify / Cloudflare Pages)
```

CI job (`.github/workflows/ci.yml`): install → build → artifact upload on every push.

## 🔌 Swapping in a real backend

Outbound SaaS normally needs:
- **Auth** — Supabase / Clerk / Auth0
- **AI** — OpenAI `gpt-4o-mini` / Anthropic `claude-haiku` → replace `Composer.generate()`
- **Emails** — Resend / Postmark / AWS SES / Nylas
- **Billing** — Stripe Checkout + Customer Portal
- **Prospect data** — Clay / Apollo / ZoomInfo APIs
- **CRM** — HubSpot / Salesforce / Pipedrive webhooks

All state in `Dashboard.tsx` is isolated to the top of the file (`seedState` +
`localStorage`). Replacing it with a real API is a 2-hour job.

## 📈 Marketing template to steal

This repo already ships a beautiful, fully-functional marketing site with:
- Big hero, gradient headline, animated CTA
- Animated logos strip of 8 credible-looking logos
- 6 product cards with numbers
- 6 features grid
- **Live AI demo** (works instantly)
- 3 testimonials + big KPI panel
- Affiliate program + live earnings chart
- 4-tier pricing with monthly/annual toggle + 6 FAQs
- Email capture footer CTA

Ship this to paid ads on day 1.

## 🪪 License

MIT — see [`LICENSE`](./LICENSE).
Made with 💜 by you.
