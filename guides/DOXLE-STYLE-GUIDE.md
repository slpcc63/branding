# Doxle UI Style Guide

Version 1 draft for review · November 15, 2026

Doxle interfaces should feel warm, capable and calm. Blue-violet depth connects the products; clear hierarchy and restrained amber accents help people see what matters. This guide turns that direction into practical defaults for websites and apps.

The existing brand identity and approved artwork remain authoritative in [the brand guide](../BRAND-GUIDE.md) and [asset index](../assets/ASSET-INDEX.json). Exact interface measurements and additional theme colors below are proposed defaults, pending visual approval. They are not claims about existing app implementations.

## How the documents fit together

| Resource | Purpose |
| --- | --- |
| Brand guide | Identity, product names, approved visual direction and usage boundaries. |
| UI style guide | Fonts, sizing, color roles, spacing, surfaces, controls and appearance rules. |
| Brand family workbook | Visual catalog of products, icons, logo alternatives and approval status. |
| Asset index | Exact artwork paths and approval classifications. |
| Doxle Design System | The broader shared system: these foundations plus reusable components, interaction patterns, accessibility guidance and implementation resources. |

[The first design-system edition](../design-system/DOXLE-DESIGN-SYSTEM.md) now defines component and interaction specifications, with a visual specimen and foundation tokens. A finished production component library has not been delivered. The workbook is a catalog, not the full design system.

## Coverage and Compass

These foundations apply to the shared Doxle software and website family. Product-specific exceptions must be deliberate and documented. Creative projects retain their established visual identity and canon.

The current catalog includes Doxle, Cue, Prism by SLPCC63, Portal, Tether, Trace, Trace for Alexa, Cadence, Sentinel, Handoff, Fuse, SIFT and Dispatch. Some entries still lack a collected approved master; consult the asset index before integration.

Coverage has not been reconciled against the current hosted Compass inventory. Do not describe the workbook or this guide as covering every Compass project. Compass remains the project source; the branding folder is the appearance and artwork source. A future coverage review should match verified project identities to brand entries and record approved artwork, missing assets, applicable style exceptions and implementation status separately.

## Principles

1. Make the next useful action easy to recognize.
2. Convey warmth through color, shape and language without adding visual noise.
3. Use depth to explain hierarchy, not to decorate every element.
4. Keep navigation predictable and preserve context when people return.
5. Let each product retain a recognizable motif within the family.

## Color foundations

These existing family reference colors anchor the palette:

| Color | Value | Role |
| --- | --- | --- |
| Midnight | #0B1023 | Dark canvas and deep brand backgrounds. |
| Pearl | #F7F8FC | Light canvas and dark-mode primary text. |
| Electric blue | #568BFF | Brand highlights and artwork. |
| Violet | #9474FF | Secondary brand highlights and artwork. |
| Amber | #FFB547 | Warm focal accents and attention, used sparingly. |

Proposed semantic theme defaults:

| Role | Light | Dark |
| --- | --- | --- |
| Canvas | #F7F8FC | #0B1023 |
| Surface | #FFFFFF | #151C34 |
| Raised surface | #FFFFFF | #1C2542 |
| Primary text | #18213A | #F7F8FC |
| Secondary text | #4E5B73 | #B8C3DB |
| Primary action | #354AC8 | #B7C6FF |
| Text on primary action | #FFFFFF | #111A36 |
| Link | #354AC8 | #B7C6FF |
| Decorative border | #DFE4EF | #303B58 |
| Essential control outline | #68748A | #8493B2 |

Use semantic roles rather than applying raw brand colors everywhere. Pale decorative borders may separate cards; essential controls need sufficiently visible outlines. Amber is not automatically a warning, and blue is not automatically success. Pair status color with an icon and plain-language label. Establish status colors with the implementation’s contrast checks.

For gradients, flow from cyan through electric blue into violet. Reserve amber for a distinct focal area. Body text sits on stable, quiet backgrounds; do not put it over bright bloom or moving gradients.

## Typography

Proposed default: the platform system sans serif. Use the native system font in Apple apps and a system sans-serif stack on the web. This provides a familiar, readable foundation without requiring a new commercial font. A custom brand typeface remains open for a later specimen review.

| Text role | Web starting size | Weight | Line height |
| --- | --- | --- | --- |
| Marketing display | 40–56 px, responsive | 600–700 | 1.1–1.2 |
| Page title | 28–32 px | 600–700 | 1.2 |
| Section title | 20–24 px | 600 | 1.3 |
| Card title | 18 px | 600 | 1.35 |
| Body | 16 px | 400 | 1.5 |
| Label and button | 14–16 px | 500–600 | 1.4 |
| Supporting text | 14 px | 400 | 1.45 |
| Minor metadata | 12–13 px | 400–500 | 1.4 |

