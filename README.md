# Maple MPSS — Website

The public website for Maple MPSS. Plain HTML, CSS, and a small amount of vanilla JS. No build step.

## Pages

- `index.html` — Home (positioning + service overview)
- `sourcing.html` — Sourcing Services (packaging OEMs · system integrators · general sourcing)
- `ai-services.html` — AI Services (CRM · workflow automation · supply chain optimisation · operations audit)
- `about.html` — About the firm
- `contact.html` — Contact

## Other files

- `style.css` — Shared stylesheet
- `images/` — All site images (see `images/README.md` for the filename list)
- `vercel.json` — Vercel deployment config (clean URLs, cache headers)

## Local preview

No build tool required. Any static server will work:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deployment

Configured for Vercel. Push to GitHub and import the repo into Vercel —
no framework preset needed, Vercel will serve it as static files.

## Images

The site ships with branded placeholder images for slots that don't yet
have real photography. To swap in a real photo:

1. Replace any file in `images/` using the exact same filename
2. Commit and push — Vercel redeploys automatically

See `images/README.md` for the full list of filenames, aspect ratios,
and crop-behaviour controls.


<!-- Trigger redeploy -->
