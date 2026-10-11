# Repolex Knowledge Graph of pallets-eco/flask-orjson

RDF knowledge graph data for [pallets-eco/flask-orjson](https://github.com/pallets-eco/flask-orjson), parsed by [repolex](https://repolex.ai).

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
rlex download pallets-eco/flask-orjson
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4e9ee0e46da6034b6e754f2e538c740c654bad17
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 4e9ee0e46da6034b6e754f2e538c740c654bad17
│           └── chunk-001.nq.gz
├── blob
│   ├── 099b123cc590e3735e4120a210c984aaa89971e7.nq.gz
│   ├── 0f433a047c73565c67a1eb48cb93c3879215e9a4.nq.gz
│   ├── 2f1b482e402cecfd58a9388bfcf06eb9d2358108.nq.gz
│   ├── 2ff985a67af35fdfd1076354b771c425867cdab4.nq.gz
│   ├── 31aa58ee5a8d72304575f4d818cbb0e3ae4e8512.nq.gz
│   ├── 35e705c5abf566a1ae72137eeb3fab13e89629b3.nq.gz
│   ├── 422f0cceef6c300501c16b3c7c8e735a06c57129.nq.gz
│   ├── 5f522c22204b689033f69e581c007bc1e1d73774.nq.gz
│   ├── 68ba5f6eb4f42281ecb27a2488370a5f044c8022.nq.gz
│   ├── 6e372429c2465e45dcb1c31a898d4f76731f3e17.nq.gz
│   ├── 71d3db72614f347bfdad95a39e0749f7e99ea30a.nq.gz
│   ├── 8441e5a64f3bdd680c9d67e8b44c9f176d2a351b.nq.gz
│   ├── 855f4dd62792d44051a757d74e2c36f8cac93b4b.nq.gz
│   ├── 93d2b317a243b1b555b157d0241612ab2804663a.nq.gz
│   ├── 97370978f8d73ba8e0c6b103b8fa5c83db5e91a6.nq.gz
│   ├── 992cd796e64a8787faebb7264867896867024a2b.nq.gz
│   ├── a711b9a7bd7369ba90860e72cbd79e1a6c7bfdb9.nq.gz
│   ├── acbd83f90b38e208b211fc7e62366556e9565dd8.nq.gz
│   ├── b9657a44c4b9e80ccdaf2a5fe2710849447ff192.nq.gz
│   ├── cf4483a25742a594abaf865445d3ffa7aeeea27f.nq.gz
│   ├── e4d8146b20f9dcc29d566165cce7758710dd775d.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eda8c518a76e6d8e02e166c2cf2eaec3a8a1bb09.nq.gz
│   └── f58a02ca7d3f4b334edfa38185d454c06c7d44bd.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 4e9ee0e46da6034b6e754f2e538c740c654bad17.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 31 files
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

[pallets-eco/flask-orjson](https://github.com/pallets-eco/flask-orjson)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
