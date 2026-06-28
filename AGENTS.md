# MarkItDown — Fork for professahx-code

**Upstream:** microsoft/markitdown (MIT License)
**Fork URL:** https://github.com/professahx-code/markitdown
**Integration Skill:** Infrastructure/Skills/markitdown/SKILL.md

## Purpose

Forked to integrate MarkItDown into the Zo Computer content pipeline as a universal document-to-markdown converter. All modifications are additive — we don't alter upstream core.

## Integration Files (in Zo workspace, not in this repo)

| File | Purpose |
|------|---------|
| `Infrastructure/Skills/markitdown/SKILL.md` | Skill definition — CLI, Python API, MCP server |
| `Infrastructure/Skills/markitdown/scripts/markitdown-convert.ts` | Bun CLI wrapper |
| `Infrastructure/Skills/markitdown/scripts/markitdown-pipeline.ts` | Batch conversion script |
| `Infrastructure/Skills/markitdown/scripts/markitdown-service.sh` | MCP lifecycle manager |
| `Infrastructure/Identity/Operations/PGIPR-MARKITDOWN-2026-06-28.md` | PGIPR analysis |

## Use Cases

1. **Content Pipeline** — Convert client deliverables (DOCX, PDF, XLSX) to markdown before AI processing
2. **Research Pipeline** — Convert PDF reports and EML attachments to markdown for research index ingestion
3. **Intel Pipeline** — Convert email attachments (EML/MSG) to markdown for keyword scanning
4. **Agent Tooling** — MCP server exposes `convert_to_markdown(uri)` as a Zo tool for any agent
5. **Batch Ingestion** — Pipeline script handles bulk directory conversion with directory-tree mirroring

## Version

Tracking upstream v0.1.6 (May 26, 2026). Merge upstream periodically for bug fixes and new converters.
