# TechQuest × iQOO Z Series — Design Blueprint and Reusable Build Prompt

## Core public page gallery

The `pages/` folder preserves the stable public experience: `home.png`, `mentors.png`, `privacy.png`, `terms.png`, and `register.png`. The registration route currently redirects to the event login entry, so `register.png` also records the authentication design. Dynamic participant or event data is intentionally excluded.

> Use this file as the visual and interaction authority for future pages inspired by this design language. Adapt the copy, brand, content, and images to the new project; preserve the composition logic, typographic hierarchy, color roles, spacing rhythm, component geometry, and responsive behavior described here.

## 1. Reference and scope

- Source audited: <https://techquest.reskilll.com/>
- Live page title: `iQOO Z Series Sneak Peek - First Look + AI Tech Workshop`
- Audit date: 2 September 2026
- Desktop measurement viewport: `1280 × 720 CSS px` at DPR `2`
- Desktop document width observed: `1272px` excluding scrollbar
- Mobile measurement viewport: `390 × 844 CSS px`
- Visual reference: [`iqoo_design_image.png`](iqoo_design_image.png)

This is not a request to copy the source page literally. It is a design grammar for building a new, original page with the same high-energy industrial event aesthetic. Do not reuse protected logos, product renders, city photography, or brand copy unless the project owner has permission.

## 2. One-sentence design direction

Create a premium technology-launch landing page that combines a cinematic black product reveal with energetic iQOO-gold campaign surfaces, compressed editorial typography, generous editorial whitespace, modular information cards, and precise event metadata.

## 3. Visual personality

The design should feel:

- Premium, technical, bold, and fast.
- More like a product launch poster than a generic SaaS page.
- Dense with useful information but visually controlled.
- Industrial rather than playful: hard black/white/gold contrast, short labels, strong rules, compressed headings.
- Human and event-oriented through city photography, schedules, preparation checklists, and progressive disclosure.

Use contrast as the main compositional device. Alternate between:

1. Cinematic black product moments.
2. Clean white editorial sections.
3. Saturated gold action or workshop panels.
4. Warm cream utility sections.

Avoid blue-purple gradients, glassmorphism, soft pastel SaaS styling, oversized abstract blobs everywhere, or excessive card shadows.

## 4. Color system

### 4.1 Core tokens

```css
:root {
  /* Structural colors */
  --color-ink: #000000;
  --color-ink-soft: #1a1a1a;
  --color-ink-muted: #5a5a5a;
  --color-cinematic-black: #0b0b0f;

  /* Brand/action colors */
  --color-primary: #f0b31c;
  --color-primary-deep: #c8920a;
  --color-primary-soft: #fef6dd;

  /* Surfaces */
  --color-white: #ffffff;
  --color-paper: #fafaf7;
  --color-paper-deep: #f2f2ec;
  --color-line: #e8e5db;

  /* Optional location/category accents */
  --color-accent-orange: #e8801f;
  --color-accent-violet: #7c4dda;
  --color-accent-gold: #f0b31c;
  --color-accent-blue: #2e7ce4;
}
```

### 4.2 Color roles

| Role | Token | Use |
|---|---:|---|
| Primary brand/action | `#F0B31C` | Main CTA fills, highlighted title words, timeline markers, small rules, badges, icon accents |
| Primary structural | `#000000` | Hero, footer, dark half-panel, inner cards, high-contrast text |
| Secondary brand | `#C8920A` | Darker gold borders, small metadata text, pressed states |
| Secondary surface | `#FEF6DD` | Schedule and preparation backgrounds, icon tiles, warm halos |
| Editorial surface | `#FAFAF7` | Neutral section background and breathing space |
| Clean surface | `#FFFFFF` | City gallery, FAQ, cards, icon plates |
| Muted text | `#5A5A5A` | Body copy and secondary explanations on light surfaces |
| Divider | `#E8E5DB` | Thin rules, accordion separators, quiet card boundaries |

### 4.3 Usage balance

