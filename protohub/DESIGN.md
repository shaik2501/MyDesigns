# ProtoHub — Design Blueprint and Reusable Build Prompt

Source: https://protohub.wedevit.in/landing

Use this document as the visual authority for future public-sector innovation, fabrication-network, prototyping, facility-booking, or government workflow products inspired by this design language. Replace the source identity, government marks, programme names, seeded records, and copy with original or authorized material.

## Core public page gallery

The `pages/` folder preserves the stable public and authentication surfaces:

- `landing.png` — statewide platform proposal and service overview.
- `facilities.png` — public facility discovery, filters, cards, and map.
- `track.png` — project tracking entry.
- `login.png` — role-based portal authentication.
- `register.png` — account-creation entry state.

Private role dashboards and seeded demo records are intentionally excluded from the public design archive.

## Design direction

Create an accessible, trustworthy public-service platform for a statewide prototyping network. The interface should feel official and operational without becoming bureaucratically dense: deep navy anchors, saffron actions, white information cards, cool gray application surfaces, precise grid alignment, compact accessibility utilities, map-led discovery, clear workflow diagrams, and role-specific portal entry.

The visual tone combines a government information portal with a modern industrial operations product. Emphasize provenance, status, geographic reach, service boundaries, and the distinction between public information and authenticated workflows.

## Color system

| Role | Value | Use |
|---|---|---|
| Primary navy | `#003580` | Navigation, key headings, links, controls |
| Deep navy | `#0B1744` | Hero fields, workflow bands, footer, portal framing |
| Saffron accent | `#FF9933` | Primary CTAs, active emphasis, small rules |
| White | `#FFFFFF` | Cards, form panels, content surfaces |
| App background | `#F0F4F8` / `#F6F8FB` | Alternating sections and portal canvas |
| Main text | `#212529` | Long-form copy and card headings |
| Secondary text | `#526079` | Supporting descriptions and metadata |
| Muted text | `#8A9AB5` | Captions and disabled states |
| Success green | `#198754` / `#138808` | Available status and completed steps |

Use saffron deliberately for actions and programme emphasis. Navy should carry institutional trust; green communicates operational state. Do not decorate every card with all three colors.

## Typography

- Primary family: `Noto Sans`, with system sans fallbacks.
- Institutional utility text may use Helvetica Neue or Arial.
- Technical identifiers and compact machine/project values may use monospace.
- Hero heading: 48–64px desktop, bold, tight line-height.
- Section heading: 30–44px, dark navy, strong weight.
- Card heading: 16–22px.
- Body: 14–17px with 1.45–1.65 line-height.
- Eyebrows and metadata: 11–13px, uppercase or semibold.

Keep typography highly legible. Use saffron only to emphasize a word or short phrase inside a heading; do not use it for paragraphs.

## Layout and alignment

- Use a full-width accessibility utility bar above the main header.
- Main content containers should sit around 1160–1240px.
- Alternate white and pale-gray section backgrounds to separate workflows.
- Hero uses a deep navy field with left-aligned narrative and right-aligned operational dashboard illustration.
- Service journeys use modular cards in three- or four-column grids.
- Architecture and ownership information should be diagrammatic and easy to scan.
- Geographic discovery combines a large map with facility cards and compact filters.
- Public pages use generous 64–96px section spacing; authenticated pages are denser.

Align text, icons, labels, and buttons to a consistent grid. Intentional asymmetry may be used in the hero, but operational sections should remain orderly.

## Shape language

- Square geometry dominates; most elements use `0px` radius.
- Controls and compact cards commonly use 4–6px rounding.
- Featured cards and panels may use 8–14px rounding.
- Status chips may use 999px pill geometry.
- Use thin cool-gray borders and occasional saffron top rules.
- Avoid heavy soft shadows; use restrained elevation for maps, modal cards, and floating operational summaries.
- Use circles for map markers, workflow nodes, avatar initials, and status indicators.

## Header and accessibility controls

Create a slim utility strip containing skip navigation, screen-reader guidance, text-size controls, and language selection. Below it, place the institutional marks, programme name, short status descriptor, anchor navigation, and one saffron primary action.

All controls require visible focus states, usable keyboard order, and clear accessible names. Text-size controls must visibly indicate the current selection.

