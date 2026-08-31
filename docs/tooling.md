# Project Tooling

The `flow` project is initialized for the following local development tools.

## Tools

| Tool | Project setup | Use |
| --- | --- | --- |
| ripgrep | Available on `PATH` | Fast text and file search |
| ast-grep | Available on `PATH` | Structural search for supported source files |
| Serena | `.serena/project.yml` with Markdown support | Project-aware language-server navigation |
| Graphify | `graphify-out/` | Repository knowledge graph and documentation relationships |
| Context7 | Registered globally | Current third-party library and API documentation |

## Health Checks

Run the checks that match the tool you are using:

```powershell
serena project health-check .
graphify --help
```

Serena's health check should find a Markdown file and successfully query its symbols. `rg` and `ast-grep` are command-line tools and can be checked with their version commands above. Context7 is an MCP integration and is verified by resolving and querying documentation for an external dependency when one is introduced.

## Verification

Run these commands from the repository root to verify the local tools:

```powershell
rg --version
ast-grep --version
serena --version
graphify --version
```

Serena uses `.serena/project.yml` for the project name, encoding, workspace root, and ignore behavior. Its generated cache and memories are ignored by Git.

Graphify stores its generated graph under `graphify-out/`, which is also ignored by Git. To build or refresh the graph:

```powershell
graphify extract .
graphify update .
```

For this documentation-only project, Graphify needs a semantic-extraction provider to create a document graph. When the local Claude CLI is available, use:

```powershell
graphify extract . --backend=claude-cli
```

Without a provider, the tool can still be checked without changing the repository with:

```powershell
graphify --help
```

Context7 is provided through the globally registered MCP server. Use it for external library, framework, SDK, API, and CLI documentation; keep project-specific facts in this repository's documentation.

## Search Guidance

- Use `rg --files` and `rg` for fast text and file searches.
- Use `ast-grep` when the search depends on code structure rather than exact text.
- Use Serena for symbols, references, and language-aware navigation.
- Use Graphify queries for relationships across project documents when `graphify-out/graph.json` exists.

## Maintenance

Keep `.serena/project.yml`, `.claude/settings.json`, and this guide aligned when tooling changes. Do not commit `.serena/` caches, Graphify output, API keys, or machine-specific executable paths.