- Black carries the product-reveal drama and anchors the page.
- Gold is the unmistakable call-to-action color; use it sparingly enough that every gold control feels important.
- White and warm paper occupy most long-reading sections.
- Cream is a functional background, not decoration; reserve it for schedules, logistics, and preparation.
- Category accent colors appear only as small chips or labels. They must not compete with the primary gold.

### 4.4 Contrast rules

- Use white text on black and black text on gold.
- Body copy on black may use white at roughly `55–80%` visual opacity, but headings and CTA labels remain full white.
- Body copy on white/cream uses `#5A5A5A`; headings use pure black.
- Do not place gold body text on cream. Use deep gold only for small metadata.

## 5. Typography

### 5.1 Font stacks observed

```css
--font-sans: "vivo Sans", "Inter", system-ui, -apple-system, sans-serif;
--font-condensed: "vivo Sans Comp", "vivo Sans", "Barlow Condensed", sans-serif;
--font-display: "vivo Sans Comp", "vivo Sans", "Anton", sans-serif;
--font-mono: "JetBrains Mono", ui-monospace, monospace;
```

Web font families available on the source include:

- Barlow Condensed: `400, 600, 700, 800, 900` plus `700 italic`.
- Inter: `400, 500, 600, 700`.
- Anton: display fallback.
- JetBrains Mono: `400, 500, 700`.
- Fraunces and Inter Tight are loaded by the source but are not materially present in the inspected page. Do not introduce them unless the new concept explicitly needs them.

If proprietary `vivo Sans` fonts are unavailable, use:

- `Barlow Condensed` for headings, buttons, navigation, and labels.
- `Inter` for paragraphs.
- `JetBrains Mono` for time, index, status, and technical metadata.

### 5.2 Type hierarchy

| Element | Desktop | Mobile | Weight | Line height | Tracking | Treatment |
|---|---:|---:|---:|---:|---:|---|
| Hero H1 | `76.8px` | `48px` | `800` | `0.9` (`69.12/43.2px`) | `0.01em` | Condensed, uppercase, 2 lines |
| Main section H2 | `46.08px` | `36px` target | `800` | `0.95` | `0.01em` | Condensed, uppercase |
| Hero subheading | `24px` | `22–24px` | `800` | `32px` | `0.01em` | Condensed, uppercase |
| Card H3 | `24–30px` | `24px` | `800` | `1.0–1.15` | `0.01em` | Condensed, uppercase |
| Small card H4 | `16–20px` | `16px` | `700–800` | `1.15–1.3` | `0.01em` | Usually uppercase |
| Body | `16px` | `15–16px` | `400` | `24px` | normal | Sentence case |
| Small body | `13–14px` | `13px` | `400` | `19.5–21px` | normal | Sentence case |
| CTA label | `15px` | `15px` | `700` | `22.5px` | `0.9px` | Condensed uppercase |
| Header CTA | `14px` | `14px` | `700` | `20px` | `1.4px` | Condensed uppercase |
| Eyebrow/overline | `10–12px` | `10–12px` | `600–700` | `15–18px` | `0.12–0.18em` | Mono/condensed uppercase |
| Time/index/status | `9–12px` | `9–12px` | `500–700` | `1.25–1.5` | `0.08–0.16em` | Mono uppercase |

### 5.3 Typography rules

- Headings are short, declarative, and usually end with a period.
- Use compressed uppercase type to create vertical poster-like blocks.
- Highlight only one phrase in the hero H1 with gold.
- Keep body copy in a normal-width sans-serif; never set paragraphs in the condensed display face.
- Long text columns should remain between `448px` and `576px`.
- Use mono text as a functional accent, not as a novelty font.
- Do not center all headings. Center only the page's explanatory bridge section; keep most sections left-aligned.

## 6. Spacing, containers, and grid

### 6.1 Base rhythm

Use a `4px` spacing unit. Preferred values:

```text
4, 8, 12, 16, 20, 24, 28, 32, 40, 48, 64, 80, 96, 112px
```

Observed common gaps are `8, 10, 12, 16, 20, 24, 28, 32px`.

### 6.2 Containers

