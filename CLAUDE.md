# Graphify

AI coding assistant skill that builds knowledge graphs from codebases, docs, and images. Type `/graphify` in Claude Code, Codex, OpenCode, OpenClaw, or Factory Droid.

## Tech Stack

- **Language**: Python 3.10+
- **Package**: `graphifyy` on PyPI (CLI and skill command are `graphify`)
- **Default branch**: `v3`
- **Graph library**: NetworkX with Leiden community detection
- **AST parsing**: tree-sitter (19 languages)

## Project Structure

```text
graphify/           Core Python package
tests/              Test suite
pyproject.toml      Package config and dependencies
```

## Development

```bash
pip install -e ".[dev]"
pytest
```

## Key Concepts

- Two-pass extraction: deterministic AST pass + Claude subagent pass for docs/images
- Relationship tagging: EXTRACTED, INFERRED (with confidence), AMBIGUOUS
- Graph-topology clustering (Leiden), no embeddings needed
- Output: interactive HTML graph, GRAPH_REPORT.md, queryable JSON, SHA256 cache
- `.graphifyignore` for excluding paths (same syntax as .gitignore)
