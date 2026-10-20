# Liquid Loom — safe adoption beats clever build tooling

[Source](https://github.com/yotamon/Liquid-Loom) · [First-project guide](https://github.com/yotamon/Liquid-Loom/blob/main/docs/FIRST_PROJECT.md) · [Validation plan](https://github.com/yotamon/Liquid-Loom/blob/main/docs/VALIDATION.md) · [Back to my profile](../README.md)

## The problem
Shopify Liquid's native theme directory format works for deployment, but a growing team may want feature-oriented source ownership, modern asset tooling, diagnostics and safe migrations. Forcing a rewrite just to introduce tooling would increase risk for merchant sites.

## Key design choices
- **Dual source, one deployable theme:** existing native Shopify files and new feature-organized files can coexist, then compile to standard Shopify theme output.
- **One output, one owner:** conflicting paths fail with diagnostics. There is no silent 'last writer wins' behavior.
- **Transactional publishing:** assemble in isolation; failed builds leave the previous deployable output intact.
- **Migration preview:** a developer can inspect what would move before any source change, preserving Shopify output identity.
- **Native-by-default:** Vite and Tailwind are optional, not mandatory new runtime dependencies.
- **Explainable structure:** deterministic ownership/dependency information is usable by humans, CI and coding agents without inventing dynamic Liquid relationships.

## Evidence available
- Documented CLI, install instructions and Shopify-compatible output.
- CI covering tests, packed-package installs, fresh scaffold and existing-theme hybrid adoption.
- Release validation document records npm Trusted Publishing and release automation.
- [Real development-store verification](https://github.com/yotamon/Liquid-Loom/issues/13) and [external developer sessions](https://github.com/yotamon/Liquid-Loom/issues/14) are still open.

## Honest adoption status
A passing fixture or registry release is **not** the same as successful use on a merchant store. I do not claim time savings or community adoption without paired measurements or independent users.

## Next evidence
1. Install a published package from the public registry in both new/existing theme flows.
2. Preview those themes in a real Shopify development store.
3. Observe three independent developers attempting a real change.
4. Compare original and new workflows on the same machine/theme; capture friction and failure outcomes.

**Interview discussion:** determinism, migration strategy, build transactionality, developer experience, avoiding ecosystem lock-in and when not to add abstraction.
