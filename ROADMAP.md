# Roadmap

What is next for `duestreasury-docs`, in order. Anything not listed as done is
**not implemented**.

## Status

- [x] Repository governance: AGENTS.md, CONTRIBUTING.md, ROADMAP.md, LICENSE,
      .gitignore, .gitattributes (2026-10-01).
- [ ] v0 book, written from the real v0 contract code.

## Next

- [ ] mdBook configuration (`book.toml`) and `src/SUMMARY.md`.
- [ ] Pages written from the real contract code once it exists: architecture
      with every claim pointing at a file, function or test; limitations;
      threat model (STRIDE, with honest "not applicable" entries); pilot
      playbook; PRD; a privacy page on what is and is not stored on-chain.
- [ ] Dependency-free link checker (`scripts/check-links.mjs`) with tests.
- [ ] CI (`docs.yml`): link check, checker tests, mdBook build.

## Contract scope the book describes

Set by `STELLAR-BUILD-PLAYBOOK-v3.md` section 7 (in
`~/Desktop/Drips/_reference/playbooks/`, confirmed 2026-10-02): a group
collects dues into a treasury and spends only when enough designated signers
approve; one payment per member per period; spending descriptions stay
off-chain as hashes. The book is still written from the real code once it
exists, not from the playbook alone.

Deliberately unimplemented in the v0 contract (section 7): membership changes
by proposal, proposal expiry, per-period spending limits, key rotation,
dissolution refunds, audit-trail export, property-based invariant tests.

## Decisions needed from Tim

1. **Build standard — decided (2026-10-02).** v3 section 7 scopes what the
   book documents; v4's doc set plus the schoolfees docs are the standard
   for how it is built (templates, AGENTS.md, CI, checkers).
2. **Second reviewer.** Name the second human reviewer required before any funded test.

## Explicitly out of scope

Mainnet deployment, investor or fundraising material, and any page that
describes a feature the code does not have.
