# Doxle Design System

First edition · 0.1 · November 15, 2026 · Draft for review

Doxle products should help people feel capable, supported and oriented. The shared system combines calm readable interfaces with luminous blue-violet artwork, warm amber focal accents and softened surfaces. Each product retains its own purpose and recognizable symbol.

This first edition is a design specification and reference kit. It includes a visual specimen and machine-readable foundations; it is not a shipped application framework. Approved artwork and the established family direction remain approved. New component details, numerical defaults and example screens are proposals for review.

## Start here

- [Visual specimen in light and dark](preview.html)
- [Foundation tokens](tokens.json)
- [UI style guide](../guides/DOXLE-STYLE-GUIDE.md)
- [Current brand decisions](../BRAND-GUIDE.md)
- [Approved artwork index](../assets/ASSET-INDEX.json)
- [Brand family workbook](../outputs/01a1ab5c-f2b1-7822-8aea-a0c008b598c0/SLPCC63-brand-family.xlsx)

| Resource | Question it answers |
| --- | --- |
| Brand guide | Who are we, and which product names and artwork are approved? |
| Style guide | What should typography, colors, spacing and surfaces look like? |
| Design system | How do those foundations become consistent controls, states and complete experiences? |
| Workbook | What identities and visual options have been collected? |
| Compass | Which projects and work are tracked, and what is their delivery status? |

## Store naming

Approved November 15, 2026: store names follow “[Product] | Doxle” (Cue | Doxle, Prism | Doxle). Home-screen labels stay Cue, Prism and the other bare product names. This replaces the “by SLPCC63” qualifier. Preserve technical identifiers.

## Scope and authority

The system supports Doxle software and the website. Creative projects keep their own canon and identity. The current branding catalog includes Cue, Prism, Portal, Tether, Trace, Trace for Alexa, Cadence, Sentinel, Handoff, Fuse, SIFT and Dispatch, plus Doxle itself. This is not a verified inventory of every current Compass project. A missing branding entry does not mean a project does not exist.

The central brand guide governs identity and approval. This edition governs proposed shared interface conventions. Product requirements govern functionality. Platform conventions govern native behavior where they differ from the web examples. If these conflict, record the conflict rather than silently changing an approved identity or product behavior.

## Experience principles

**One clear priority.** Give each decision area an obvious useful action. Supporting actions remain accessible without competing for equal emphasis.

**Warmth with restraint.** Use friendly language, spacious layouts and subtle warmth. Keep bright glow away from long reading areas and dense controls.

**Visible orientation.** People should know where they are, how to return and whether a change saved. Preserve their context when moving between related areas.

**Progressive detail.** Present what is needed to act; make explanations and advanced settings easy to open. Do not hide essential limitations or errors.

**Shared family, distinct products.** Reuse foundations and interaction rules while preserving product-specific artwork and vocabulary.

## Foundations

### Color

Use named roles such as canvas, surface, text and action. Do not choose colors independently for every screen. The token file separates brand colors from semantic theme roles.

| Role | Light | Dark |
| --- | --- | --- |
| Canvas | #F7F8FC | #0B1023 |
| Surface | #FFFFFF | #151C34 |
| Raised | #FFFFFF | #1C2542 |
| Text | #18213A | #F7F8FC |
| Muted text | #4E5B73 | #B8C3DB |
| Action | #354AC8 | #B7C6FF |
| On action | #FFFFFF | #111A36 |
| Decorative border | #DFE4EF | #303B58 |
| Control outline | #68748A | #8493B2 |
| Focus | #354AC8 | #B7C6FF |

Brand accents remain electric blue #568BFF, violet #9474FF and amber #FFB547. Gradients flow between cyan, blue and violet. Amber identifies warmth or a focal point; do not assign it conflicting status meanings within a screen. Status always includes words and, when useful, a symbol. Semantic success, warning and danger palettes require component-level review before adoption; this edition does not establish universal status colors.

Decorative borders are intentionally soft. They must not be the only visible boundary of an essential control. Text and controls use tested solid backgrounds rather than unpredictable areas of artwork.

### Typography

Use the platform system sans serif as the proposed foundation. Native Apple interfaces use semantic system styles with Dynamic Type. Web specimens use a system font stack; no custom typeface has been selected.

| Role | Web size | Weight | Line height |
| --- | --- | --- | --- |
| Display | 40–56 px responsive | 600–700 | 1.15 |
| Page title | 28–32 px | 600–700 | 1.2 |
| Section | 20–24 px | 600 | 1.3 |
| Card title | 18 px | 600 | 1.35 |
| Body | 16 px | 400 | 1.5 |
| Supporting | 14 px | 400 | 1.45 |
| Label | 14–16 px | 500–600 | 1.4 |
| Metadata | 12–13 px | 400–500 | 1.4 |