- Full-bleed backgrounds span the viewport.
- Primary wide container: `max-width: 1200px`.
- Editorial inner container: `max-width: 1120px`.
- Larger atmospheric/hero canvas may reach `1280–1440px`.
- Desktop side inset is approximately `40px` for wide visual grids and `76px` for editorial headings inside a 1272px document.
- Mobile horizontal padding is `24px`.
- Keep dense explanatory copy to `448–576px`; do not let it span the whole container.

### 6.3 Section rhythm

- Desktop vertical padding: `112px` on major editorial sections.
- Mobile vertical padding: `80px`.
- Use `64–80px` between a section header and major content when the page needs an editorial pause.
- Use `32–40px` between a section header and a card grid.
- Use `12–16px` between sibling cards.

### 6.4 Responsive breakpoints

The inspected implementation follows Tailwind-like breakpoints:

```text
base:  < 640px
sm:    ≥ 640px
lg:    ≥ 1024px
```

Use fluid interpolation between breakpoints where practical, but preserve the observed structural changes.

## 7. Shape language

### 7.1 Radii

```css
--radius-small: 6px;
--radius-medium: 8px;
--radius-large: 12px;
--radius-card: 16px;
--radius-panel: 24px;
--radius-feature-panel: 28px;
--radius-pill: 9999px;
```

- Most cards use `16px`.
- Icon plates use `12px` or `16px`.
- Large gold participation panels use `24–28px`.
- CTAs, chips, timeline dots, and status badges are fully pill-shaped.
- City imagery is clipped inside rounded cards; do not round the image independently from its card.

### 7.2 Lines and markers

- Dividers are thin: `1px` in `#E8E5DB`, black at `10–20%`, or white at `10–25%`.
- Use short gold rules before eyebrow labels and below compact headings.
- Arrow icons are small, simple, and inline with CTA labels.
- Timeline nodes are `24px` black circles with a `4px` cream ring.

### 7.3 Decorative shapes

- Hero drama comes from the product render and a diagonal illuminated beam, not generic vector blobs.
- On dark panels, use one restrained gold atmospheric glow: approximately `520 × 420px`, `12%` gold, `130px` blur.
- Step cards may include a giant `144px` ghost numeral at the bottom-right at roughly `4%` white opacity.
- Edge fades on the horizontal schedule use cream-to-transparent gradients, `32px` wide on mobile and `48px` at small/desktop sizes.
- Decorative elements must stay behind content and never reduce readability.

## 8. Elevation and borders

This design is mostly flat. Hierarchy comes from color and composition.

- Default card shadow: `0 1px 3px rgb(0 0 0 / 0.10), 0 1px 2px -1px rgb(0 0 0 / 0.10)`.
- Gold CTA glow: `0 10px 30px -10px rgb(240 179 28 / 0.80)`.
- Dark CTA shadow on gold: `0 10px 30px -8px rgb(0 0 0 / 0.55)`.
- Prefer one-pixel rings for icon plates and metadata cards.
- Never stack large soft shadows on every component.

## 9. Imagery and alignment

### 9.1 Hero image

- Source visual type: wide product hero, approximately `16:9` (`1280 × 720` in the audited asset).
- Rendering: full-bleed `object-fit: cover`, centered.
- Desktop composition: phone hardware occupies the upper-right and lower-right; a bright diagonal gold beam creates the letterform/energy stroke; text occupies the left safe zone.
- Apply a strong left-to-right black gradient so the heading and body remain readable.
- Apply a subtle bottom black gradient to merge the image into hero metrics.
- Do not place important image detail behind the left text column.
- Mobile: maintain the product on the right; crop aggressively rather than shrinking the whole image. The text remains left-aligned and sits over a nearly black field.

### 9.2 City/editorial cards

- Use portrait architectural photography with a source ratio near `4:5`.
- Desktop observed render: about `289 × 385px`, four cards in one row with `12px` gaps.
- Mobile observed render: two columns of approximately `161px` with a `12px` gap.
- Use `object-fit: cover` and `object-position: 50% 0%` to protect landmarks.
- Add a black gradient from transparent to opaque at the bottom.
- Put date/status chips at the top and large condensed city names at the bottom.
- Category chips may use orange, violet, gold, and blue, but card text remains white.

