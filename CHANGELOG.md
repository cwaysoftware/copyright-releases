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