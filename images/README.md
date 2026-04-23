# Images

This folder holds every image used on the website. The HTML files reference
these by exact filename — to swap a placeholder for a real photo, just
replace the file with the same name and push to GitHub. Vercel redeploys
automatically.

## Important: Any dimensions will work

The site is designed to handle **any image dimensions gracefully**. You do
not need to crop photos to match the specs below. The CSS automatically
centers and covers each frame, so your images will always look framed —
never distorted, never broken.

- **Default behavior:** images are cropped from the center to fill the
  frame. Best for photographs with a roughly centered subject.
- **For full image with no cropping:** add `class="img-contain"` to the
  `<img>` tag in the HTML. The image will be letterboxed inside the frame.
- **For UI screenshots and dashboards:** use `class="img-screenshot"` —
  full image shown, padded, on a white background. Already applied to the
  AI services page screenshots.

The aspect ratios below are **suggestions**, not requirements. They
indicate the shape of the frame, so photos in that aspect will show most
of the image without cropping.

## The 19 image slots

### Homepage (`index.html`)
| Filename | Suggested aspect | Content |
|----------|------------------|---------|
| `hero.jpg` | 21:9 landscape | Homepage hero — currently aerial Chennai shop floor |
| `og-image.jpg` | 1200 x 630 | Social-sharing card (used on every page) |
| `case-parts.jpg` | 4:3 landscape | Case study — currently Chennai machines + stock |

### Sourcing Services (`sourcing.html`)
| Filename | Suggested aspect | Content |
|----------|------------------|---------|
| `sourcing-hero.jpg` | 21:9 landscape | Page header — currently shop-floor wide angle |
| `sourcing-packaging.jpg` | 4:3 landscape | Packaging OEMs subsection — currently Lynx CNC turning |
| `sourcing-integrators.jpg` | 4:3 landscape | System integrators subsection — currently STM VMC |
| `sourcing-general.jpg` | 4:3 landscape | General sourcing subsection (placeholder) |
| `sourcing-materials.jpg` | 4:3 landscape | Material stock photo (placeholder) |
| `sourcing-case.jpg` | 4:3 landscape | Sourcing case study (placeholder) |

### AI Services (`ai-services.html`)
| Filename | Suggested aspect | Content |
|----------|------------------|---------|
| `ai-hero.jpg` | 21:9 landscape | Operations dashboard — representative interface (Maple MPSS-branded mockup) |
| `ai-crm.jpg` | 4:3 landscape | Quote-to-order CRM — representative interface (Maple MPSS-branded mockup) |
| `ai-workflow.jpg` | 4:3 landscape | Operations dashboard with KPIs and feed — representative interface (Maple MPSS-branded mockup) |
| `ai-supplychain.jpg` | 4:3 landscape | Supplier performance scorecard — representative interface (Maple MPSS-branded mockup) |
| `ai-audit.jpg` | 4:3 landscape | Audit findings document — representative deliverable (Maple MPSS-branded mockup) |
| `ai-case.jpg` | 4:3 landscape | Customer reorder portal — representative interface (Maple MPSS-branded mockup) |

### About (`about.html`)
| Filename | Suggested aspect | Content |
|----------|------------------|---------|
| `about-hero.jpg` | 21:9 landscape | Page header — dual-location shot (placeholder) |
| `about-canada.jpg` | 1:1 square | Burlington office (placeholder — needs Canadian photo) |
| `about-india.jpg` | 1:1 square | Chennai facility — currently real photo |

### Contact (`contact.html`)
| Filename | Suggested aspect | Content |
|----------|------------------|---------|
| `contact-hero.jpg` | 21:9 landscape | Page header — desk, drawing, or phone shot (placeholder) |

## Currently real photos vs placeholders

**Real photos (6):**
- `hero.jpg` — Chennai aerial overhead
- `case-parts.jpg` — Chennai machines + stock
- `sourcing-hero.jpg` — Chennai wide-angle shop floor
- `sourcing-packaging.jpg` — DN Solutions Lynx 2100LY (CNC lathe)
- `sourcing-integrators.jpg` — STM VL1300 (vertical machining center)
- `about-india.jpg` — Chennai machines + stock (same as case-parts)

**Branded placeholders (13):** everything else. They use the site's
ivory/oxblood/ink palette so the site looks composed before real
photography is added.

## File format and size

- **JPG recommended** for photos. PNG is fine for screenshots with sharp
  edges or transparency.
- **Aim for 1600–2400px on the long edge** for web. The site uses
  `object-fit: cover`, so images just need to be large enough to look
  sharp on high-density screens.
- **Target file size: 200–400 KB per photo.** Run images through
  [Squoosh](https://squoosh.app) before committing.
- **WebP and AVIF work too** — keep the filename stem the same and update
  the `src` attribute in HTML (e.g., `hero.webp`).

## Changing crop behavior per image

Open the relevant HTML file, find the `<img>` tag, and add a class:

```html
<!-- Default: center-crop to fill frame -->
<img src="images/hero.jpg" alt="..." />

<!-- Letterbox: show full image, no crop -->
<img src="images/hero.jpg" alt="..." class="img-contain" />

<!-- Screenshot: full image on white background, padded -->
<img src="images/hero.jpg" alt="..." class="img-screenshot" />
```

You can also shift the crop focus with an inline style:

```html
<!-- Crop toward the top of the image -->
<img src="images/hero.jpg" alt="..." style="object-position: top;" />

<!-- Crop toward bottom-right -->
<img src="images/hero.jpg" alt="..." style="object-position: bottom right;" />
```