### 9.3 Product cutout

- Use a transparent or black-background product teaser centered within the dark half-panel.
- Audited display: approximately `229 × 256px` at desktop; `object-fit: contain`.
- Give the product generous negative space. Do not box it in a white card.

### 9.4 Icons

- Use simple line/flat icons with one gold accent.
- Place icons on white `44–48px` square tiles with `12–16px` radius.
- Small theme chips use `20px` icons; preparation rows use `36px`; hero metrics use `44px`; feature rows use `48px`.
- Keep stroke weight and illustration style consistent across the page.

### 9.5 Logos

- Header logo is compact and left-aligned.
- Partner mark sits toward the right on desktop, immediately before the register button.
- On mobile, hide the central navigation and partner mark if space is limited; keep only the primary logo and register CTA.

## 10. Component specifications

### 10.1 Primary CTA

```css
.cta-primary {
  min-height: 52px;
  padding-inline: 28px;
  border: 0;
  border-radius: 9999px;
  background: #f0b31c;
  color: #000;
  font-family: var(--font-condensed);
  font-size: 15px;
  font-weight: 700;
  line-height: 22.5px;
  letter-spacing: 0.9px;
  text-transform: uppercase;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  box-shadow: 0 10px 30px -10px rgb(240 179 28 / 0.8);
}
```

- Header variant: `44px` high with `24px` horizontal padding and `14px` label.
- Dark variant: black background, white text, black shadow.
- Outline variant on dark: transparent background with `1px solid rgb(255 255 255 / 0.25)`.
- Outline variant on light: transparent background with `1px solid rgb(0 0 0 / 0.25)`.
- Keep an arrow after the label; shift it a few pixels on hover.

### 10.2 Eyebrow label

- One short gold line followed by uppercase mono/condensed text.
- `10–12px`, `600–700`, `0.12–0.18em` letter spacing.
- Gold on light backgrounds; white or muted white on black.
- Keep it visually separate from the H2 by `16–20px`.

### 10.3 Feature row

- Horizontal flex row, icon tile first, copy second.
- `16px` gap; vertically align at the top.
- Title: condensed uppercase, `14–16px`, `700–800`.
- Copy: `13–14px` with relaxed line height.
- Avoid extra borders; spacing separates rows.

### 10.4 White utility card

- `16px` radius, white fill, subtle shadow or one-pixel warm ring.
- Padding: `16–24px` depending on density.
- Use on gold or cream surfaces.
- Titles remain black; body copy remains muted.

### 10.5 Dark step card

- `16px` radius, black fill, white text, `24px` padding.
- Optional giant ghost number in the bottom-right.
- Top row combines a white icon tile, a two-digit index, and a compact metadata tag.
- Keep all cards the same visual family even if copy length varies.

### 10.6 City card

- Portrait media card with `16px` radius and `overflow: hidden`.
- Full-card image; no separate caption block.
- Top chips float over the image.
- Bottom gradient supports large city name and date.
- Hover may scale the image slightly while keeping the card bounds fixed.

### 10.7 FAQ row

- Full-width accordion with no card box.
- Minimum row height observed: `84px` on desktop.
- Padding: `24px 16px`.
- Thin horizontal divider between rows.
- Two-digit mono index at left, condensed question in the middle, circular gold plus/minus control at right.
- First item may be open by default.
- Animate height and icon rotation gently; preserve `aria-expanded` and labelled regions.

### 10.8 Horizontal schedule item

- Scrollable on both desktop and mobile; do not force every item to fit.
- Each event item is approximately `210px` wide and centered on the timeline.
- Continuous `2px` low-opacity line runs behind markers.
- Group separators use black `24px` dots with cream rings.
- Event cards are small white rounded rectangles below their times.
- Edge fade masks communicate horizontal overflow.
- Show a small “Scroll the timeline” hint on narrow screens.

## 11. Page architecture

Build sections in this order unless the new information architecture requires a deliberate change.