## Hero

Use a deep navy gradient or flat field with a subtle technical pattern. Place a short status eyebrow above a bold multiline headline. Highlight one word in saffron. Follow with concise explanatory copy, a saffron primary CTA, a secondary outlined CTA, and small trust/status chips.

On the right, show a realistic operational mockup: project count, utilization bars, facility status, estimate, or workflow card. Keep the mockup information-dense but readable.

## Core components

### Trust and status panel

State what is operational, illustrative, seeded, or planned. Use labeled definition rows or a compact matrix. This pattern is essential for prototypes, pilots, and public-sector systems where product boundaries must be explicit.

### Service journey cards

Use icon-led cards for discovery, booking, estimates, expert support, tracking, analytics, and operations. Each card needs a title, one short explanation, and a direct action. Keep icon treatments pale and consistent.

### Platform architecture

Explain responsive web, mobile targets, layers, ownership, security, multi-tenancy, and scalability using connected blocks, small labels, and thin lines. Distinguish current capabilities from future targets.

### Facility map and cards

Pair a large geographic map with filters and compact facility markers. Below or beside it, show cards with city, utilization, capabilities, machine availability, and one clear routing action. Keep map attribution visible.

### Role-based login

Use a split authentication layout: a navy informational panel explains the service, while a white form panel provides role cards and credential access. Roles should show a short description and a clear one-click demo or sign-in action. Registration should appear as a secondary path.

### Project tracking

Keep tracking entry minimal: one identifier field, explanatory hint, strong submit action, status privacy note, and visible path back to public help.

### Footer

Use a deep navy footer with programme status, public links, support, accessibility, external references, and last-updated information. Add a thin saffron rule for visual closure.

## Imagery and icons

- Prefer maps, operational UI mockups, charts, workflow diagrams, machine/facility icons, and approved institutional marks.
- Use line icons with consistent stroke weight.
- Avoid stock-photo-heavy storytelling; the system itself is the primary visual evidence.
- When photography is necessary, show fabrication labs, equipment, prototypes, and people using services in authentic contexts.

## Motion and interaction

- Use 150–250ms hover, focus, and expansion transitions.
- Reveal workflow steps and map results without dramatic parallax.
- Animate progress bars and counters only when they enter view.
- Keep modals focused and trap keyboard focus correctly.
- Respect `prefers-reduced-motion`.
- Never allow animation to delay access to forms, maps, or status information.

## Responsive behavior

- Collapse the main navigation to a menu while retaining accessibility and language controls.
- Stack hero copy above the operational illustration.
- Convert service grids from four columns to two and then one.
- Move map filters above the map; place facility cards below it.
- Keep tables horizontally scrollable only when a card alternative would lose meaning.
- Preserve 44px minimum touch targets and adequate form spacing.
- Prevent institutional marks and programme titles from crowding the header on narrow screens.

## Accessibility

- Include a skip link as the first focusable control.
- Support text resizing without clipping or overlap.
- Maintain WCAG-level contrast for navy, saffron, green, and gray combinations.
- Do not use color alone for facility availability or project status.
- Label map controls, markers, icons, dialogs, and charts.
- Keep headings semantic and ordered.
- Provide multilingual content without changing navigation structure.
- Make prototype or non-production status explicit in text.

## Reusable generation prompt

Design a responsive, accessible public-sector prototyping and facility-network portal with a deep navy institutional foundation, saffron primary actions, white and pale-gray content surfaces, Noto Sans typography, square information panels, compact accessibility and language controls, a high-contrast operational hero, workflow-service cards, architecture diagrams, map-led facility discovery, utilization and availability indicators, role-based authentication, project tracking, and a dense navy public-information footer. Keep the visual system trustworthy, grid-aligned, and operational. Clearly separate public information, demo data, authenticated actions, and planned capabilities. Avoid generic SaaS gradients, excessive rounding, and decorative stock imagery.

## Do not

- Do not copy government emblems, programme logos, facility data, or seeded accounts without authorization.
- Do not imply that a prototype is an official production service.
- Do not remove accessibility, language, attribution, or status information.
- Do not use saffron as a large reading background.
- Do not over-round the interface or add glassmorphism.
- Do not hide core service boundaries inside legal fine print.
