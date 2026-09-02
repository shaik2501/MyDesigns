# MastryHub Design Blueprint

Source: https://mastryhub.com/

Use this document as a reusable design prompt for recreating the visual language of MastryHub without copying its brand text, logos, or event content verbatim.

## Design direction

Create a bold, rebellious builder-community and hackathon platform. The experience should feel like a digital zine mixed with an arcade interface: black and white foundations, loud yellow accents, rough display lettering, hard offset shadows, oversized typography, sticker-like cards, looping marquees, and playful technical diagrams.

## Core page set

The `pages/` directory records the stable public product surfaces rather than every changing event or hub detail page:

- `explore.png` — combined discovery surface.
- `events.png` — hackathon/event listing.
- `hubs.png` — community hub listing.
- `become-organizer.png` — organizer entry page.
- `journey.png` — participant journey entry page.
- `catalyst.png` — Catalyst program page.
- `about.png` — company and community story.
- `login.png` — authentication entry screen.

## Color system

| Role | Color | Use |
|---|---|---|
| Primary canvas | `#000000` | Hero, footer, navigation, dramatic sections |
| Primary ink | `#FFFFFF` | Headings, cards, inverse body text |
| Signature accent | `#FACC15` / `#FFDE59` | Highlights, active labels, CTA backplates, marquee accents |
| Deep surface | `#0A0A0A` / `#0F0F0F` | Raised dark panels |
| Muted copy | `#A3A3A3` | Supporting text and metadata |
| Alert accent | `#FF4757` / `#E84C3D` | Energetic labels, badges, diagrams |
| Success accent | `#06C270` | Status and positive signals |
| Cyan accent | `#3EC1D3` | Illustrative nodes and category accents |
| Blue accent | `#2F80ED` | Links and ecosystem categories |
| Purple accent | `#8E44AD` | Secondary category differentiation |

Keep most sections monochrome. Use yellow as the dominant accent and reserve the other colors for compact labels, icons, diagram nodes, and occasional cards.

## Typography

- Body and interface: `Space Mono`, monospace.
- Condensed utility headings: `Oswald`, weights 500 and 700.
- Primary display style: the site’s custom `Trap`-style face or a similarly heavy, angular grotesk.
- Decorative distressed styles: rough, hand-cut, punk or stamped display faces similar in character to BombSound, KindlyCrunch, and 23Seconds.
- Body default: 16px / 24px, regular.
- Metadata: 10–14px, uppercase, with generous positive tracking.
- Section headings: 36–76px, tight line-height, often uppercase.
- Hero lettering: 72–96px on desktop; clamp responsively.
- Background display words may exceed 200px and can be partially cropped.

Headlines should be short, high contrast, and visually irregular. Highlight one important phrase using a yellow rectangular marker, outlined lettering, or a rotated sticker.

## Layout and spacing

- Use full-width alternating black, white, and pale neutral bands.
- Center main content within 1200–1400px containers.
- Desktop sections typically use 64–120px vertical padding.
- Build two-column hero and feature layouts with a 45/55 or 50/50 split.
- Mix disciplined grids with intentional overlaps, rotated tags, and oversized cropped decoration.
- Use wide gutters on desktop and reduce to 20–24px on mobile.
- Important sections may remain pinned while copy or illustrations transition during scroll.

## Shape language

- Prefer square corners for editorial sections and 8–12px rounding for cards.
- Pills and chips use a 9999px radius.
- Use thick black or white outlines, usually 2–4px.
- Signature hard shadows: `4px 4px 0 #fff`, `4px 4px 0 #000`, `6px 6px 0 #000`, or `4px 4px 0 #facc15`.
- Buttons should resemble printed labels: solid fill, bold border, offset shadow, minimal softness.
- Add circles, connector lines, dotted paths, ticket edges, browser frames, sticky notes, and rough underline strokes.

## Images and illustration

- Favor vector-like browser mockups, community collages, event posters, logos, avatars, and diagrammatic illustrations.
- Present imagery inside framed cards with strong borders and offset colored backplates.
- Maintain sharp contrast and deliberately layered depth.
- Partner logos may run in a continuously moving horizontal strip.
- Use real photographs sparingly and crop them tightly inside poster-like cards.

## Core components

### Navigation

Use a compact dark navigation treatment with a strong wordmark, menu trigger or rail, and a visible dark-mode control. Navigation should feel functional and slightly industrial.

### Hero

Pair a massive distressed headline with one yellow-highlighted phrase. Place primary and secondary CTAs below the copy. Balance the text with a browser-window or product illustration using an offset yellow backplate.

### Event and hub cards

Use poster-like cards with image, category label, event title, date/status metadata, and an obvious action. Mix monochrome cards with occasional bright accent cards. Cards should respond with a short translate, shadow, or border-color change.

### Marquee

Create a full-width ticker containing short uppercase verbs separated by stars or symbols. The loop must be seamless and keep strong contrast against its section.

### Journey diagrams

Represent progress as connected nodes, checkpoints, or pitstops. Combine labels, icons, lines, and compact explanatory cards so the system feels like a game map.

### Authentication

Keep the sign-in page visually consistent with the main product: dark canvas, compact centered panel, monospaced labels, strong outlined controls, and yellow as the primary action color. Avoid adding unrelated decorative density that distracts from authentication.

### Footer

Use an oversized, theatrical closing area with social links, contact details, large cropped type, and the same hard-edged black/yellow language.

## Interaction and motion

- Hover transitions: 150–300ms for color, translation, and hard-shadow changes.
- Large illustration transitions: 500–1200ms.
- Marquees and logo strips loop horizontally at a steady readable speed.
- Use scroll-triggered reveals and pinned storytelling sections sparingly.
- Buttons may shift 2–4px toward their shadow on press.
- Respect `prefers-reduced-motion`; replace loops and pinned transformations with static layouts.

## Responsive behavior

- Stack two-column sections vertically below tablet widths.
- Scale hero type with `clamp()` and preserve its distressed impact without overflow.
- Convert side navigation to a compact menu.
- Allow card grids to move from three columns to two and then one.
- Keep horizontal lists swipeable where useful, but never hide essential actions off-canvas.
- Remove decorative overlaps that obscure reading on narrow screens.
- Maintain 44px minimum interactive targets.

## Accessibility

- Preserve strong text contrast on black and white surfaces.
- Do not use color alone for status or category meaning.
- Add useful alt text for event art and meaningful illustration; mark decorative marks as hidden.
- Provide visible focus states that match the yellow/white outline system.
- Keep rough display type for headings only; use Space Mono for longer reading.
- Ensure moving marquees can pause and are disabled for reduced-motion users.

## Reusable generation prompt

Design a responsive builder-community or hackathon platform with a black-and-white editorial base, electric yellow as the primary accent, Space Mono interface text, oversized distressed uppercase display headings, thick outlines, hard offset shadows, poster-like cards, looping marquees, browser-window illustrations, diagrammatic journey maps, sticker labels, and energetic asymmetric composition. Alternate dramatic black sections with clean white breathing space. Keep content containers between 1200 and 1400 pixels, use bold two-column storytelling, and stack cleanly on mobile. Include discovery cards, community hubs, organizer and journey entry points, an accessible sign-in screen, and a theatrical oversized footer. Motion should feel playful and mechanical while respecting reduced-motion preferences.

## Do not

- Do not soften the design into a generic gradient SaaS page.
- Do not replace the hard shadows with floating glassmorphism.
- Do not overuse all accent colors in one section.
- Do not use distressed type for paragraphs or form instructions.
- Do not reproduce the original brand, logos, copy, or event artwork without permission.
