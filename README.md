# Repolex Knowledge Graph of beeware/briefcase-macOS-app-template

RDF knowledge graph data for [beeware/briefcase-macOS-app-template](https://github.com/beeware/briefcase-macOS-app-template), parsed by [repolex](https://repolex.ai).

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
rlex download beeware/briefcase-macOS-app-template
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 140848a9556d83d2fa7e88138fe5b9dc59199582
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 140848a9556d83d2fa7e88138fe5b9dc59199582
│           └── chunk-001.nq.gz
├── blob
│   ├── 0e8ade5d6ce61b71dd04bd554b92a2e85442a1f0.nq.gz
│   ├── 13b092d8fb1ea141fd7aa39917867838bad82eb9.nq.gz
│   ├── 15a8810c305e2d9eb22e233d8a99b02351f8bb69.nq.gz
│   ├── 27b43d39d1c038a7bf7c8c5f26dd6b5f1b141417.nq.gz
│   ├── 31dccfdf7adeeedc0f94b2183b5c709aacb22288.nq.gz
│   ├── 38ccc26131a793d53c11af78ec104b8d30174b88.nq.gz
│   ├── 3b2f609a65fabb2a10691faa66339cde9787e979.nq.gz
│   ├── 475161993f1f18a1e1a2950ab4072437749675b2.nq.gz
│   ├── 58e6d181749620ed71467588f20049b3421628ee.nq.gz
│   ├── 7aca58c9c4f7e5361baea2ee6dd18237a65568ae.nq.gz
│   ├── 80deff1c4b16b80fcaeb47d43dbe24e9cfa65cb3.nq.gz
│   ├── 857047968d454fecd7428381d3f3429c7055d934.nq.gz
│   ├── 88d66807a814d1f9d13b30576f9e9e45ab1d9c3a.nq.gz
│   ├── b834affdddcf5014398ca9c16aafe3ea7f2d0422.nq.gz
│   ├── bc1f7a982ad7bcef54f5399b9a2fa3fd51ba77c8.nq.gz
│   ├── be2bd37eb31d4d31057de9baa0960ade7a7677d3.nq.gz
│   ├── bef17c1e8932f6c57dac4a0a4cd672caedf0f11e.nq.gz
│   ├── c2a7758c607dc29240bd4bf8e829b0494c0c9fdf.nq.gz
│   ├── c4d88e8173e484996f9c1fe716bd0fb7e4c8a73b.nq.gz
│   ├── d7d79ec7ba0cf483c6c5f6313cedae532be9b36d.nq.gz
│   ├── e3805e4e4afb4955455f087f831d1f91285116e3.nq.gz
│   └── fb058dba910dc15812cbc7d46a8a99488fd4da7c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 140848a9556d83d2fa7e88138fe5b9dc59199582.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
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

[beeware/briefcase-macOS-app-template](https://github.com/beeware/briefcase-macOS-app-template)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
