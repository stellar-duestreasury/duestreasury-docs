# Guide for signers

Read the selected group and proposal before signing. `propose` requires a designated signer, positive atomic-unit amount, destination, and a bytes32 hash of an off-chain description. The app accepts the SHA-256 hash, never free-form spending descriptions. Creating a proposal does not count as approving it.

Each distinct designated signer calls `approve` once. Anyone may call `execute` when approvals reach the fixed threshold and recorded group balance covers the amount. Execution closes the proposal before transferring; host failure rolls back both status and accounting.

The proposer may cancel directly. Threshold cancellation takes a unique list of group signers who each separately authorize cancellation. Spending approvals are not cancellation consent. The browser exposes proposer cancellation only: coordinating threshold cancellation needs reviewed multi-party authorization tooling. A lost signer key can permanently block spending.

See `threshold_lifecycle_preserves_accounting_after_every_step`, `proposer_and_explicit_threshold_can_cancel`, and authorization/error tests in contract `src/test.rs` and `src/error_paths.rs`.
