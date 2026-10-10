# Repolex Knowledge Graph of tiangolo/latest-changes-app

RDF knowledge graph data for [tiangolo/latest-changes-app](https://github.com/tiangolo/latest-changes-app), parsed by [repolex](https://repolex.ai).

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
rlex download tiangolo/latest-changes-app
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a9c141236754e1de7496f44302e02c5527a1bfa5
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── a9c141236754e1de7496f44302e02c5527a1bfa5
│           └── chunk-001.nq.gz
├── blob
│   ├── 00bdb878e61dd4a525f867b4f024cc8c426ad76e.nq.gz
│   ├── 02ae4470144e53742759d50e6b66ecaab579b02c.nq.gz
│   ├── 04be4e66201f215da97314a42a20dea9e39d470a.nq.gz
│   ├── 1690fd6fed5ff116a1cfc6184e18fde0eb762fd7.nq.gz
│   ├── 1d449edf7b23aba21047b1cd65103f4fec3a5dd7.nq.gz
│   ├── 25a7da6494655a39a9d630bd660a853e662c7cf4.nq.gz
│   ├── 4dd3469bc81a18ed19472897ed0b985f60b27af1.nq.gz
│   ├── 4e8ce8015d6864f86658ece9a8d62c2439e6701a.nq.gz
│   ├── 4f93e1bd0c20bbba741a6a0d4e8de731889b7dd4.nq.gz
│   ├── 5473b12c4a15ac44ca89b187e6b49ae32236abd9.nq.gz
│   ├── 56faf8029689503990b7cf5b52b9a003a19ac485.nq.gz
│   ├── 5c08e9ac40f72c5001758383188e60736cb320f2.nq.gz
│   ├── 6324d401a069f4020efcf0ff07442724b52f47c2.nq.gz
│   ├── 642cd6760aa9add906e338720b42e3f5b04aa3da.nq.gz
│   ├── 670f5c10a6b516ce382111526ae39cae9373bc87.nq.gz
│   ├── 6b8f7a8e45e86ebd7876330bdf689cb2b7ed0700.nq.gz
│   ├── 8938170b50350f5d2f7728f1cf7882b875ecd90e.nq.gz
│   ├── 8dc006060a91211097221b51302dfa60d1fee337.nq.gz
│   ├── 9a3615dde623fc365fc82c238e7a7fe314e6b855.nq.gz
│   ├── 9a824413e2ac5dc63da7b8b258cf2c31b8205448.nq.gz
│   ├── 9be5cba851151ae0eaed7aea5da56bb018dc7761.nq.gz
│   ├── a83f2c0a8897967c9b116d62d70b8c0ca0d98d64.nq.gz
│   ├── ab691199d2e4f6fb95883a26c9406c4a58d7e564.nq.gz
│   ├── ac3154dd6ec59bc83ca008a770a93e0f053714d4.nq.gz
│   ├── bd30510f121b4675e9f2092bcdd0682933b49032.nq.gz
│   ├── c27ba54b8c6e437aa260e7b0b91aeaaccb670103.nq.gz
│   ├── c8d325d9057545968fc198c8805613ddbd618278.nq.gz
│   ├── ca3c2467dde78e00839895c22386b4392f8fcd5a.nq.gz
│   ├── d266c16c124fd55f2fefa85969ba38fc55bb724e.nq.gz
│   ├── d7db364d213b0fb6ec4ebdca16fd27c6e73c4ab9.nq.gz
│   ├── dbc21f648922b954e29ec216f07e8be3554d02e2.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── a9c141236754e1de7496f44302e02c5527a1bfa5.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 39 files
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

[tiangolo/latest-changes-app](https://github.com/tiangolo/latest-changes-app)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