### 11.1 Header

- Height approximately `96px` on desktop.
- Transparent over the black hero; no separate white bar.
- Left: primary logo.
- Center: compact uppercase navigation.
- Right: partner/powered-by mark, then gold register CTA.
- Desktop navigation is visually quiet and widely spaced.
- Mobile: logo left, gold CTA right, hide the center nav.

### 11.2 Cinematic hero

- Full-bleed dark image extending behind the header.
- Minimum visual height around `840px` at the audited desktop width, inclusive of the header/image canvas.
- Content starts about `40px` from the left on desktop and `24px` on mobile.
- Eyebrow → two-line H1 → subheading → short gold rule → paragraph → CTA row → metric strip.
- Desktop H1 copy width approximately `672px`; paragraph/CTA block approximately `448–576px`.
- CTA row contains one gold primary and one white outline secondary.
- Metrics sit behind a top rule and use four columns on desktop, two columns on mobile.

### 11.3 City gallery

- White background.
- Desktop padding `112px 0`; mobile `80px 0`.
- Header uses a two-column editorial split: title left, explanatory copy and dark CTA right.
- Four portrait cards on desktop; two columns on mobile.
- Use tight `12px` gaps so the cards read as a sequence.

### 11.4 Editorial bridge

- Warm paper background.
- Centered eyebrow, heading, and a narrow explanatory paragraph.
- Its purpose is to reset the rhythm before the dense split program section.
- Use noticeably more whitespace than a normal marketing section.

### 11.5 Split program section

- Desktop: two equal-width vertical panels.
- Left panel: black, white copy, product reveal story, product render, gold CTA.
- Right panel: saturated gold, black copy, workshop syllabus, white topic tiles, black action cards, dark CTA.
- Panels meet edge-to-edge with no gutter.
- Maintain matching top padding and aligned section headings.
- Mobile: stack black panel first, gold panel second.
- Use the gold blurred halo in the black panel and compact icon tiles in both halves.

### 11.6 Participation panel

- Paper background containing one large gold rounded panel.
- Panel radius `24–28px`; generous inner padding.
- Heading and intro at top-left.
- Three dark step cards in a row on desktop and one column on mobile.
- Black pill CTA sits below the cards and aligns to the left.

### 11.7 Run of show

- Cream background.
- Header uses an asymmetric two-column layout: roughly `1.15fr / 0.85fr` on large screens.
- Timeline is intentionally wider than the viewport and horizontally scrollable.
- Use group labels and key-event chips to break a long sequence into meaningful phases.

### 11.8 What to bring / what we provide

- Same cream section family as the schedule.
- Split heading and explanation at top.
- Two white cards below: “you bring” and “we provide.”
- Each card contains three feature rows with illustrated icon tiles.
- Desktop: two columns. Mobile: stack.

### 11.9 FAQ

- White background and strong left-aligned title.
- Support/contact copy aligns to the right of the title at desktop.
- Accordion runs almost the full inner width with separators instead of card boxes.
- Open answer text is indented to align with the question label, not the index.

### 11.10 Closing CTA and footer

- Return to pure black for a decisive ending.
- Center a small eyebrow, a large “See it first.”-style line with one gold word, a short paragraph, and a gold CTA.
- Footer below uses a thin white/low-opacity divider.
- Logo left; navigation and legal links spread across the remaining width.
- Keep footer typography small, condensed, and low-contrast.

## 12. Alignment rules

- Alternate alignment deliberately: left-aligned hero, split editorial header, centered bridge, two-column program, left-aligned cards, centered closing CTA.
- Align the first text baseline of each two-column section.
- In split panels, align matching eyebrows, headings, and CTAs even when internal content differs.
- Keep icons in a strict vertical column within repeated feature lists.
- Center timeline content on its nodes; do not left-align each timeline card to its node.
- Use equal-height city cards and equal-width schedule items.
- Do not distribute body copy across wide empty space. Narrow text measures are essential to the editorial quality.

## 13. Responsive behavior

### 13.1 Mobile findings at 390px

