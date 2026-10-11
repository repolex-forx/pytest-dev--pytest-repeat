# Repolex Knowledge Graph of pytest-dev/pytest-repeat

RDF knowledge graph data for [pytest-dev/pytest-repeat](https://github.com/pytest-dev/pytest-repeat), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download pytest-dev/pytest-repeat
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a84eaa91965a00af03d8c3576e5b0f32114a06c8
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── a84eaa91965a00af03d8c3576e5b0f32114a06c8
│           └── chunk-001.nq.gz
├── blob
│   ├── 101d6a7c6ee4e0cbba3b5e636f53d5913bd6feb7.nq.gz
│   ├── 157047d23fabff929c84cd635943f54f6771858a.nq.gz
│   ├── 1a3e9ddb295a496c103f80d503d10310d775bb6b.nq.gz
│   ├── 1e55f5dbf5d77dae745dca596e13babf6df79ebb.nq.gz
│   ├── 455872a0128b88cf418c40aa0f9b254d6cde3eb2.nq.gz
│   ├── 71e1f61e9828527a3414e1bd882b02838a4074f9.nq.gz
│   ├── 9c8fe599a55af2b6c73503c15f27a63b868ec9b9.nq.gz
│   ├── ad59222ccb82807bfcdf455b3f39e0944bdb88c1.nq.gz
│   ├── c454e6a6040da66664add6a1c5d4d9e453cf5365.nq.gz
│   ├── df3c3d2d6cba753321b6df187127cf620ca8eb06.nq.gz
│   ├── f89bb8a3368f305f113a3133b8cb59edaa3d2eec.nq.gz
│   └── fc16527d1703aa4b019e82e5ebf249780dcb3771.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── a84eaa91965a00af03d8c3576e5b0f32114a06c8.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 20 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[pytest-dev/pytest-repeat](https://github.com/pytest-dev/pytest-repeat)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
