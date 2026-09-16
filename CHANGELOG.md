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