- Center navigation is hidden.
- Header retains logo and register CTA.
- Hero H1 computes to `48px / 43.2px` with `0.48px` tracking.
- Main mobile content width is approximately `334px` inside `24px` side padding.
- Major sections use `80px` vertical padding.
- Hero metric grid is two columns.
- City gallery is two columns (`~161px + 12px gap + ~161px`), not a single list.
- Split program panels stack vertically.
- Syllabus and build-step grids become one column below `640px`.
- Timeline remains horizontally scrollable with fixed-width items.
- Participation cards stack one per row.
- CTA pairs stack when they cannot fit; preserve at least `12px` gap.

### 13.2 Tablet

- Use two-column internal grids from approximately `640px` where copy remains readable.
- Keep the main split program stacked until `1024px`; it needs enough width for each half to breathe.
- City cards may remain two columns until the full four-column layout has at least `~280px` per card.

### 13.3 Desktop

- At `≥1024px`, restore the two equal program panels.
- Use four city cards.
- Use three participation steps.
- Use two preparation cards.
- Use editorial header splits and show full navigation.

### 13.4 Overflow protection

- Never allow the page itself to scroll horizontally.
- Only the schedule/timeline track should overflow horizontally.
- Long CTA labels may wrap only as a last resort; prefer full-width mobile buttons.
- Preserve image focal points with explicit `object-position` rules.

## 14. Motion and interaction

Observed transition families:

- `150ms` for color, border, fill, and stroke transitions.
- `200ms` for button/card background, color, shadow, and small transforms.
- `300ms` for larger transform transitions.
- `600ms` ease-out for entrance transforms.

Recommended behavior:

- Fade-up repeated cards by `16–20px` as they enter the viewport.
- Stagger siblings by `50–90ms`; never delay core content excessively.
- CTA hover: slightly deepen the fill, strengthen the shadow, and translate the arrow `2–4px`.
- City hover: scale only the image to about `1.03`; keep card bounds fixed.
- Dark/white cards: lift no more than `2px`.
- FAQ: rotate or swap plus/minus icon and animate content height/opacity.
- Timeline: native horizontal scrolling with visible fade affordances; support mouse wheel/trackpad/touch.
- Respect `prefers-reduced-motion`; remove entrance translation and keep instant/short opacity changes.

## 15. Accessibility and usability

- Keep all primary controls at least `44px` high; standard CTA is `52px`.
- Maintain WCAG AA contrast for body copy.
- Use semantic `header`, `nav`, `main`, `section`, `dl`, `ol`, `button`, and `footer` elements.
- Every decorative icon should have an empty alt or `aria-hidden="true"`.
- Every meaningful image needs descriptive alt text.
- The hero background must have a CSS overlay; never rely on the source image being dark enough.
- Accordion controls require `aria-expanded`, `aria-controls`, labelled regions, and keyboard support.
- Horizontal schedule must remain keyboard and touch scrollable.
- Provide visible focus rings in gold/white depending on background.
- Do not communicate city/category/status with color alone; include text labels.
- Do not reduce body text below `13px`.

## 16. Content style

- Use short, forceful headings: “First look. Then build.”
- Use two-part rhythm: reveal → action, learn → ship, bring → provide.
- Eyebrows establish context; H2 communicates the promise; body copy explains details.
- Write CTA labels as verbs: “Build at…”, “Register…”, “See how…”.
- Use precise event metadata: date, time, status, phase, eligibility.
- Avoid buzzword-heavy generic copy. The design works because information is concrete.

## 17. Copy-ready master prompt

Copy the block below into a design or coding task. Replace bracketed fields only. Attach this file and the visual reference when possible.

