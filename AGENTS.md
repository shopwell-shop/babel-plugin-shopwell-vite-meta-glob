# Shopwell repository rules

This repository is an independently maintained Shopwell npm dependency fork. Every AI
coding agent must read this file before changing files in this repository.

## Hard rules

- Preserve UTF-8 and existing user changes.
- Shopwell-owned code and publishable packages use Apache License 2.0.
- Every project-owned package manifest must declare `Apache-2.0`.
- Root `LICENSE` contains the standard, unmodified Apache License 2.0 text.
- Original upstream legal text remains verbatim in root `NOTICE`; do not brand,
  shorten, or move it into `LICENSE.upstream-*` files.
- Do not merge or cherry-pick unrelated upstream history, copy upstream tags, or force-push.
- Runtime code and workflows must not depend on `shopware/*`, `shopwarelabs/*`,
  `@shopware-ag/*`, or their GitHub repositories.
- Before commit, push, release, or sync completion, run:
  `../sync-upstream/bin/syncctl audit-license babel-plugin-shopware-vite-meta-glob` and
  `../sync-upstream/bin/syncctl audit-upstream-dependencies babel-plugin-shopware-vite-meta-glob`.
- A failed audit blocks commit, push, release, and sync completion.
