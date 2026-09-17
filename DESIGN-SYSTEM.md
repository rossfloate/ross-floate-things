# Ross Floate Things

**Interface and product system — v0.2**  
**Status:** Canonical living source of truth

This document records the shared product and interface language for small Ross Floate utilities. It exists so the work carries its own context across chats, devices, collaborators and implementation sessions.

## What these things are

Small, focused utilities born from a simple instinct: **I had a problem, so I fixed it.**

They should feel authored rather than generated: useful first, distinctly Ross second, and never burdened with product-platform theatre.

## Core principles

### 1. Mac-assed, not web-assed
Use native macOS behaviour and conventions unless there is a good reason not to. These are Mac tools, not web dashboards trapped in windows.

### 2. Whimsy reveals function
Quirk should make the state of the tool clearer or more pleasurable, never harder to understand. A split-flap counter for thousands of processed files is good because it is both legible and delightful.

### 3. Small tools deserve good manners
Cancel means cancel. Quit means quit. Progress is truthful. Errors explain what happened and what the user can do next. Never leave the user wondering whether the app is working.

### 4. Safety orange is the signature, not wallpaper
Use Ross safety orange deliberately for identity, hierarchy, emphasis and selected moments. **Orange means attention.** Selected navigation, primary action, active progress, key numbers and app identity are appropriate uses. Do not flood the interface with it or use it as decoration for decoration's sake. Never sacrifice contrast or legibility to preserve the colour.

Good Internetting currently uses **#FF5A00** for its H1. Treat this as the known display orange and starting point for the family palette. Accessible production variants for specific light/dark UI contexts remain to be tested rather than guessed.

### 5. Accessibility is architecture
Accessibility is designed in from the first build, not backfilled.

- Meet appropriate contrast requirements.
- Never communicate meaning by colour alone.
- Support keyboard operation and sensible focus order.
- Give controls and changing status useful VoiceOver labels/announcements.
- Respect Reduce Motion.
- Do not require animation to understand progress.
- Completion sounds must be restrained and respect user/system sound choices; visual completion feedback must always exist too.
- Prefer native controls where they provide better accessibility and platform behaviour.

### 6. One unnecessary pleasure
Every utility should contain at least one small detail whose job is simply to make using it nicer: a satisfying counter, a tiny animation, excellent completion copy, a polite chime, or another restrained moment of delight.

It must never interfere with getting the job done.

### 7. Authored, not generated
Avoid the generic AI/SaaS visual vocabulary: endless rounded cards, excessive whitespace, gratuitous gradients, dashboard furniture and decoration without purpose.

The interface should have opinions.

### 8. Show the machinery
When useful, expose real state: files processed, items found, elapsed work, totals, current operation and meaningful progress. Interesting work does not need to be hidden behind an indeterminate spinner.

### 9. It is a tool, not a platform
Do the thing. Do it extremely well. Get out of the way.

### 10. Native first; personality lightly layered
Let macOS handle what macOS already handles well. Add Ross personality where it improves recognition, comprehension or pleasure. Do not fight the platform merely to be distinctive.

## Visual direction v0.2

The baseline is a dark, compact, information-rich Mac utility with restrained safety-orange highlights, strong typography, clear hierarchy and visible processing state. It should feel closer in spirit to a well-made Mac instrument than a miniature SaaS product.

**Reference sensibility:** Bjango / iStat Menus — functional, dense when useful, polished, Mac-native and still possessed of personality. This is a sensibility reference, not a request to copy its visual design.

The first approved Ross Floate Things direction board is **Reference Board 001**. Its baseline choices are provisionally accepted rather than treated as a fresh design problem: charcoal/dark surfaces, secondary greys, muted grey, warm off-white supporting material, compact density, restrained radii and borders, native controls and orange used for attention. Later decisions supersede two elements visible on the early board: the exact orange starts from Good Internetting #FF5A00, and the RF signature is not part of the system.

## Typography

### H1 / display heading

The canonical Ross Floate Things H1 is the actual **Good Internetting** H1 treatment, translated appropriately into native app UI rather than approximated from the reference board.

Source treatment from `rossfloate/good-internetting`:

- Font family: **Georgia**, with **Times New Roman** then generic **serif** as fallbacks on the web.
- Font size: `clamp(48px, 10vw, 112px)` on the website. Native apps should preserve the same deliberately oversized display-heading character while sizing for the actual window rather than mechanically reproducing CSS pixels.
- Line height: **0.82**.
- Letter spacing: **-0.065em**.
- Weight: browser/default bold H1 weight; the source does not specify a custom `font-weight`.
- Colour: **#FF5A00** on Good Internetting.
- Casing: natural/mixed case, not forced uppercase.
- The Good Internetting source uses a deliberate line break (`Good` / `Internetting.`); line breaks in apps should be intentional rather than automatic decoration.

This is the family display voice. Do not substitute the Georgia-ish approximation from the early reference board: the Good Internetting implementation is the source of truth.

Functional/interface copy should normally use native macOS system typography so controls remain Mac-assed and legible. Additional intermediate text styles should be introduced only when a real app demonstrates a need for them.

## Baseline colour direction

Provisionally accept the reference board's small, useful palette rather than inventing a large brand palette:

