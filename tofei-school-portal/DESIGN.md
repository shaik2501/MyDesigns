# ToFEI School Portal — Design Blueprint and Reusable Build Prompt

## Core public page gallery

The `pages/` folder preserves `home.png` for the public landing experience and `login.png` for the school/official authentication entry screen. Private dashboards and provisioned-account content are intentionally excluded.

> Use this file as the visual authority for future public-service, education, compliance, evidence-submission, or government programme websites inspired by this design language. Preserve its accessibility-first hierarchy, institutional green palette, multilingual typography, evidence-card layout, and responsive behavior while replacing source branding, programme copy, and protected assets with original project material.

## 1. Reference and audit scope

- Source audited: <https://tofei.wedevit.in/>
- Live title: `ToFEI - Tobacco Free Educational Institutions, Andhra Pradesh`
- Audit date: 2 September 2026
- Desktop audit viewport: `1280 × 720 CSS px`, DPR `2`
- Desktop document: approximately `1272 × 2846 CSS px`
- Mobile audit viewport: `390 × 844 CSS px`
- Mobile document: approximately `382 × 5075 CSS px`
- Full-page screenshot: [`tofei-full-page.png`](tofei-full-page.png)

The reference screenshot was captured directly from the live page after scroll-triggered sections had settled. It is a faithful visual reference, not a license to reuse government marks, photography, or copy.

## 2. One-sentence design direction

Build a calm, accessibility-first government service page that combines official institutional credibility with a warm school-community tone, evidence-led cards, clear green actions, and multilingual usability.

## 3. Design personality

The design should feel:

- Official without feeling bureaucratic.
- Accessible and readable before decorative.
- Calm, healthy, optimistic, and accountable.
- Designed for school heads and programme officers, not marketers.
- Evidence-oriented: each task has a number, photo, description, and completion signal.
- Locally relevant through multilingual controls and familiar school photography.

Avoid:

- Corporate SaaS gradients.
- Dark mode as the default.
- Glassmorphism.
- Decorative animations that delay information.
- Tiny administrative interfaces.
- Overly rounded playful cards.
- Neon green or high-saturation health branding.
- Dense tables on the public landing page.

## 4. Color system

### 4.1 Core tokens

```css
:root {
  /* Text and structure */
  --tofei-ink: #10261c;
  --tofei-ink-green: #164c31;
  --tofei-muted: #667b6d;
  --tofei-muted-deep: #496556;

  /* Programme green */
  --tofei-primary: #0b6b3a;
  --tofei-primary-hover: #075b31;
  --tofei-primary-bright: #0b7a42;
  --tofei-check-green: #138808;

  /* Surfaces */
  --tofei-white: #ffffff;
  --tofei-off-white: #fbfdfb;
  --tofei-section: #f7faf8;
  --tofei-soft: #e8f3eb;
  --tofei-soft-wash: #eef7ef;
  --tofei-line: #dfe9e2;
  --tofei-neutral: #f8f9fa;

  /* Government identity accent */
  --tofei-saffron: #ff9933;
  --tofei-saffron-deep: #e17b2a;
}
```

### 4.2 Color roles

| Role | Value | Use |
|---|---:|---|
| Primary action | `#0B6B3A` | Buttons, links, numbers, check icons, emphasized headline words |
| Primary text | `#10261C` | H1/H2, official labels, body text requiring maximum contrast |
| Secondary green text | `#164C31` | Card headings and supporting institutional copy |
| Muted copy | `#667B6D` | Descriptions, metadata, captions, footer copy |
| Activity surface | `#F7FAF8` | Nine-activity section background |
| Soft green surface | `#E8F3EB` | Stat icons, CTA callout, step icon tiles, number circles |
| Line | `#DFE9E2` | Card borders, column separators, footer/section rules |
| Saffron accent | `#FF9933` | Top identity stripe, short eyebrow rule, step numbering |

### 4.3 Government identity stripe

- Use a very thin top border or stripe with saffron at the left, white/neutral in the middle, and green at the right.
- It should read as an Indian government identity cue without dominating the interface.
- Keep it approximately `4–6px` high.
- Do not use saffron as a general CTA color; actions remain green.

### 4.4 Contrast discipline

- White text on `#0B6B3A` for primary buttons.
- `#10261C` on white/off-white for headings.
- Muted green-gray copy must remain dark enough for AA contrast.
- Use pale green only as a surface; do not put pale green text on white.
- Completed/check signals use a green outline plus a recognizable check icon.

## 5. Typography