Prefer sentence case, short headings and concrete action labels. Never use a small metadata style for essential instructions. Long text wraps; layouts grow with text enlargement. Use tabular digits where people compare time or measurements.

### Geometry and layout

Spacing steps: 4, 8, 12, 16, 24, 32, 48, 64. Use 16–20 gutters on small screens and 24–32 on larger screens. Cards generally use 16–24 padding. Controls use a 12 radius, cards 16 and dialogs 24. Pills are reserved for compact labels and deliberate exceptions.

Choose layout changes based on content fit. A narrow screen uses one column; primary actions remain reachable. Tables may keep their structure in an accessible horizontal region or switch to a deliberately designed summary. Never drop important fields simply to fit.

Use generous negative space and quiet surface separation. Floating surfaces may use soft shadows; ordinary cards do not need glowing outlines. The specimen's ambient light belongs behind artwork, not behind every field.

## Component specifications

All components require a clear accessible name and defined behavior. The following are specifications, not production-ready implementations.

### Buttons and links

| Variant | Purpose | Rules |
| --- | --- | --- |
| Primary | The principal action within a decision area | Solid action background, on-action label, verb describing the result. |
| Secondary | Supporting action | Quiet surface and essential outline; no equal visual competition with primary. |
| Text action | Lightweight navigation or disclosure | Recognizable link or button treatment, adequate target area, visible focus. |
| Destructive | Irreversible or costly removal | Explicit action/object label, distinct danger styling, confirmation when warranted. |
| Icon button | Familiar compact action | Accessible name, tooltip where useful, sufficient target area; no unlabeled mystery symbol. |

Target 44 by 44 logical units for primary touch controls. Native platforms may require their own minimums. A compact desktop icon may look smaller while preserving a larger hit area.

Required states: default, hover where available, pressed, keyboard focus, disabled and loading. A loading button keeps its width and descriptive label, announces progress appropriately and prevents duplicate submission. Disabled styling cannot be the sole explanation for an unavailable action.

Use a link for navigation and a button for an action. The preview's inert component samples are visual specimens, not working navigation.

### Text fields and selection

Every input has a persistent label. Help text explains format or consequences. Errors identify the field, explain the problem and give a repair action; preserve entered data. Validate at a useful time rather than interrupting every keystroke.

Use a toggle for a binary setting that takes effect immediately. Use a checkbox for independent selections and a radio group for one option among several. A segmented control may switch between a few closely related views. Selected state requires more than color alone.

A form with explicit Save must clearly separate draft values from saved values. Leaving with unsaved changes should protect the user's work. Never use the same interaction sometimes as immediate-save and sometimes as explicit-save without explanation.

### Cards and list rows

A card groups one subject with a clear title, useful content and relevant actions. Avoid nested cards unless the hierarchy is meaningful. If the entire card is navigational, make the target and keyboard behavior clear; do not nest conflicting interactive areas.

List rows share predictable alignment. Keep primary labels, secondary information and trailing actions in consistent positions. A row's selection, status and navigation are different concepts; do not overload one checkmark to mean all three.

### Navigation

Top-level destinations remain stable. Show the current destination and provide a direct route back from subordinate views. Desktop sidebars and mobile navigation can differ in layout while retaining vocabulary and destination identity.

On returning, preserve applicable search, filters, selection and scroll context. Do not redirect people to an unrelated home view after completing a small action. Breadcrumbs suit deep web hierarchies; a native back action suits a native navigation stack.

### Dialogs, sheets and explanations

Use dialogs for bounded decisions requiring attention, not routine information. Provide a title, consequences, primary action and cancel/close path. Keyboard focus enters the dialog, remains within a modal interaction and returns to the invoking control on close. Escape dismisses when dismissal is safe.

Explanations such as Cue's Why open as a clear secondary layer with a return path. They explain the recommendation without introducing a competing set of next actions. The exact recommendation logic remains product-owned.

### Status and feedback

| Situation | Pattern |
| --- | --- |
| Brief successful action | Small confirmation near the action; a toast can supplement it. |
| Important lasting status | Persistent labeled status within the relevant area. |
| Validation error | Field-level message plus summary when the form needs one. |
| Recoverable operation failure | Preserve context, state what failed, offer a truthful recovery action. |
| Empty collection | Explain why it is empty and offer an appropriate next step. |
| No search results | Preserve query and filters; offer a clear way to adjust them. |
| Loading | Stable layout, meaningful progress when known; no invented completion percentage. |
| Offline or stale data | State what is available and the freshness/limitations when they affect decisions. |

