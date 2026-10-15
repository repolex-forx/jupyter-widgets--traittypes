# Repolex Knowledge Graph of jupyter-widgets/traittypes

RDF knowledge graph data for [jupyter-widgets/traittypes](https://github.com/jupyter-widgets/traittypes), parsed by [repolex](https://repolex.ai).

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
rlex download jupyter-widgets/traittypes
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9a1db7c182bf2884110958303bc3f54f9ed8414f
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9a1db7c182bf2884110958303bc3f54f9ed8414f
│           └── chunk-001.nq.gz
├── blob
│   ├── 0ae3bbbbf2003d4933cb1124f250e5a0fe474b02.nq.gz
│   ├── 13917eb842f3ac65ba0b01337db6c8a295258177.nq.gz
│   ├── 16715e5190e6dba65439a7df38d6685822e7d021.nq.gz
│   ├── 1a061167aa6055c4abc0ca1a31de1e6f303a04ba.nq.gz
│   ├── 2b70a6f3cb432481f7c6303d342131fcf1b27700.nq.gz
│   ├── 4a10a611299ab72aa5960d43df58466b667d7f46.nq.gz
│   ├── 4c1cd4c1d6a1a54dd87df54cad5b480ceeb27ca8.nq.gz
│   ├── 59ed73bd4b9319005f15b666e5cafb797525da9e.nq.gz
│   ├── 5c39f4dc9ec76c5aa2681e64da374a4055e196f0.nq.gz
│   ├── 5c6311daf8ff59a9699c660d006da4dbccea8458.nq.gz
│   ├── 63abb4ad113a27ae279b7c72e06d931540423374.nq.gz
│   ├── 774c7ab05026ded7425dac433839dfbebb1e2aea.nq.gz
│   ├── 7b0e3a16456094b8952b914ef84eac8c9fd0ef6b.nq.gz
│   ├── 9095bd2f0ba12c6312233505060fa73899dc6c23.nq.gz
│   ├── a71b3b58b4dd8c5494fd9c653be309e73fee11ed.nq.gz
│   ├── bc55a3b607c12b777e508e560803f47d197c04eb.nq.gz
│   ├── c4161839cf3b713404076209e81b9973d0212745.nq.gz
│   ├── cd104bdbb145f110c40ee3fd9f27aa3be5c29244.nq.gz
│   ├── d2022a05e9fa05dd889b274ce748260a56f2c5b0.nq.gz
│   ├── d4c5b7701ef8a8bdbf73b82131fcc5eaebb265bd.nq.gz
│   ├── d6e1198b1ab1f5a7f19c6f1fc2ba7338438cf718.nq.gz
│   ├── e208369a23ee95b351be69480e032d721de82ed7.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ea0b9a783b99723404abf8dd1a972436c2f4f94d.nq.gz
│   └── f272bed833684018e5a3f2d8747c27fede656887.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9a1db7c182bf2884110958303bc3f54f9ed8414f.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 33 files
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

[jupyter-widgets/traittypes](https://github.com/jupyter-widgets/traittypes)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
