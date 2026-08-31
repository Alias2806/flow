# Project Tooling Guidance

This project is documentation-only. Use the available tools according to the task:

- Use `rg --files` and `rg` for fast text and file searches.
- Use `ast-grep` for structural searches when source files are added.
- Use Serena for Markdown symbols, links, diagnostics, and language-aware navigation.
- Use Graphify for relationships across project documents when `graphify-out/graph.json` exists.
- Use Context7 for current external library, framework, SDK, API, and CLI documentation.

Before broad repository exploration, check the Graphify graph when it exists. Use Serena for symbol-specific navigation rather than text search.

## Graphify

This project has a knowledge graph at graphify-out/ with god nodes, community structure, and cross-file relationships.

Rules:

- For codebase questions, first run `graphify query "<question>"` when graphify-out/graph.json exists. Use `graphify path "<A>" "<B>"` for relationships and `graphify explain "<concept>"` for focused concepts. These return a scoped subgraph, usually much smaller than GRAPH_REPORT.md or raw grep output.
- If graphify-out/wiki/index.md exists, use it for broad navigation instead of raw source browsing.
- Read graphify-out/GRAPH_REPORT.md only for broad architecture review or when query/path/explain do not surface enough context.
- After modifying project files, run `graphify update .` when a graph exists. For documentation changes, refresh semantic extraction with `graphify extract . --backend=claude-cli` when the local Claude CLI is available.

See [Project Tooling](docs/tooling.md) for setup and verification commands.