Do not rely on a disappearing toast for a critical failure. Announce dynamic status without unnecessarily stealing focus. Skeletons must not create a false impression that unavailable data already exists.

### Tables and data displays

Use descriptive column headings, consistent numeric alignment and explicit units. Sort controls expose their direction. Filters show their current state and have a clear reset. Bulk actions state how many records are affected. Charts need readable labels, non-color distinctions and a textual way to understand the important values.

## Complete interaction patterns

### One recommendation with explanation

Cue answers what deserves attention now with one recommendation, one clear action and an accessible Why disclosure. Supporting context explains time, confidence or relevant limitations only when the product can substantiate it. Avoid fabricated certainty, countdowns or multiple competing recommendations.

The specimen uses illustrative copy to demonstrate hierarchy. It is not a decision-engine output or a finalized Cue workflow.

### Create or edit

Show current values, group related fields, distinguish required information and preserve work through validation. On save, confirm the result and return to the expected context. Ask for confirmation only when the consequence warrants it, not for every reversible action.

### Destructive action

Identify the affected object, explain recovery options honestly and label the final action specifically. Undo can support reversible deletion; it cannot stand in for safeguards around irreversible operations.

### Settings

Organize by user goal. Prefer familiar words over implementation details. Disclose advanced controls progressively. Explain material tradeoffs such as data or storage use at the point of decision. Do not imply guarantees the product does not provide.

## Artwork, icons and motion

Product icons are identity assets; common symbols support interface actions. Use approved masters from the index. Cue uses its first ribbon-and-amber-point concept. Keep unselected alternatives out of release artwork unless explicitly approved.

Dimensional raster symbols work well in spacious feature areas. Small dense controls may use simpler native or independently drawn monochrome symbols. Check each at actual size; never enlarge a raster export as if it were vector artwork. Keep platform-specific licensing separate from cross-platform original assets.

App-icon exports follow the target platform's current requirements. Preserve a full square master; apply a platform mask only where appropriate. Logo clear space should be at least one quarter of the head symbol's height as a provisional starting rule; verify legibility in each use rather than squeezing the full lockup into tiny controls.

Motion explains change and hierarchy. Start with 150–220 ms transitions. Respect reduced motion, avoid continuous attention-grabbing loops and preserve meaning without animation. Hover effects must not be required to understand a control.

## Accessibility and verification

This edition sets review criteria, not a claim of compliance. Core solid-color text pairs in tokens.json are measured in contrast-checks.json; gradients, images, states, actual screens and assistive-technology behavior need their own verification.

Before product adoption, verify keyboard navigation and visible focus, accessible names and grouping, text resizing, light and dark mode, non-color status meanings, touch targets, reduced motion and high-contrast behavior where supported. Use contrast targets of 4.5:1 for ordinary text, 3:1 for large text and 3:1 for essential non-text indicators. Platform-specific requirements and current accessibility standards must be checked during implementation.

## Adoption and change control

1. Choose one representative already-authorized screen and identify applicable components.
2. Map the product's existing styles to semantic roles. Preserve technical IDs and persisted data.
3. Review light and dark layouts plus empty, loading and error states.
4. Record the exact edition and any intentional exception. Keep approved identity separate from implementation and owner acceptance.
5. Expand only after the representative screen is reviewed; avoid an unrequested bulk rebrand.

Edition 0.1 establishes the documentation and specimen baseline. A future patch corrects documentation without altering meaning; a minor edition adds compatible patterns; a major edition changes established conventions. Retain approval evidence and old masters. New detailed defaults become approved only through an explicit decision.

The future Compass branding section may reference these files, record coverage and track adoption. Its schema and hosted integration are owned by the separate Compass work thread. This edition does not create that section or write project records.

## First edition review

The next review should decide whether to adopt the proposed system font, semantic themes, spacing and component treatments. Missing approved masters, a full Compass coverage reconciliation, production component libraries and product rollouts remain distinct work. The existing workbook has not been rewritten as part of this edition.

report_back_to: Extend project branding

report_back_url: codex://threads/01a1ab5c-f2b1-7822-8aea-a0c008b598c0

report_back_instructions: return design decisions, approved exceptions and exact artifact or screen evidence to this branding chat. Preserve each project's implementation and QA destinations. This route alone does not authorize sending messages.