- Ross display orange: **#FF5A00** — canonical starting orange from Good Internetting.
- Charcoal: approximately **#1E1E1E** — primary dark surface/background baseline.
- Secondary dark: approximately **#3A3A3A** — secondary surface/control baseline.
- Muted grey: approximately **#8E8E93** — secondary/muted information baseline.
- Primary dark-mode text: white/off-white with native/system values preferred where appropriate.
- Supporting/reference material may use a warm off-white rather than sterile white.

These are baseline design choices, not permission to hard-code inaccessible combinations. Native semantic colours should be preferred when they achieve the intended appearance and behaviour. Exact accessible variants and state colours should emerge from the reference implementation.

## Standard app anatomy

Use only the pieces the utility actually needs, but the family should normally provide:

- Clear app/task title using the canonical H1/display language where appropriate.
- Immediate explanation of what the tool does.
- Native input or drag-and-drop behaviour where appropriate.
- A real processing state rather than a cigarette-burn spinner where determinate progress is available.
- Useful count/status information.
- A genuine Cancel action during long operations.
- Clear completion state and next action.
- Recoverable, human-readable errors.
- Normal macOS Quit behaviour.
- A very small visible version number in the UI.
- The canonical circular Ross portrait + **A Ross Floate Thing** imprimatur, used as one quiet maker mark.

## Progress and counters

Progress is a signature opportunity.

Prefer determinate progress whenever the underlying operation permits it. For large item counts, explore a restrained mechanical/split-flap-inspired numeral treatment. It must remain readable, performant and accessible. VoiceOver should receive sensible periodic status rather than every animated digit change.

Show useful language such as the current count and total. Avoid fake precision and invented time remaining.

When Reduce Motion is enabled, counters should update without flip animation.

## Sound and motion

Motion should communicate transition or state, not provide constant visual activity. Keep it short and purposeful.

A subtle completion chime may be part of the family. It must not be the only completion signal and should never become noisy when processing batches repeatedly.

## Copy

Short, plain, confident and human. A little wit is welcome. Do not make the user decode jokes to understand state, errors or actions.

Avoid corporate product language and AI-ish enthusiasm.

## Imprimatur

The canonical maker mark is the approved circular Ross portrait paired with the words **A Ross Floate Thing**. The portrait and words form one indivisible imprimatur: the mark of authorship for the app family.

Use it quietly, small and consistently. It is interface furniture, not advertising.

Do not add a separate signature, RF monogram, maker logo, name treatment or secondary authorship mark elsewhere in the interface. In particular, there is no signature on the right.

Do not redraw, reinterpret or AI-generate a substitute portrait. Use the canonical approved circular artwork. Until that binary asset is stored in this repository's shared assets, implementations must treat the artwork as an external required asset rather than recreating it.

## Components and states

Do not build a giant theoretical component catalogue. Components are codified when a real app needs them.

The first reusable candidates visible in Reference Board 001 are:

- Primary, secondary and tertiary buttons.
- Drag/drop target.
- Progress bar and processing status.
- Split-flap-inspired count/status display.
- Status/footer furniture.
- Result grid/list patterns.
- Completion, empty and error states.
- Search/filter controls.
- Very small version treatment.
- Imprimatur.

For each component, define behaviour as it becomes real: idle, hover, keyboard focus, pressed, disabled, drag-over where relevant, working, cancelled, success and failure. Accessibility behaviour is part of the component, not separate documentation.

## Versioning

Every shipped/test build displays a small version number in the interface. App-specific repositories should maintain a short changelog or dated project-state record so a future session can determine what changed and why.

## Project memory rule

**The work remembers the work.**

Do not rely on chat history as the sole source of project context. Significant family-wide decisions discovered during design/build sessions belong in this repository. App-specific decisions belong in the relevant app repository.

For each app, keep enough repository context to answer:

1. What does this app do?
2. What is the current version/state?
3. What changed recently and why?
4. What decisions are unique to this app?
5. What is known to be broken or unfinished?
6. What should happen next?

A fresh collaborator or AI session should be able to read this design system plus the app repository and resume work without reconstructing the project from old conversations.

## Workflow

1. **Think together.** Explore the problem, interaction and taste before implementation.
2. **Record decisions.** Update this repository when a decision becomes a family-wide rule; update the app repository when it is app-specific.
3. **Implement.** Give the build environment an explicit brief grounded in these documents.
4. **Test the actual thing.** Function, accessibility, cancellation, errors, performance and feel all matter.
5. **React to it.** Keep what works; reject what does not.
6. **Feed learning back into the system.** The design language evolves from real apps, not a theoretical brand exercise.

**Build → notice → codify.**

## Reference implementation

**NameThese** is the first app to be deliberately redesigned against Ross Floate Things v0.2. It is the reference implementation from which reusable Swift components and more precise visual rules should emerge.

Hands and Ball should become the second test: if the system transfers cleanly from NameThese, the family has a real design system rather than a NameThese theme.

## Still to define

- Accessible production variants/state uses for Ross orange in light/dark contexts.
- Canonical maker-mark binary asset storage and implementation.
- Split-flap counter implementation and motion behaviour.
- Completion sound/chime.
- Shared Swift component package or source structure.
- Light/dark appearance policy.
- Standard spacing and sizing tokens, if they prove useful rather than bureaucratic.
- Signing, notarisation and repeatable release process.

---

**Principle for changing this document:** codify things we have actually learned. Do not create bureaucracy for hypothetical future apps.