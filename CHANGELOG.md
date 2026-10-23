# Changelog

All notable changes to this standalone edition of markitdown are documented in this file.

## v1.1.0 — Standalone enhancements (2026-10-20)

- Converted the repository from a fork into a standalone edition with its own history, keeping full upstream credit.
- Added an "About This Standalone Edition" section to `README.md` with the upstream link, base-version provenance, and credit.
- Added `ENHANCEMENTS.md` documenting everything changed in this edition.
- Extended the upstream `.github/dependabot.yml` (its GitHub Actions entry, including the 7-day cooldown, kept as-is) with weekly pip updates for `packages/markitdown`, `packages/markitdown-mcp`, `packages/markitdown-ocr` and `packages/markitdown-sample-plugin`.
- Added markdown linting automation (`.markdownlint.json` and the Markdown check workflow) for the docs; the check was later scoped via `.markdownlint-cli2.yaml` so it covers this edition's own documentation instead of failing on upstream content. Upstream's `tests.yml` and `pre-commit.yml` workflows were kept as-is — no duplicate Python CI added, since the upstream test workflow already runs the real test suite.
- Added `.editorconfig` with standard editor settings (UTF-8, LF, 2-space indent).

## v1.0.0 — Upstream baseline (2026-10-20)

- Clean standalone baseline of [microsoft/markitdown](https://github.com/microsoft/markitdown) at upstream release v0.1.8 (snapshot commit `4cc9fa17653d695d64fb9eee5b33d4de55ff84e8`, upstream HEAD dated 2026-10-03).
- Fork history severed; all files and the MIT licence (`LICENSE`) preserved as-is, including all binary test fixtures under the packages' test folders.