### 5.1 Loaded type families

```css
--font-primary: "Noto Sans", system-ui, sans-serif;
--font-devanagari: "Noto Sans Devanagari", "Noto Sans", sans-serif;
--font-telugu: "Noto Sans Telugu", "Noto Sans", sans-serif;
--font-mono: "JetBrains Mono", ui-monospace, monospace;
```

Observed web-font weights:

- Noto Sans: `400, 500, 600, 700, 800`.
- Noto Sans Devanagari: `400, 500, 600, 700`.
- Noto Sans Telugu: `400, 500, 600, 700, 900`.
- JetBrains Mono: `400, 700`.

Use script-specific Noto Sans variants for translations so Telugu and Devanagari text maintain compatible density and line height.

### 5.2 Typographic character

Unlike campaign landing pages, the main headings use regular weight rather than ExtraBold. Scale, whitespace, and color establish importance.

- H1/H2: Noto Sans `400`.
- Buttons: `800–900`.
- Eyebrows and compact official labels: `700–900` with wide tracking.
- Card titles: `400–500`.
- Body: `400`.
- Key stats: `800–900`.

### 5.3 Desktop type scale

| Element | Size | Line height | Weight | Tracking |
|---|---:|---:|---:|---:|
| Hero H1 | `64px` | `65.92px` | `400` | `-3.2px` |
| Section H2 | `38.4px` | `57.6px` | `400` | `-1.152px` |
| Step H3 | `16px` | `24px` | `400` | normal |
| Activity H3 | `14.72px` | `19.136px` | `400` | normal |
| Body | `16px` | `24px` | `400` | normal |
| Small body | `11.5–14px` | `16–20px` | `400` | normal |
| Eyebrow | `10.24–11.2px` | `15–17px` | `700–900` | `0.06–0.12em` |
| CTA label | `16px` | `24px` | `800–900` | normal |

### 5.4 Mobile type scale

- Hero H1: `40px / 41.2px`, tracking `-2px`.
- Main content width around `350px` in a `382px` document.
- Section H2: target `30–34px` with relaxed wrapping.
- Body remains `16/24px`.
- Activity text may use `14–15px`, but never reduce below readable administrative UI size.

### 5.5 Headline treatment

- Use sentence case.
- Highlight one meaningful phrase in programme green.
- Do not make the highlighted phrase bold; color alone creates the emphasis.
- Keep the H1 to three lines on desktop and approximately three lines on mobile.
- The reference phrase is integrated into the sentence rather than isolated as a badge.

### 5.6 Multilingual rules

- Language choices must remain visible in the accessibility bar.
- Match translation line-height to the English layout, but allow natural wrapping.
- Never force fixed-height cards when translated content needs more space.
- Use `lang` attributes and the correct script font.
- Avoid all-caps Telugu or Devanagari styling.

## 6. Layout and spacing

### 6.1 Containers

- Primary maximum width: `1180px`.
- At desktop, the container begins around `46px` inside a `1272px` document.
- Hero copy width: approximately `565px`.
- Hero image width: approximately `511px`.
- Hero column gap: approximately `64px`.
- Centered stat row width: `900px`.
- Mobile inner content: `342–350px` with `16–20px` margins.

### 6.2 Spacing scale

Use a `4px` base unit with these preferred values:

```text
4, 6, 8, 12, 13, 16, 20, 24, 32, 40, 48, 56, 64, 80px
```

Common gaps observed:

- Activity-card internal gap: approximately `12.8px`.
- Activity-grid gap: approximately `13.6px` on mobile.
- Step-card gap: `16px`.
- Hero column gap: `64px`.

### 6.3 Major section padding

Desktop:

- Hero: `80px 20px 64px`.
- Activity section: `80px 20px`.
- Three-step section: `80px 20px`.
- Final callout: `40px` inside the panel.
- Footer: `32px 20px`.

Mobile:

- Hero: `48px 16px 40px`.
- Activity section: `56px 20px`.
- Three-step section: `80px 20px`.
- Final callout: `24px`.

### 6.4 Grid behavior

- Hero: two columns desktop, one column mobile.
- Activity grid: `3 × 3` desktop, one column mobile.
- Steps: three columns desktop, one column mobile.
- Stats: always three compact columns; mobile columns are approximately `100px` each.
- Footer: three aligned regions desktop, stacked/wrapped mobile.

### 6.5 Breakpoints

Use practical breakpoints around:

```text
base: < 640px
tablet: 640–959px
desktop: ≥ 960px
```

