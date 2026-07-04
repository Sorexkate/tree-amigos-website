# Tree Amigos Landscaping — Website Setup

This is a single static site: `index.html` + an `images/` folder. No build step,
no npm, no server required. It works by just opening the file, and deploys in
minutes to Vercel or Netlify.

## 1. Photos — already in place

Your logo and real project photos are already added and wired in:
- `images/logo.png` — your logo, in the nav bar and footer
- `images/hero.jpg` — the topiary yard shot, as the homepage background
- `images/gallery/*.jpg` — 12 real project photos across Patios, Walkways,
  Landscaping, and Trees

Two optional slots are still open (`images/gallery/mulch-1.jpg` and
`images/gallery/snow-1.jpg`) since there wasn't a dedicated photo for those
yet — just drop a file in with that exact name later and it'll appear
automatically. Nothing breaks in the meantime; it shows a clean color
placeholder instead.

Want to add more photos, swap one out, or change a caption? Open `index.html`,
search for `galleryData`, and edit the list — each line is one photo with a
category, caption, and filename.

## 2. Set up the estimate form (5 min)

The form needs somewhere to send submissions:

1. Go to https://formspree.io and create a free account (free tier covers 50 submissions/month — plenty to start).
2. Create a new form, copy the form endpoint it gives you (looks like `https://formspree.io/f/abc123`).
3. Open `index.html`, search for `your-form-id`, and replace that whole URL with the one Formspree gave you.
4. Submissions will land in the email you signed up with.

## 3. Deploy — free, live in ~2 minutes

**Vercel** (recommended):
1. Go to https://vercel.com and sign up with your GitHub account.
2. Click "Add New Project," select your repository, click Deploy.
3. You'll get a live URL immediately (something like `Tree-amigos-NJ.vercel.app`).

**Netlify** works the same way if you prefer it — https://netlify.com, "Add new site" → "Import an existing project" → pick the repo.

Either way: every time you push a change to GitHub (like adding new photos), the live site updates automatically within a minute or two.

## 5. Add your own domain (optional, ~15 min, ~$12/year)

1. Buy a domain (e.g. `TreeAmigosNJ.com`) from Namecheap or a similar registrar.
2. In your Vercel/Netlify project settings, go to "Domains" and add it.
3. Follow the DNS instructions it gives you (usually just adding one or two records at your registrar) — it walks you through it.
4. SSL (the padlock/https) is automatic and free on both platforms.

Until you buy a domain, the free `.vercel.app` or `.netlify.app` link is a fully working, shareable website — good enough to go live with today.

## What's in this version (Phase 1)

Home (hero, services, why-us, testimonials, CTA) + Gallery + Contact/estimate
form. No login, client portal, admin dashboard, or invoicing — that's
intentionally left out of this build and can be scoped separately later if
you want it.
