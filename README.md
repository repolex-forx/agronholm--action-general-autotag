# Repolex Knowledge Graph of agronholm/action-general-autotag

RDF knowledge graph data for [agronholm/action-general-autotag](https://github.com/agronholm/action-general-autotag), parsed by [repolex](https://repolex.ai).

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
rlex download agronholm/action-general-autotag
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 7d2ae9fb8015632ad3bfefecc0096368366e281d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 7d2ae9fb8015632ad3bfefecc0096368366e281d
│           └── chunk-001.nq.gz
├── blob
│   ├── 07c2592ac1cb8af723553fdfef8a62998d1f687b.nq.gz
│   ├── 2ba891f39c5fe321d366514586106aff3dfcd2f0.nq.gz
│   ├── 43d395e608c05d994ad9170e94774178d06a6b9c.nq.gz
│   ├── 608ee7f31a8cdfe2946430d91c84200e885d2e45.nq.gz
│   ├── 75e1cea3c519be7a59ca2debcc53c91a366344a0.nq.gz
│   ├── 7775d4e178f70db739147e3169769243b21a2284.nq.gz
│   ├── 7c0c456ca9c267fae8ec6af7ffb94f25f553900a.nq.gz
│   └── b4dda4853ea7a8414482fa3e146445cff8305db4.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 7d2ae9fb8015632ad3bfefecc0096368366e281d.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 15 files
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

[agronholm/action-general-autotag](https://github.com/agronholm/action-general-autotag)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