Prefer content-driven collapse: switch the activity grid to one column before cards become too narrow for a thumbnail and readable description.

## 7. Shape language

### 7.1 Radii

```css
--radius-button: 8px;
--radius-card-small: 7.2px;
--radius-card: 11.2px;
--radius-panel: 12.8px;
--radius-hero-image: 16px;
--radius-pill: 999px;
--radius-circle: 50%;
```

- Buttons are rounded rectangles, not pills.
- Activity and step cards use restrained `7–12px` radii.
- Hero photo uses `16px`.
- Number and icon chips are circular or near-circular.
- The final callout uses approximately `12–13px` radius.

### 7.2 Borders

- Cards use a quiet `1px` green-gray border near `#DFE9E2`.
- Selected/completed controls may use `#0B6B3A` borders.
- The hero image may use a slightly stronger pale-green edge.
- Column separators in the stat row use thin vertical lines.
- Avoid dark outlines and heavy dividers.

### 7.3 Shadows

Primary button:

```css
box-shadow: 0 8px 18px rgb(11 107 58 / .14);
```

Header sign-in button:

```css
box-shadow: 0 8px 18px rgb(11 107 58 / .18);
```

Hero image/evidence card:

```css
box-shadow: 0 20px 45px rgb(23 59 40 / .14);
```

Quiet cards may use:

```css
box-shadow: 0 10px 25px rgb(23 59 40 / .05);
```

## 8. Top utility and institutional header

### 8.1 Accessibility bar

- Place it at the very top below the thin identity stripe.
- Align content to the right on desktop.
- Include:
  - Accessibility label.
  - Decrease text button `A−`.
  - Normal text button `A` with selected state.
  - Increase text button `A+`.
  - Telugu and English language options.
- Buttons are square-ish with visible border and high-contrast selected state.
- The selected `A` uses a green fill with white text.
- Keep all controls keyboard accessible and expose `aria-pressed` where relevant.

### 8.2 Institutional header

- White background with generous breathing room.
- Government department logo on the left.
- Thin vertical divider.
- Programme identity stack:
  - Government jurisdiction.
  - Strong portal name.
  - Programme subtitle.
- Green sign-in button aligned at the far right.
- Desktop height is approximately `136px` including utility bar/header structure.
- Mobile header becomes tall enough to keep logo, title, and sign-in button readable; it does not collapse into a hamburger because the primary function is sign-in.

## 9. Hero composition

### 9.1 Desktop

- Off-white/very pale green background.
- Two-column grid inside the `1180px` container.
- Left column:
  1. Saffron line plus uppercase green eyebrow.
  2. Large regular-weight H1 with one green phrase.
  3. Concise explanatory paragraph.
  4. Primary portal button and green text link.
  5. Small audience/jurisdiction metadata row with check-circle icon.
- Right column:
  - School-community evidence photograph.
  - Small dark process chip at top: `DO → CAPTURE → REVIEW`.
  - White translucent evidence caption panel across the bottom.

### 9.2 Hero image

- Audited source ratio: `640 × 360`.
- Desktop render: approximately `511 × 430px`.
- Use `object-fit: cover`, centered.
- Clip with `16px` radius.
- Choose authentic school/community photography with a visible programme sign or activity.
- The caption card uses white at roughly `94–95%` opacity.
- Add a small shield/check icon to the caption.

### 9.3 Mobile

- Hero becomes one column.
- Text appears first, image second.
- The portal button becomes full-width.
- “See how it works” moves to a separate line.
- Metadata wraps into two balanced columns if needed.
- Image width approximately `339px`, height `300px` at a `390px` viewport.
- Maintain the process chip and evidence caption within the image.

## 10. Stat row

- Centered white panel floating between hero and activity section.
- Desktop size approximately `900 × 104px`.
- Mobile size approximately `342 × 128px`.
- Three equal columns:
  1. Number of activities.
  2. Number of scorecards.
  3. GPS/location evidence.
- Large green value, very small muted label.
- Separate columns with thin vertical rules.
- `11–13px` panel radius and quiet shadow.

## 11. Nine-activity scorecard section

### 11.1 Section composition

- Pale `#F7FAF8` background.
- Left-aligned uppercase eyebrow.
- Large regular-weight H2.
- Narrow explanatory paragraph.
- `3 × 3` card grid.
- Full-width pale action bar beneath the grid.

### 11.2 Activity card anatomy

Each card contains four visual columns:

