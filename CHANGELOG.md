## v0.12.0 — 2026-09-23

Copyright v0.12.0

## Changes since v0.11.0

- perf(dev): scope the tailwind class scan, and one splash watchdog for every profile
- refactor(boot): fold the watchdog gate snapshot into the transition
- fix(boot): stop the splash watchdog firing on a cold dev boot
- build: pin Rust to 1.98.1 locally and in CI
- fix(pdf): use as_chunks for UTF-16 decoding
- chore(just): rename go-live recipes to release / release-local
- perf(dev): static splash, and stop Vite watching src-tauri/target
- chore(dev): give this app its own dev port, 41431
- chore: sync the lockfiles to 0.11.0
- docs(spec): mark the copy editor implemented
- docs: format this branch's design spec
- fix(ui): keep the copy editor's ink on paper in dark mode
- refactor: share segmentCss between the two text-area renditions
- refactor: drop a text area's legacy pattern string from both models
- docs: mirror Task 22's browser check and what it caught into the plan
- fix(ui): mount completion popups inside the copy editor dialog
- test(harness): add a browser mount for the copy editor dialog
- docs: mirror Task 21's wiring into the plan
- fix(ui): clear the copy editor flag on an implicit dialog unmount
- feat(ui): open the copy editor from the inspector and by double-clicking a text area
- docs: mirror Task 20's inspector section into the plan
- fix(ui): resolve the copy-region label collision, keyboard and duplicate state machine
- feat(ui): show a text area's copy read-only in the inspector, with a way into the editor
- docs: mirror Task 19's dialog and the retargeting fix into the plan
- fix(ui): stop useFiltersAt from retargeting onto an adjacent chip
- fix(ui): cover useFiltersAt's own-edit cases and move it to its own file
- feat(ui): add the copy editor dialog, one undo step per session
- docs: mirror Task 18's committed preview into the plan
- feat(ui): preview a text area's resolved copy in its styles
- docs: mirror Task 17's second fix round into the plan
- fix(ui): keep a pressed toolbar toggle legible in dark mode and cancel colour cleanly
- docs: mirror Task 17's fix round into the toolbar and schema blocks
- fix(ui): keep the transformer popover live and the chip selected across its edits
- docs: mirror Task 17's committed toolbar into the plan
- feat(ui): add the copy editor's toolbar
- docs: mirror Task 16's fix round and hand Task 19 the popover's position
- fix(ui): let a field's popover name and clear a blank column, and harden its focus
- docs: mirror Task 16's committed popover and tests into the plan
- docs(spec): record the { completion's remaining edge over unpaired prose
- feat(ui): draw fields as chips and edit their transformer chains
- docs: mirror Task 15's committed completions and note the popup's stacking
- fix(ui): close the { completion over prose and pin both triggers end to end
- docs: mirror the committed suggestion renderer into Task 15
- docs: make the plan's columnItems agree with its own tests
- feat(ui): complete columns after { and transformers after | in the copy editor
- fix(ui): reject a non-Color or blank size when parsing pasted copy
- docs: mirror the paste-safe schema into Task 14's code blocks
- fix(ui): carry the copy editor's object attrs through HTML so paste keeps them
- test(ui): pin that the rich-doc bridge never writes an empty text node
- feat(ui): add the copy editor's schema and editor hook
- docs(spec): record that the editor's marks cannot express bold: false
- docs(ui): say what the rich-doc bridge drops and why its marks are trusted
- docs: point Task 14's stubs at the tasks that flesh them out
- feat(ui): bridge a text area's rich content to a ProseMirror document
- docs(ui): say which engine mode a text area's markup fallback would hit
- docs: name the test files tsc caught in Task 12 and the dead mock arm Task 23 removes
- test(ui): pin the rich resolution's identity and name what the preview resolves
- feat(ui): lay text areas out from Rust's resolution of their rich content
- refactor(app): tighten the rich-resolution docs and pin pre-flight reports once
- feat(app): resolve rich text areas for the editor and pre-flight their fields
- docs: hand Task 11 the pre-flight leftovers from Task 10's review
- test(generate): pin inline emphasis and a styled field's colour and face
- perf(generate): borrow the lines for the emphasis fact before measuring
- docs: add Task 10's newline-split guard step and the CRLF follow-up
- feat(generate): lay text areas out from their rich content
- perf(generate): skip the newline split when no segment carries one
- refactor(model): move the model tests into their own file
- docs: record that a cell's own newlines become lines in the rich resolver
- fix(generate): give a cell's own newlines lines of their own
- feat(generate): resolve a text area's rich content into styled lines
- test(layout): pin the surviving literal beside an empty segment's face
- docs: name the request's font method correctly in the design
- docs(layout): say why a segment's face is will-use as policy, not fact
- docs: point Task 12 at the task that closes the window and stage columnDrop.ts
- feat(layout): count a segment's face among a request's will-use fonts
- test(layout): pin segment boundaries in multi-byte copy
- docs: complete Task 6's staging line in the plan
- feat(layout): attribute selector rules under a segment's own style
- refactor(ui): free the Segment name for the request's styled copy
- docs: list the request literals Task 6 found outside the layout crate
- feat(layout): let a request carry styled segments
- docs: note the expand/contract split in the design and pre-empt model.rs's size
- fix(model): always write a filter's args and pin the migration order
- docs: record the column-drop helpers' move out of model.ts in the plan
- feat(model): carry a text area's copy as a rich tree beside its pattern text
- refactor(model): move the column-drop helpers into their own module
- docs: settle the plan on an empty rich text being one line
- fix(model): make an empty rich text one line and drop a dead arm
- chore: refresh the layout-wasm lock for domain's pattern dependency
- feat(model): add the rich text tree a text area's copy becomes
- docs: have the plan's contract stage name the third shared-source file
- fix(pattern): badge a half-built transformer and tighten the catalog guard
- docs: match the plan's sentence-case doc comment to the shipped wording
- feat(pattern): publish the transformer catalog to both languages
- docs: settle the plan's case-filter rules on a word's first letter
- fix(pattern): capitalise the first letter of a word, not its first character
- feat(pattern): add sentence and title case filters
- docs: route the plan's filter work to the pattern crate's new module
- docs(pattern): state what field_source can and cannot round-trip
- refactor(pattern): move filter application into its own module
- feat(pattern): give filters a structured form beside the string grammar
- docs: plan the textarea copy editor
- docs: design the textarea copy editor


## v0.11.0 — 2026-09-22

Copyright v0.11.0

## Changes since v0.10.0

- refactor(release): share the signing environment between the two builders
- refactor(release): one script, two endings for the release paths
- feat(fonts): offer every installed face, picked by family like the font panel
- chore: refresh the layout-wasm lockfile for 0.9.0


## v0.10.0 — 2026-09-16

Copyright v0.10.0

## Changes since v0.9.0

- docs: correct the release notes on the CI path and tag annotations
- fix(release): keep Markdown headings in the local path's tag annotation


## v0.9.0 — 2026-09-16

Copyright v0.9.0

## Changes since v0.8.0

### Colour picker
- A colour picker popover opens from the inspector, with a saturation square,
  a hue strip and hex entry.
- The picker offers the colours the document already uses.
- Dragging in the picker no longer strands an undo gesture.

### Inspector
- The inspector is now organised into named, foldable sections.
- Numeric fields can be emptied — clearing one sets it to no value rather
  than snapping back.
- A bound record's text is shown in the inspector.

### PDF output
- Output is now a single format: the layered PDF.
- A frame can pick its PDF layer, defaulting from preferences; layers are
  emitted as named optional-content groups, and overlap across layers warns.
- PDF output settings live on the template (schema v6): intent, ICC profile
  and document metadata.
- Metadata patterns resolve per variant, and the preview agrees with the
  engine.
- A PDF/X-4 claim the file cannot honour is refused rather than written.
- A TrimBox is derived from the visible page for a base that has none.
- Embedded fonts are named by their own PostScript name.

### Output file naming
- Output files are named from a pattern saved on the template (schema v5),
  edited in the toolbar's naming dialog.
- Resolved names are sanitized into safe paths, and collisions are refused
  before anything is written.

### Text
- Text area copy can be composed from spreadsheet columns with pattern text.

### Fixes and performance
- Toolbar hover text stays legible in dark mode.
- The live layout pass is keyed on what the engine is actually given,
  cutting redundant re-layout.


## v0.8.0 — 2026-09-01

Copyright v0.8.0

- fix: satisfy the 1.98 chunks_exact lint in barcode and pdf
- feat(ui): adopt the Lightbox visual language


## v0.7.3 — 2026-09-01

Copyright v0.7.3

First release built, signed and published by CI.

- feat: vendor the barcode crate as copyright-barcode, dropping the last path
  dependency on a sibling stencil checkout. That dependency broke
  `cargo metadata` on any machine without stencil beside copyright, which kept
  the rust job in checks.yml red and killed the v0.7.1 build.
- fix: read Copyright's own release secrets rather than lightbox's. The token
  inherited from lightbox is scoped to lightbox-releases, which is what
  refused the v0.7.2 publish after a clean signed build.
- ci: verify the tag against all three manifests, not package.json alone
- ci: stamp a versioned CHANGELOG entry into the releases repo before
  publishing, so /releases/latest orders by a distinct commit date
- ci: assert every signing and notarization secret is present up front
- ci: digit-anchored tag filter, per-tag concurrency, workflow_dispatch
  escape hatch, --locked builds