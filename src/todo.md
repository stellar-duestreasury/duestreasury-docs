# Limitations and verification

TODO(verify): deployed app/contract integration, real-wallet lifecycle, threshold multi-party cancellation tooling, screen-reader/manual device checks, and independent custody review. There is no deployment, funded test, pilot or audit. Local unit tests are synthetic host/client checks only.

Deliberately unimplemented: membership/signer changes, expiry, spending caps, rotation, dissolution refunds, historical arrears, proposal index/full history export, reminders, CSV export, multilingual UI and property-based tests. Draft issues exist in the contract repository.

The local app automated axe check disables color contrast because happy-dom cannot compute it; it does not establish full accessibility compliance. Source changes are uncommitted until the maintainer publishes them.

Local verification on 2026-10-08: app lint, strict typecheck, 46 unit/render tests across six files and production build passed. Isolated production browser fixtures at 320, 390 and 1280 px had no horizontal overflow and no automated WCAG axe violations; fixtures blocked network calls and made no contract invocation. The final main chunk is 780.98 kB (183.63 kB gzip), above Vite's warning threshold. The app lockfile audit has 19 unresolved findings (13 low, six moderate; zero high/critical). The book link checker passed 13 tests and resolved 18 relative links. mdBook compilation is configured in CI, not locally verified.

The contract passed fmt, all-target clippy with warnings denied, 32 Rust tests, nine Node checker tests and its 17-error synchronization check. CLI 28.1.0 built a 13,072-byte optimized Wasm with nine exports; checksum `265b4b71e2d15301226ca6d028a70b2677686e59194959bc8fa6935d7d3b7434`. This proves local compilation and synthetic tests, not a funded exercise or audit.
