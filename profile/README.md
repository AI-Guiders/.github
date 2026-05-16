# AI-Guiders

**Open tools for agent-first .NET work** — IDE, MCP servers, and shared libraries so humans and coding agents share the same observable ground truth (build, tests, git, Roslyn, memory).

| | |
|---|---|
| **Handbook** (mission, values, how we work) | [handbook wiki](https://github.com/AI-Guiders/handbook/wiki) · [repo](https://github.com/AI-Guiders/handbook) |
| **Public knowledge slice** (CC BY-SA) | [kb-public](https://github.com/AI-Guiders/kb-public) |
| **Org site** (EN/RU) | [ai-guiders.github.io](https://ai-guiders.github.io/) |
| **Writing & project cards** | [karataevdmitry.github.io](https://karataevdmitry.github.io/) |

---

## Open stack (start here)

### IDE & agent surface

| Project | What it is |
|---------|------------|
| [**cascade-ide**](https://github.com/AI-Guiders/cascade-ide) | Agent-, keyboard-, C#-first IDE (Avalonia, .NET 10). Cockpit-style attention model, in-proc MCP, chat. MIT. |
| [**agent-notes-mcp**](https://github.com/AI-Guiders/agent-notes-mcp) | MCP 2.0: hot context, `knowledge/`, routing, localhost status — one TOML config (`--config`). MIT. |
| [**AIGuiders.AgentNotes.Core**](https://github.com/AI-Guiders/AIGuiders.AgentNotes.Core) | Shared storage & routing library (MCP + IDE). NuGet. MIT. |
| [**kb-public**](https://github.com/AI-Guiders/kb-public) | Published read-only KB for agents (playbooks, integrity kernel). Content **CC BY-SA**; not the full private canon. |

### C# toolchain (MCP parity)

Same facts in the IDE and in Cursor/Claude via MCP — not a second story in chat.

| Project | Role |
|---------|------|
| [**RoslynMcp**](https://github.com/AI-Guiders/RoslynMcp) | Diagnostics, code actions, go-to-definition, rename, solution structure |
| [**dotnet-debug-mcp**](https://github.com/AI-Guiders/dotnet-debug-mcp) | DAP debugging (breakpoints, steps, variables) |
| [**dotnet-build-test-mcp**](https://github.com/AI-Guiders/dotnet-build-test-mcp) | Structured `dotnet build` / `dotnet test` |
| [**git-mcp**](https://github.com/AI-Guiders/git-mcp) | Git status, diff, logical commits |
| [**hybrid-codebase-index**](https://github.com/AI-Guiders/hybrid-codebase-index) | Hybrid FTS + optional semantic index (SQLite) |

### Shared libraries & utilities

| Project | Role |
|---------|------|
| [**git-mcp-core**](https://github.com/AI-Guiders/git-mcp-core) | Shared git argv (IDE + git-mcp) |
| [**hybrid-codebase-index-core**](https://github.com/AI-Guiders/hybrid-codebase-index-core) | Index core (NuGet) |
| [**dotnet-debug-core**](https://github.com/AI-Guiders/dotnet-debug-core) | Debug session core |
| [**dotnet-build-test-parsers**](https://github.com/AI-Guiders/dotnet-build-test-parsers) | MSBuild/test output parsers (NuGet) |
| [**mcp-tool-manifest**](https://github.com/AI-Guiders/mcp-tool-manifest) | `mcp-tools.manifest.json` helpers |
| [**AIGuiders.DotnetTools**](https://github.com/AI-Guiders/AIGuiders.DotnetTools) | Small .NET utilities across repos |

### Capture & analysis (opt-in)

| Project | Role |
|---------|------|
| [**webcam-capture-mcp**](https://github.com/AI-Guiders/webcam-capture-mcp) | Webcam / screen / audio burst capture |
| [**webcam-analysis-mcp**](https://github.com/AI-Guiders/webcam-analysis-mcp) | Burst analysis, OCR, Whisper |
| [**webcam-mcp-shared**](https://github.com/AI-Guiders/webcam-mcp-shared) | Shared library for webcam MCPs |

### Learning & other

| Project | Role |
|---------|------|
| [**agent-first-learn**](https://github.com/AI-Guiders/agent-first-learn) | Course: designing with and for AI agents. MIT. |
| [**TInvestMcp**](https://github.com/AI-Guiders/TInvestMcp) | T-Bank Invest API (read-only MCP) |
| [**dotnet-mcp-templates**](https://github.com/AI-Guiders/dotnet-mcp-templates) | Templates for new MCP servers |

---

## Principles (short)

- **Parity** — if the agent can do it via MCP, the IDE should not contradict it.
- **Observable loop** — editor, tools, and agent stay in one legible contour ([cockpit attention model](https://karataevdmitry.github.io/writing/cascade-ide-attention-cockpit.html) in Cascade IDE).
- **Fail fast on config** — e.g. Agent Notes MCP requires explicit `--config` / TOML, no silent defaults to the wrong KB.

---

## Contribute

- **Issues & PRs** — in the relevant repo above.
- **Handbook** — org norms and boundaries: [handbook](https://github.com/AI-Guiders/handbook).
- **Security** — use each repo’s security policy if present; no secrets in issues.

---

## Licenses

| Kind | Typical license |
|------|-----------------|
| MCP / IDE / libraries code | **MIT** (per-repo `LICENSE`) |
| **kb-public** content | **CC BY-SA 4.0** (see repo `PUBLISHING.md`) |

Third-party notices live in individual repositories.

---

<p align="center"><sub>AI-Guiders · agent-first open stack for .NET</sub></p>

