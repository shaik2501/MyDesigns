# fal.ai — Design Blueprint and Reusable Build Prompt

Source: https://fal.ai/

Use this file as the visual and interaction authority for future developer-platform, AI infrastructure, model marketplace, and technical product websites inspired by this design language. Replace fal branding, product copy, model artwork, customer names, and protected assets with original material.

## Core public page gallery

The `pages/` directory records the stable product surfaces rather than hundreds of changing model-detail pages:

- `home.png` — platform landing page.
- `explore.png` — generative model discovery and filtering.
- `serverless.png` — serverless GPU infrastructure product page.
- `pricing.png` — pricing and usage model.
- `enterprise.png` — enterprise offering and contact entry.
- `about.png` — company story and team positioning.
- `login.png` — authentication entry screen.

## Creative direction

Create a developer-first generative-media platform that feels simultaneously technical, editorial, playful, and fast. Combine a mostly monochrome interface with pale cyan fields, saturated violet panels, electric blue accents, acid yellow highlights, pixel-like halftone creatures, clean model imagery, precise monospace metadata, and oversized dense display typography.

The composition should feel like modern AI infrastructure—not a generic gradient SaaS template. Use strong flat color blocks, narrow rules, sharp cards, code fragments, performance diagrams, and expressive low-resolution decorative graphics.

## Color system

| Role | Approximate value | Use |
|---|---|---|
| Primary ink | `#000000` | Headlines, rules, dark buttons, footer details |
| Primary paper | `#FFFFFF` / `#FAFAFA` | Main reading surfaces and cards |
| Dark surface | `#161618` / `#202022` | Navigation, code, model UI and dark sections |
| Muted dark | `#383A42` | Secondary dark controls and diagrams |
| Pale cyan | `#99EDFF` | Hero field, large product bands, footer |
| Electric blue | `#4078F2` / `#115EF3` | Links, active controls, technical emphasis |
| Deep violet | approximately `#4B16C9` | Major CTA and infrastructure bands |
| Acid yellow | approximately `#E8FF3F` | Decorative highlights and energetic contrast |
| Magenta | approximately `#A626A4` | Pixel illustrations and limited emphasis |
| Muted text | `#787881` and white at 60% opacity | Supporting copy and metadata |

Keep backgrounds predominantly white, black, cyan, or violet. Bright accents should appear as deliberate illustrations, tags, data marks, or one-off panels—not as ambient gradients everywhere.

## Typography

- Primary display and body family: custom `Focal` or a close dense neo-grotesk substitute.
- Technical labels, prices, filters, and code: `Chivo Mono`, monospace.
- Secondary rounded display accents: custom `Public Sans Rounded` or a similar friendly rounded grotesk.
- Rare editorial accent: a custom serif comparable to the site’s `Hal` face.
- Hero heading: very large, black, tightly tracked, compressed line-height; approximately 64–96px desktop.
- Section headlines: 44–72px with line-height near 0.9–1.0.
- Card titles: 16–24px, dense and assertive.
- Body copy: 14–18px with comfortable 1.35–1.55 line-height.
- Technical metadata: 11–14px monospace.

Use hard line breaks as a composition tool. Large headings may occupy three or four compact lines and align directly against illustration fields.

## Layout system

- Full-width bands alternate between white, pale cyan, black, light gray, and saturated violet.
- Main containers sit near 1200–1280px with compact horizontal gutters.
- Use a thin, low-height navigation bar with the logo left, product links centered, and sales/login actions right.
- Hero composition uses large text on the left and pixel/halftone generative graphics across the surrounding canvas.
- Product sections use asymmetric two-column layouts, large empty areas, and modular 2×2 capability cards.
- Model galleries use image-first cards in horizontal or multi-column grids.
- Technical sections combine code samples, architecture diagrams, benchmark UI, logos, and concise explanatory text.
- Footers can become large cyan information fields with dense link columns and an oversized cropped brand mark.

## Shape language

- Most structural geometry is square: `0px` radius dominates.
- Compact controls and cards use 4px or 6px radii.
- Larger media cards may use 8–12px radii.
- Pills are rare and reserved for filters, tags, and status chips.
- Borders are thin, crisp, and neutral; avoid soft neumorphic edges.
- Use large flat rectangles, browser-like panels, code windows, graphs, vertical bars, pixel grids, halftone animal silhouettes, and cropped abstract shapes.