```text
Design and implement [PAGE/PRODUCT NAME], a responsive [PAGE TYPE], using the attached TechQuest × iQOO design blueprint as the visual authority.

GOAL
Create an original page for [AUDIENCE] that communicates [PRIMARY OUTCOME]. Do not copy iQOO or Reskilll brand assets, names, or copy. Translate the blueprint's visual grammar to [NEW BRAND/PRODUCT].

VISUAL DIRECTION
- Premium industrial technology-launch aesthetic.
- Cinematic black hero with a high-contrast product/subject image weighted to the right and readable left-side content.
- Gold (#F0B31C) is the primary action/highlight color; black is the structural anchor; warm cream (#FEF6DD), paper (#FAFAF7), and white are reading surfaces.
- Strong compressed uppercase display type, neutral sans-serif body text, mono metadata.
- Alternate black, white, saturated gold, and warm cream sections to create rhythm.
- Flat, precise components with 16px card radii, 24–28px feature-panel radii, pill CTAs, thin rules, restrained shadows, and small illustrated icon tiles.

TYPOGRAPHY
- Display: Barlow Condensed or a licensed brand-condensed face; 800 weight, uppercase, tight line-height.
- Body: Inter; 400–600.
- Metadata: JetBrains Mono; 500–700.
- Hero H1: clamp(48px, 6vw, 76.8px), line-height .9, letter-spacing .01em.
- Section H2: clamp(36px, 4vw, 46.08px), line-height .95.
- Body: 16/24px; small copy 13–14/19.5–21px; CTA 15/22.5px, 700, .9px tracking.

LAYOUT
- Full-bleed section backgrounds with 1200px wide and 1120px editorial containers.
- Desktop major-section padding 112px; mobile 80px.
- Desktop side inset ~40px for visual grids and ~76px for editorial content; mobile side padding 24px.
- Keep paragraphs 448–576px wide.
- Breakpoints: base, 640px, 1024px.

PAGE STRUCTURE
1. Transparent header over hero: logo, navigation, partner/context mark, gold CTA. Hide central nav on mobile.
2. Cinematic hero: eyebrow, two-line H1 with one gold phrase, subheading, gold rule, concise paragraph, primary + outline CTAs, four metric items.
3. [PRIMARY GALLERY/LOCATIONS/PRODUCTS]: editorial split header and four portrait cards desktop / two columns mobile.
4. Centered editorial bridge with generous paper-colored whitespace.
5. Edge-to-edge dual program/value section: black reveal/story panel and gold workshop/action panel. Stack on mobile.
6. Large gold participation/process panel with three black numbered step cards.
7. Cream schedule/process section with a horizontally scrollable timeline.
8. Cream two-card preparation/resources comparison.
9. White FAQ accordion with full-width divider rows.
10. Centered black closing CTA and compact dark footer.

COMPONENT RULES
- Primary CTA: 52px high, 28px inline padding, pill radius, gold fill, black label, small arrow, restrained gold shadow.
- Cards: 16px radius; white cards use subtle 1–3px shadow; black cards use no heavy shadow.
- Icon tiles: 44–48px squares, 12–16px radius, white or cream fill.
- Use short gold rules, two-digit indices, status chips, and small mono labels as repeatable motifs.
- Use a single soft gold halo on dark sections and large ghost numerals at 4% opacity in step cards.

IMAGERY
- Hero image is full bleed and cover-cropped; preserve a left text safe zone with a black gradient overlay.
- Portrait gallery images use object-fit cover and top-center focal alignment.
- Product/cutout images use object-fit contain and generous negative space.
- Never use unlicensed iQOO/Reskilll imagery; create or source original assets for [NEW BRAND].

MOTION
- 150ms color transitions; 200ms component hover; 300ms transforms; 600ms ease-out fade-up entrances.
- Stagger repeated items 50–90ms.
- Keep movement subtle and support prefers-reduced-motion.

RESPONSIVE
- Mobile H1 48/43.2px, 24px side padding, 80px section padding.
- Two-column compact gallery on mobile when each card can remain at least ~155px wide.
- Stack the black/gold split panels and process cards below desktop.
- Keep the timeline horizontally scrollable with fixed ~210px event items and edge fade masks.
- Prevent page-level horizontal overflow.

ACCESSIBILITY
- Semantic landmarks and heading order.
- 44px minimum touch targets.
- AA color contrast, visible focus states, useful alt text.
- Fully accessible accordion and keyboard/touch scroll behavior.
- Do not use color as the only status signal.

CONTENT TO USE
[PASTE THE NEW PAGE COPY, SECTIONS, DATA, CTA TARGETS, AND ASSET LIST HERE]

DELIVERABLE
Produce a polished, production-ready implementation. Preserve the blueprint's visual hierarchy and composition, but make the result unmistakably original to [NEW BRAND]. Verify desktop, tablet, and 390px mobile layouts and report any intentional deviations.
```

