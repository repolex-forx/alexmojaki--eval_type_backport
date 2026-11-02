# Repolex Knowledge Graph of alexmojaki/eval_type_backport

RDF knowledge graph data for [alexmojaki/eval_type_backport](https://github.com/alexmojaki/eval_type_backport), parsed by [repolex](https://repolex.ai).

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
rlex download alexmojaki/eval_type_backport
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 154aa07f564bb1c4335838f69fe6399d14e5c073
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 154aa07f564bb1c4335838f69fe6399d14e5c073
│           └── chunk-001.nq.gz
├── blob
│   ├── 347588dc76a1bd471df37df9dd92e900e86ac798.nq.gz
│   ├── 42eb4101e514e6e82ecd5111fe09e81a786de694.nq.gz
│   ├── 4489ba73d6464102d91968f89e9f33a136b74f4d.nq.gz
│   ├── 460a46ef29240d20e824f213d9f00a1dbe124527.nq.gz
│   ├── 53f1c5a98f9d516a6fc0c8ab41964de466c1fdad.nq.gz
│   ├── 5c73f19e45cfd67634c0fe8ec5e07f862a5ea33d.nq.gz
│   ├── 6eb895e561921be777f6f034b85ddcef9b5caf8b.nq.gz
│   ├── 909f939c642d55b5c392bc01c5f6c44700047928.nq.gz
│   ├── 9853426ea790bdba794d57405d2ebf43ea719d97.nq.gz
│   ├── b1664f84f6bf86953215a3930efe3fbed010c325.nq.gz
│   ├── bd47ad19a5ff84ceb703d7afc9cfcafa650bc1f0.nq.gz
│   ├── ccfd3c392722c8422cb491f843206e7a735fb2bf.nq.gz
│   ├── d2ab05b35a4baf3a95cadff1d21c64afcfaadf64.nq.gz
│   ├── d60cc3bbec68ea9d4329c8fca3eef690adf01454.nq.gz
│   ├── e5b155af0ed4a62d7fd54e2a5da0a1a61146414e.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 154aa07f564bb1c4335838f69fe6399d14e5c073.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 24 files
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

[alexmojaki/eval_type_backport](https://github.com/alexmojaki/eval_type_backport)

---
*Parsed on 2026-11-02 by [repolex](https://repolex.ai)*
