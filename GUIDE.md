# Reader's Guide — markitdown

## What this project is

**MarkItDown** is Microsoft's lightweight Python utility for **converting
files to Markdown** — built for feeding documents to LLMs and text-analysis
pipelines. Unlike plain text extractors, it preserves the document structure
that matters in Markdown: headings, lists, tables, links and more. The output
is meant to be consumed by models (and is usually quite readable by humans
too), not to be a pixel-perfect rendition.

It currently converts from: PDF, PowerPoint, Word, Excel, images (EXIF
metadata and OCR), audio (EXIF metadata and speech transcription), HTML,
text-based formats (CSV, JSON, XML), ZIP files (iterating over the contents),
YouTube URLs, EPubs — and more.

## How the content is organised

- `packages/markitdown/` — **the core library and CLI**: the converter
  framework and one converter per format.
- `packages/markitdown-mcp/` — a **Model Context Protocol server** wrapping
  MarkItDown, so MCP-compatible AI tools can call the conversion directly.
- `packages/markitdown-ocr/` — the **OCR plugin** for image-based content.
- `packages/markitdown-sample-plugin/` — a reference plugin showing how
  third-party converters plug into the framework.
- [`README.md`](README.md) — the manual: **Why Markdown?**, Prerequisites,
  Installation, and a Usage chapter covering the Command-Line interface,
  Optional Dependencies, Plugins, Azure Content Understanding, Azure
  Document Intelligence, the Python API, and Docker — plus the security
  considerations the project flags prominently (MarkItDown reads with the
  privileges of the calling process, so inputs should be sanitised).
- Root extras: `Dockerfile` for the container route, `SECURITY.md`,
  `SUPPORT.md`, `CODE_OF_CONDUCT.md`.

## How to use it

1. Install per the README (Python, with `uv pip install` in a virtualenv) and
   add the optional dependencies for the formats you need.
2. Convert a file from the command line, or from Python through the API —
   choosing the narrowest `convert_*` entry point for your case, as the
   README's security note advises.
3. For AI-tool integration, run the `markitdown-mcp` server instead; for
   scans and photos, enable the OCR plugin.

## About this standalone edition

This repository is a standalone edition of
[microsoft/markitdown](https://github.com/microsoft/markitdown), converted
from a fork into its own repository and enhanced in place. See
[`ENHANCEMENTS.md`](ENHANCEMENTS.md) for what this edition adds and
[`CHANGELOG.md`](CHANGELOG.md) for its version history (v1.0.0 upstream
baseline, v1.1.0 enhancements). All original work belongs to Microsoft and the
upstream contributors; licence MIT (see `LICENSE`).