1. Circular two-digit number badge.
2. Text block with title and description.
3. Small evidence thumbnail.
4. Outlined completion/status circle.

Desktop titles use approximately `14.72/19.136px`.

Mobile measured card columns:

```text
32px number | ~154px copy | 62px image | 18px status
```

with approximately `12.8px` gaps.

### 11.3 Activity thumbnails

- Desktop render: approximately `68 × 54px`.
- Use `object-fit: cover` for photography.
- Use `object-fit: contain` for notice boards or documents.
- Thumbnails remain documentary, not decorative.
- Keep the same visual crop across cards where possible.

### 11.4 Responsive activity behavior

- Desktop: three equal columns.
- Mobile: one column, approximately `342px` wide.
- Mobile card heights may vary from `150–179px` based on copy length.
- Do not truncate instructions.
- Preserve number, thumbnail, and completion indicator on the first visual row.

### 11.5 Section CTA bar

- Pale green bordered panel below the cards.
- Prompt text left.
- Green button right.
- Stack prompt and button on mobile.
- Use the same button geometry as the hero CTA.

## 12. Three-step process section

- White background.
- Uppercase eyebrow: “Simple for schools” or equivalent.
- H2 communicates a three-step journey.
- Three equal cards desktop, one column mobile.
- Each card includes:
  - Small saffron step number.
  - Pale green icon tile.
  - Green title.
  - Muted explanation.
- Cards use thin borders and minimal shadow.
- Mobile grid measured at `342px` width with `16px` gaps.

## 13. Final callout

- Large pale-green panel inside the main container.
- Desktop render approximately `1180 × 224px`.
- Text block left and green sign-in CTA right.
- Overline at top-left.
- H2 maximum width approximately `690px`.
- Supporting line explains credentials or eligibility.
- Mobile uses a single-column layout and `24px` padding.
- Primary CTA becomes full-width or left-aligned beneath copy.

## 14. Footer

- Very light/off-white background; do not switch to a heavy dark footer.
- Three zones desktop:
  1. System ownership and last-updated date.
  2. Quick links.
  3. Support/contact and powered-by attribution.
- Headings use compact bold text.
- Links are programme green.
- Metadata is small but readable.
- Mobile stacks sections with clear gaps and avoids center-aligning long official ownership text.

## 15. Buttons and links

### 15.1 Primary button

```css
.tofei-button-primary {
  min-height: 50px;
  padding: 12.8px 17.6px;
  border: 0;
  border-radius: 8px;
  background: #0b6b3a;
  color: #fff;
  font-family: "Noto Sans", system-ui, sans-serif;
  font-size: 16px;
  font-weight: 900;
  line-height: 24px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  box-shadow: 0 8px 18px rgb(11 107 58 / .14);
}
```

- Use a right arrow icon.
- Header sign-in variant is approximately `47px` high with `10.4px 16px` padding and `7.2px` radius.
- Mobile hero CTA spans the content width.

### 15.2 Text link

- Programme green.
- Weight `800`.
- No underline by default; add underline/focus indicator on interaction.
- Keep link label direct and action-oriented.

## 16. Iconography

- Use thin outlined icons with rounded joins.
- Core symbols: shield/check, upload/cloud, document/check, location pin, arrow.
- Icon tile: pale green square/circle around `36–44px`.
- Status indicator: small outlined circle with check.
- Avoid colorful mixed icon packs.
- Maintain sufficient contrast at small sizes.

## 17. Motion

Observed motion families:

- `180ms` ease for card transform, shadow, and border.
- `180ms` ease for button transform, background, and shadow.
- `250ms` for larger hover states.
- `700ms` entrance reveal for opacity and vertical transform using `cubic-bezier(.22,1,.36,1)`.

Recommended implementation:

- Reveal sections with a subtle fade-up only after core content is already accessible.
- Do not start important content at `display:none`.
- Card hover: `translateY(-2px)` maximum.
- Button hover: slightly darken green and raise `1px`.
- Arrow shifts `2–3px`.
- Honor `prefers-reduced-motion` by removing entrance translation and shortening transitions.

## 18. Accessibility requirements

- Accessibility controls are a real product feature, not decoration.
- Text-size controls must change the root scale predictably and preserve layout.
- Language switching must update page language metadata and visible copy.
- Every button and link needs a visible keyboard focus state.
- Maintain at least `44px` touch targets.
- Use semantic `header`, `nav`, `main`, `section`, `article`, and `footer` elements.
- H1/H2 hierarchy must be logical.
- Every evidence photo needs descriptive alt text.
- Completion indicators require text/ARIA state, not just a check icon.
- Never rely on green alone to communicate completion.
- Ensure high contrast under increased text-size mode.
- Cards must grow vertically instead of clipping translated content.
- Use `aria-pressed` on text-size mode buttons.
- Provide a skip-to-main-content link.

