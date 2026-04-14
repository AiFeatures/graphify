# graphify

## Project
- **Name**: graphify
- **Org**: AiFeatures (iAiFy)
- **Language**: Python
- **Description**: AI coding assistant skill that reads files, builds a knowledge graph, and reveals codebase structure. Supports 19 languages via tree-sitter AST. Fully multimodal (code, PDFs, markdown, images).

## Build / Test / Lint
- Install: `pip install -e .`
- Test: `pytest`
- Lint: `ruff check .`
- Format: `ruff format .`

## Conventions
- Default branch is `v3`
- PyPI package name: `graphifyy`
- Requires Python >= 3.10
- Conventional Commits

## CI/CD
- Uses shared workflows from `Ai-road-4-You/enterprise-ci-cd`