## Imagery and media

- Lead with a curated grid of high-quality generative image and video previews.
- Crop media edge-to-edge inside cards and overlay concise white or black labeling.
- Use model artwork to demonstrate diversity: cinematic scenes, portraits, stylized animation, product imagery, and motion thumbnails.
- Decorative artwork should feel computational: pixel clusters, dithered creatures, skeletal grids, geometric particles, and low-resolution gradients.
- Do not fill every section with photography; alternate rich media with precise technical diagrams and generous white space.

## Components

### Navigation

Create a compact top bar with logo, product/docs/pricing/enterprise/resource links, a light contact-sales button, and a dark login button. Maintain clear focus outlines and collapse to a menu at mobile widths.

### Hero

Use a pale-cyan canvas, an oversized multiline headline, short platform description, two compact CTAs, and playful pixel graphics placed at the edges. The content should communicate the product category within one glance.

### Model gallery

Present model cards as a dense visual row or grid. Each card needs a preview, model/task name, creator or category metadata, and hover feedback. Keep discovery controls technical and concise.

### Capability cards

Build modular cards for APIs, serverless GPUs, dedicated compute, training, or related infrastructure. Use different pale accent fields while maintaining identical typographic hierarchy.

### Benchmark and architecture sections

Combine a large editorial label on one side with benchmark charts, code panels, architecture nodes, or deployment diagrams on the other. Explain performance using simple visual evidence rather than decorative dashboard clutter.

### Pricing

Keep pricing transparent and technical. Use clear units, monospace numbers, structured tables/cards, and short caveats. Highlight the recommended or most common option with color, not excessive shadows.

### Authentication

Use a focused, compact sign-in screen that inherits the black/white/cyan system. Keep third-party authentication options and legal text visually subordinate. Avoid unrelated promotional density.

### Footer

Use a cyan closing field with dense multi-column navigation, legal links, product/model shortcuts, social links, and a very large cropped logo or mark.

## Motion and interaction

- Use quick 150–250ms state changes for buttons, links, filters, and cards.
- Model previews may animate only when visible or hovered.
- Pixel illustrations can drift, pulse, or assemble subtly.
- Charts and architecture paths may reveal on scroll.
- Avoid heavy parallax that competes with model media.
- Respect `prefers-reduced-motion` and provide static preview frames.

## Responsive behavior

- Scale large headings with `clamp()` and preserve tight leading.
- Stack asymmetric desktop sections into a single readable column.
- Change four-card model rows to two columns and then one or a controlled horizontal scroller.
- Keep filter and search controls reachable without horizontal page overflow.
- Reduce decorative pixel artwork before reducing core content.
- Convert dense footer link columns into grouped sections.
- Maintain a minimum 44px interaction target on touch devices.

## Accessibility

- Maintain strong black/white contrast and verify text placed on cyan, violet, and media.
- Provide text labels for icons and meaningful alt text for generated media examples.
- Never communicate model status, performance, or price using color alone.
- Preserve visible keyboard focus on navigation, model cards, filters, and forms.
- Pause animated previews when off-screen and honor reduced-motion settings.
- Use the display face only where large enough to remain legible; keep longer technical copy in a clean sans or monospace face.

## Reusable generation prompt

Design a responsive developer-first generative-media and AI-infrastructure platform with a white and near-black editorial foundation, broad pale-cyan sections, saturated violet CTA bands, electric-blue controls, acid-yellow and magenta pixel accents, oversized tightly spaced neo-grotesk headings, Chivo Mono technical metadata, square cards, thin rules, compact buttons, media-first model galleries, code panels, benchmark diagrams, serverless infrastructure cards, transparent pricing, a restrained login screen, and a dense cyan footer. Use computational halftone creatures and pixel clusters as decorative motifs. Keep layouts asymmetric but precise, alternate expressive media with generous white space, and avoid generic glassmorphism or ambient gradient SaaS styling.

## Do not

- Do not copy fal’s logo, product copy, model artwork, customer quotes, or partner marks.
- Do not turn the interface into a rounded pastel dashboard.
- Do not replace the flat cyan/violet blocks with vague gradients.
- Do not over-round cards or add soft floating shadows everywhere.
- Do not use decorative display typography for code, prices, filters, or long paragraphs.
- Do not archive every frequently changing model-detail page; use the core gallery as the stable system reference.