Use native semantic text styles and Dynamic Type in Apple apps rather than copying pixel sizes literally. Essential instructions should not depend on tiny metadata. Support text resizing and allow labels to wrap. Prefer sentence case; reserve uppercase for short, exceptional labels. Use tabular numerals when comparing times or measurements.

## Spacing and layout

Use a 4-unit spacing rhythm: 4, 8, 12, 16, 24, 32, 48 and 64. Units are CSS pixels on the web and logical points in native layouts, adapted to platform conventions.

- Mobile content gutters: 16–20. Desktop content gutters: 24–32.
- Card padding: 16–24. Related field spacing: 12–16. Section spacing: 24–32.
- Reading text: approximately 60–75 characters per line.
- Marketing content: usually within a centered 1120–1200-wide container. Data-heavy tools may use more space.
- Small screens: one clear content column. Add columns when the content fits comfortably, not at the expense of labels or controls.

Keep the primary action near its relevant content. Avoid nested cards that obscure hierarchy. Dense tools may tighten spacing while retaining readable labels and usable targets.

## Surfaces and depth

Proposed radii: 10–12 for controls, 16 for cards and 20–24 for dialogs. Fully rounded pills are for compact tags or a deliberate special action, not every container.

Use softened borders with subtle tonal separation. Shadows should be broad, low-opacity and limited to elevated surfaces such as popovers and dialogs. Avoid thick outlines, glossy reflections on controls and bright glows around every card.

Place blue-violet ambient light behind hero artwork or a key feature, keeping the reading area calm. Dark mode should preserve visible surface hierarchy; light mode should retain pearl backgrounds rather than placing every component on saturated gradients.

## Controls and states

| Component | Appearance and behavior |
| --- | --- |
| Primary button | Solid theme action color, clear verb, one dominant action per decision area. |
| Secondary button | Quiet surface with visible outline; supports the primary action. |
| Text action | Recognizable link treatment with visible hover and keyboard focus. |
| Destructive action | Explicit wording and a distinct danger treatment; request confirmation when consequences warrant it. |
| Input | Persistent label, visible boundary and nearby help or error message. Placeholder text does not replace a label. |
| Toggle | Describes the resulting enabled state; changes immediately unless the flow clearly has Save. |
| Card | Clear heading and grouped content. If clickable, expose a clear target and focus state. |
| Dialog | Clear title, close or cancel path and predictable return to the invoking control. |

Design default, hover, pressed, focus, disabled, loading, error and selected states. Hover must never be the only way to discover an action. Loading states preserve context and prevent accidental duplicate actions. Explain disabled actions when the reason would otherwise be unclear.

Proposed target size: at least 44 by 44 logical units for primary touch controls. Give compact desktop controls sufficient spacing and a larger usable hit area where practical.

## Navigation and interaction

Keep the current location visible. Related sections share stable navigation, and detail views provide a clear return path. Preserve filters, scroll position and selection when returning where appropriate. Labels describe destinations consistently; do not change the same section’s name between screens.

For Cue specifically, the main experience centers on one recommendation and a tappable Why. Supporting information stays available without becoming competing recommendations. The style guide does not alter the decision engine or interruption policy.

## Icons and artwork

Use the approved product masters from the asset index. Cue’s selected icon is the first concept: the embracing blue-violet C-shaped ribbon with one amber sphere. The other Cue concepts remain unselected alternatives.

The shared 500-icon pack provides dimensional raster symbols. Use these selectively for prominent features, onboarding or spacious navigation. Small or dense controls may need simpler native or independently drawn monochrome symbols to remain legible. Keep platform-specific symbol licensing separate from cross-platform originals.

Common UI icon sizes start at 20–24 for controls and 32–48 for feature illustrations. Test each raster at its actual displayed size and export scale. Do not enlarge a small export as if it were a vector master. Preserve product-specific shapes; do not redraw approved app icons as generic library symbols.

## Motion and accessibility

Use short, purposeful transitions; 150–220 ms is a proposed starting range. Respect reduced-motion preferences and avoid continuous pulsing that competes for attention. Important state changes must remain understandable without animation.

Verify actual screens in both themes, with keyboard navigation, text enlargement and assistive technology. Check normal-text contrast against a 4.5:1 target, large text against 3:1, and essential non-text boundaries against 3:1. These are verification targets, not certification of this proposed palette. Never rely on color alone for meaning. Keep focus indicators visible on every background.

## Applying the guide

Start with one representative screen in light and dark mode before extending new defaults across a product. Review a normal, empty, loading and error state. Record departures needed for a platform or product. An approved icon does not imply approval of an interface, successful integration or release acceptance.

Current next step: visual review of this first style-guide draft. Reusable component implementations, project-by-project adoption and a complete Compass coverage audit remain separate work.

Report back to: Extend project branding

Report back URL: codex://threads/01a1ab5c-f2b1-7822-8aea-a0c008b598c0

Report back instructions: return style decisions, product exceptions and verified preview or implementation evidence to this branding chat. Preserve each project’s own delivery and QA destinations. This saved route does not authorize sending messages.
