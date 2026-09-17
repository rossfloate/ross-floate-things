# Ross Floate Things

The shared design and product system for small Ross Floate utilities.

> **I had a problem, so I fixed it.**

This repository is the canonical source of truth for the family: visual language, interaction rules, accessibility, maker mark, reusable components and lessons learned from real apps.

## How to use this repo

Read [`DESIGN-SYSTEM.md`](DESIGN-SYSTEM.md) before designing or implementing a Ross Floate Thing.

Individual app repositories own their app-specific behaviour, changelog, known issues and next steps. This repository owns decisions that apply across the family.

**NameThese** is the first reference implementation. The system should evolve from things learned while building actual utilities rather than from hypothetical component bureaucracy.

## Current status

Design system: **v0.2**

Current foundation decisions include:

- Mac-assed, not web-assed.
- Authored, not generated.
- Native macOS behaviour first; personality lightly layered.
- Good Internetting's actual H1 treatment is the canonical display voice.
- Safety orange is used for attention and identity, not wallpaper.
- Accessibility is architecture.
- The canonical imprimatur is the circular Ross portrait + **A Ross Floate Thing** as one indivisible maker mark.
- No RF signature, alternate maker logo or secondary authorship mark.
- Progress should show the machinery where useful.
- Every utility gets one restrained unnecessary pleasure.

## Repository shape

- `DESIGN-SYSTEM.md` — authoritative written system.
- `references/` — approved visual reference material and notes.
- `assets/` — canonical shared assets such as the imprimatur artwork once stored here.
- `components/` — reusable implementation patterns/components when real apps justify them.

**The work remembers the work.** Significant family-wide decisions belong here so a future session can resume without reconstructing them from old chats.