## 19. Content style

- Use clear administrative language without legalistic complexity.
- Explain the user, action, evidence, and outcome.
- Prefer short verbs: submit, verify, save, track.
- Use numbered activities and steps.
- Keep evidence requirements concrete.
- Identify ownership, programme authority, and last-updated date.
- Keep technical credentials guidance near sign-in CTAs.
- Avoid celebratory marketing claims that do not help programme completion.

## 20. Page architecture

Build in this order:

1. Thin tricolor identity stripe.
2. Accessibility and language utility bar.
3. Government/programme header with sign-in action.
4. Two-column evidence-led hero.
5. Centered three-column programme fact row.
6. Pale nine-activity scorecard section.
7. White three-step process section.
8. Pale-green sign-in callout.
9. Light institutional footer.

## 21. Copy-ready master prompt

```text
Design and implement [PUBLIC SERVICE / EDUCATION PROGRAMME NAME], a responsive evidence-led government or institutional portal landing page, using the attached ToFEI School Portal design blueprint as the visual authority.

Create an original result for [USERS, JURISDICTION, AND PROGRAMME GOAL]. Do not copy ToFEI or Andhra Pradesh government logos, school photography, programme copy, or protected assets. Use authorized or original material.

VISUAL DIRECTION
- Calm, accessible, official, and community-oriented.
- White, off-white, and pale green surfaces with institutional forest-green actions.
- Thin saffron/white/green identity stripe at the top.
- Regular-weight oversized Noto Sans headings rather than heavy marketing typography.
- Authentic evidence photography and clearly numbered task cards.
- Restrained radii, thin borders, quiet green shadows, and no decorative gradients.

COLOR TOKENS
- Ink #10261C
- Secondary ink #164C31
- Primary green #0B6B3A
- Primary hover #075B31
- Muted #667B6D
- Activity surface #F7FAF8
- Soft green #E8F3EB
- Line #DFE9E2
- Saffron #FF9933

TYPOGRAPHY
- English: Noto Sans, weights 400–800.
- Telugu: Noto Sans Telugu.
- Devanagari: Noto Sans Devanagari.
- Technical labels only: JetBrains Mono.
- Desktop H1 64/65.92px, weight 400, tracking -3.2px.
- Mobile H1 40/41.2px, tracking -2px.
- Desktop H2 38.4/57.6px, weight 400.
- Body 16/24px.
- CTA 16/24px, weight 800–900.

LAYOUT
- 1180px maximum container.
- Desktop hero: approximately 565px copy + 64px gap + 511px image.
- Desktop major section padding 80px; mobile 48–56px where appropriate.
- Mobile side padding 16–20px.
- Breakpoints around 640px and 960px.

PAGE STRUCTURE
1. Thin government identity stripe.
2. Accessibility bar with A−, A, A+ and language controls.
3. Institutional header with department logo, programme title, subtitle, and sign-in button.
4. Hero with eyebrow, sentence-case H1 containing one green phrase, explanation, primary CTA, secondary link, user metadata, and an evidence photograph.
5. Centered three-column programme fact row.
6. Pale activity section with eyebrow, H2, introduction, and a numbered evidence-card grid.
7. Pale CTA strip below the activity grid.
8. White three-step process section with icon cards.
9. Pale-green final sign-in callout.
10. Light footer with ownership, updated date, quick links, and support.

COMPONENT RULES
- Primary CTA: 50px high, 8px radius, green fill, white 900-weight label, right arrow, subtle green shadow.
- Header CTA: 47px high and 7.2px radius.
- Activity cards: 7–11px radius, thin #DFE9E2 border, number badge, title, description, evidence thumbnail, and completion state.
- Hero image: 16px radius, authentic documentary photo, overlay process chip, translucent evidence caption.
- Stat row: white, 900px desktop width, three equal columns with thin separators.
- Callout panel: pale green, 12–13px radius.

RESPONSIVE
- Hero and all card grids become one column on mobile.
- Mobile content width approximately 342–350px at 390px viewport.
- Primary hero CTA becomes full-width.
- Evidence image follows the hero copy.
- Activity cards retain number, readable copy, 62px thumbnail, and status icon.
- Stat row retains three compact columns.
- Footer stacks without centering long ownership text.
- No horizontal page overflow.

MOTION
- 180ms hover transitions, 250ms larger states, 700ms subtle reveal.
- Maximum card lift 2px and arrow shift 3px.
- Support reduced motion.

ACCESSIBILITY
- Working text-size controls and language switching.
- Correct script fonts and lang attributes.
- Semantic structure, visible focus states, 44px controls, useful alt text.
- Completion state communicated through text/ARIA as well as color.
- Cards grow naturally under increased text size and translations.
- WCAG AA contrast minimum.

CONTENT AND FUNCTIONAL REQUIREMENTS
[PASTE PROGRAMME OWNER, USERS, ACTIVITIES, EVIDENCE RULES, LOGIN METHOD, LANGUAGES, CTA TARGETS, SUPPORT DETAILS, AND ASSET LIST]

Deliver a production-ready implementation. Verify desktop, tablet, 390px mobile, keyboard navigation, text enlargement, and each supported language. Report intentional deviations from this blueprint.
```

