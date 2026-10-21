# Enhancements — Standalone Edition Changelog

Upstream: <https://github.com/microsoft/markitdown>
Maintainer of this edition: Syed Mujtaba Abbas (@mujtbabbas)

## v1.1.0 — Enhancement release (2026-10-20)

- Added "About This Standalone Edition" section to README.md with upstream
  link, base version provenance, and credit.

- Added this changelog (ENHANCEMENTS.md).
- Extended the upstream .github/dependabot.yml (its GitHub Actions entry,
  including the 7-day cooldown, kept as-is) with weekly pip updates for
  packages/markitdown, packages/markitdown-mcp, packages/markitdown-ocr and
  packages/markitdown-sample-plugin.

- Added .markdownlint.json and .github/workflows/markdown-check.yml
  (markdown linting automation for the docs; upstream tests.yml and
  pre-commit.yml workflows kept as-is — no duplicate Python CI added, the
  upstream test workflow already runs the real test suite).

- Added .editorconfig (standard editor settings: UTF-8, LF, 2-space indent).

## v1.0.0 — Baseline (2026-10-20)

- Clean standalone baseline of microsoft/markitdown at upstream release
  v0.1.8 (snapshot commit 4cc9fa17653d695d64fb9eee5b33d4de55ff84e8,
  upstream HEAD dated 2026-10-03).

- Fork history severed; all files and the MIT licence (LICENSE) preserved
  as-is, including all binary test fixtures under the packages' test folders.
