# Components

Reusable Ross Floate Things implementation patterns belong here **after real apps prove they are reusable**.

Do not pre-build a giant component library.

NameThese is the first reference implementation. When a component or behaviour survives that build and proves family-wide, codify it here. Hands and Ball is the second transfer test.

Initial candidates: buttons, drag/drop target, progress/status, split-flap counter, completion/error/empty states, version furniture and the imprimatur.

**Build → notice → codify.**

## Proven in NameThese 1.0

The first reference build established a small set of reusable implementation
decisions without requiring a shared component package yet:

- In a compact native Mac utility, use Georgia Bold for the display heading and
  keep controls, status, tables and settings in the system font.
- Use `#FF5A00` for attention states with redundant non-colour cues. In NameThese
  it identifies the display heading and active drag target; it is not general
  surface decoration.
- A drag target can remain the whole working surface. During a valid drag, add a
  restrained orange outline and explicit instructional copy; reject invalid or
  busy drops through normal macOS drag behaviour.
- Progress copy should expose `completed of total`, elapsed time and the current
  item when useful. Final status should distinguish processed items, useful
  results, unsupported/unsuggested items and access errors. Do not invent ETA.
- Mechanical counter motion is a 120 ms settling transition on the true count,
  with a static update under Reduce Motion. VoiceOver receives the current value
  and periodic status rather than every visual transition.
- Cancel stops pending analysis and multi-file mutation between atomic operations.
  Copy must state what already happened and whether completed work is undoable.
- The tiny visible version belongs beside the display heading. The maker mark
  belongs quietly in the footer; text alone is an explicit temporary fallback
  only while the approved portrait asset is unavailable.

These are behaviour patterns learned from the real app. Extract source components
only after the second implementation demonstrates that code reuse is worthwhile.