## 18. Implementation tokens

```json
{
  "colors": {
    "ink": "#000000",
    "inkSoft": "#1A1A1A",
    "inkMuted": "#5A5A5A",
    "cinematicBlack": "#0B0B0F",
    "primary": "#F0B31C",
    "primaryDeep": "#C8920A",
    "primarySoft": "#FEF6DD",
    "paper": "#FAFAF7",
    "paperDeep": "#F2F2EC",
    "line": "#E8E5DB",
    "white": "#FFFFFF"
  },
  "fonts": {
    "display": "Barlow Condensed, sans-serif",
    "body": "Inter, system-ui, sans-serif",
    "mono": "JetBrains Mono, monospace"
  },
  "radii": {
    "icon": 12,
    "card": 16,
    "panel": 24,
    "featurePanel": 28,
    "pill": 9999
  },
  "containers": {
    "wide": 1200,
    "editorial": 1120,
    "copyMin": 448,
    "copyMax": 576
  },
  "sectionPadding": {
    "mobile": 80,
    "desktop": 112
  },
  "breakpoints": {
    "sm": 640,
    "lg": 1024
  },
  "motionMs": {
    "color": 150,
    "component": 200,
    "transform": 300,
    "entrance": 600
  }
}
```

## 19. Build and QA checklist

### Visual

- [ ] Hero reads clearly over the image at desktop and mobile.
- [ ] Only the most important phrase and CTAs use primary gold.
- [ ] Display headings are condensed, uppercase, and tightly led.
- [ ] Paragraphs stay within the 448–576px measure on desktop.
- [ ] Black, white, gold, and cream sections alternate with intentional rhythm.
- [ ] Cards use the correct 16px radius; large panels use 24–28px.
- [ ] Shadows are restrained.
- [ ] Images have correct focal points and do not stretch.
- [ ] Repeated icon tiles align to a strict column.
- [ ] Timeline nodes and cards align to one continuous line.

### Responsive

- [ ] Header navigation hides cleanly on mobile.
- [ ] Mobile hero H1 is approximately 48px with .9 line-height.
- [ ] Compact gallery retains two readable columns at 390px.
- [ ] Split black/gold panels stack below desktop.
- [ ] Timeline is the only intended horizontal overflow region.
- [ ] All CTA labels fit or become full-width without awkward wrapping.
- [ ] No page-level horizontal scrollbar appears.

### Interaction

- [ ] Hover and focus states are visible on every control.
- [ ] Entrance animations are subtle and do not hide content if JavaScript fails.
- [ ] Reduced-motion preferences are respected.
- [ ] Accordion works with mouse, touch, and keyboard.
- [ ] Schedule works with trackpad, mouse wheel, keyboard, and touch.

### Accessibility

- [ ] Heading hierarchy is logical.
- [ ] Touch targets are at least 44px.
- [ ] Contrast passes WCAG AA.
- [ ] Meaningful images have useful alt text.
- [ ] Decorative graphics are hidden from assistive technology.
- [ ] Status is conveyed in text as well as color.
- [ ] Focus rings remain visible on black, gold, white, and cream surfaces.

## 20. Fidelity priorities

If time is limited, preserve these aspects in order:

1. Color-role contrast and section alternation.
2. Condensed uppercase typographic hierarchy.
3. Hero image composition with a protected left text zone.
4. Section spacing and narrow paragraph measures.
5. Split black/gold program panels.
6. Pill CTAs and 16px modular cards.
7. Portrait media cards and horizontal schedule.
8. Micro-details: mono labels, arrows, rings, ghost numerals, and entrance motion.

The design will still feel correct with new content and original imagery if these priorities remain intact.
