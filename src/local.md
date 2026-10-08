# Run locally

Contract: Rust with wasm32v1-none, SDK 28.0.0, Stellar CLI 28.1.0. Run `cargo fmt --all --check`, `cargo clippy --all-targets -- -D warnings`, `cargo test --locked`, `node --test`, `node scripts/check-errors.mjs`, and `stellar contract build`. On Windows GNU use the existing MinGW linker on PATH.

App: `npm ci`, then `npm run lint`, `npm run typecheck`, `npm test -- --maxWorkers=1`, and `npm run build`. Copy `.env.example` to `.env.local` and configure testnet/RPC/contract/explorer values only after the deployment gate is satisfied. Until then the app shows configuration guidance and refuses wallet operations. `npm run dev -- --host 127.0.0.1` starts the local interface.

Book: `node --test` and `node scripts/check-links.mjs`. mdBook compilation is configured in CI; it has not been verified locally unless noted in the verification record.