## 22. Implementation tokens

```json
{
  "colors": {
    "ink": "#10261C",
    "inkGreen": "#164C31",
    "primary": "#0B6B3A",
    "primaryHover": "#075B31",
    "muted": "#667B6D",
    "white": "#FFFFFF",
    "offWhite": "#FBFDFB",
    "section": "#F7FAF8",
    "soft": "#E8F3EB",
    "line": "#DFE9E2",
    "saffron": "#FF9933"
  },
  "fonts": {
    "primary": "Noto Sans, system-ui, sans-serif",
    "telugu": "Noto Sans Telugu, Noto Sans, sans-serif",
    "devanagari": "Noto Sans Devanagari, Noto Sans, sans-serif",
    "mono": "JetBrains Mono, ui-monospace, monospace"
  },
  "radii": {
    "button": 8,
    "smallCard": 7.2,
    "card": 11.2,
    "panel": 12.8,
    "heroImage": 16
  },
  "containers": {
    "main": 1180,
    "stat": 900,
    "mobileInset": 20
  },
  "breakpoints": {
    "sm": 640,
    "desktop": 960
  },
  "motionMs": {
    "hover": 180,
    "largeState": 250,
    "reveal": 700
  }
}
```

## 23. QA checklist

### Visual

- [ ] Tricolor identity stripe remains thin and restrained.
- [ ] Green, off-white, and pale-green roles are consistent.
- [ ] Noto Sans families render correctly for every language.
- [ ] H1/H2 use regular weight and large scale.
- [ ] Only one meaningful H1 phrase is green.
- [ ] Hero uses authentic evidence photography.
- [ ] Activity cards contain number, copy, thumbnail, and status.
- [ ] Shadows remain subtle and green-tinted.
- [ ] Buttons are rounded rectangles, not oversized pills.

### Responsive

- [ ] Desktop container is approximately 1180px.
- [ ] Hero uses two columns desktop and one column mobile.
- [ ] Activity grid is 3 × 3 desktop and one column mobile.
- [ ] Steps are three columns desktop and one column mobile.
- [ ] Mobile activity cards preserve readable text and evidence thumbnails.
- [ ] No page-level horizontal overflow.
- [ ] Increased text size does not clip content.

### Accessibility

- [ ] A−, A, and A+ controls work and expose state.
- [ ] Language controls update content and metadata.
- [ ] Skip link and semantic landmarks are present.
- [ ] Keyboard focus is visible on every control.
- [ ] Touch targets are at least 44px.
- [ ] Evidence images have descriptive alt text.
- [ ] Completion state is available to assistive technology.
- [ ] AA contrast is maintained.
- [ ] Reduced motion is respected.

### Content and governance

- [ ] Programme ownership is clearly stated.
- [ ] Audience and login method are explained near CTAs.
- [ ] Activities use direct, verifiable language.
- [ ] Evidence expectations are concrete.
- [ ] Last-updated date is visible.
- [ ] Support details and official external links are present.

## 24. Fidelity priorities

If time is limited, preserve these aspects in order:

1. Accessibility and multilingual controls.
2. Institutional green/off-white color system.
3. Noto Sans regular-weight heading hierarchy.
4. Evidence-led hero photography.
5. Numbered activity cards with thumbnails and status.
6. Three-step process and green CTA pattern.
7. Light government-service footer and ownership metadata.
8. Subtle reveal/hover motion.

The result will retain the ToFEI design character with entirely original content when these priorities remain intact.
