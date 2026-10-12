# Repolex Knowledge Graph of scrapy/loginform

RDF knowledge graph data for [scrapy/loginform](https://github.com/scrapy/loginform), parsed by [repolex](https://repolex.ai).

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
rlex download scrapy/loginform
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e61facef4927a581a94bf4aebdd0609b4c1317c9
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── e61facef4927a581a94bf4aebdd0609b4c1317c9
│           └── chunk-001.nq.gz
├── blob
│   ├── 0e44105ca8e96f5628d5779183c0c0e925343ba2.nq.gz
│   ├── 2a3c9be20a1866d838e52ad603b1c47619c34a12.nq.gz
│   ├── 325877ea55d8a7c8c0ef03600cea2d4c657e285f.nq.gz
│   ├── 359ace7ddabdee505994febcf97dd5e3c0e87786.nq.gz
│   ├── 3c3f2cf7039ca2a0b22187ef3004d7f61ce11498.nq.gz
│   ├── 3cd2d84921fa90c08f44de4be75961f0e1291cfc.nq.gz
│   ├── 48723dc8f962757bf71da3016bb13c94b52bfe70.nq.gz
│   ├── 580da87bb333186862bc79bf72283b951485d48b.nq.gz
│   ├── 59aa759b77cb2eb53de0562f38938a4e3e7c5265.nq.gz
│   ├── 72b9b49cab6cd14e712b370bfd287becf5df5a17.nq.gz
│   ├── 73f06203127a3b4e875b7212eed1e53d0b125524.nq.gz
│   ├── 8d709769af5f87185b25581f9a2a6f43776c82bf.nq.gz
│   ├── 8ea2b08800dff68271151336483c72f9715e806d.nq.gz
│   ├── 9bb63c33320ebc13317e1a4f0096fa8117ea1dc8.nq.gz
│   ├── a3596c046925fbc8216ff110afa64c211b0cbbd3.nq.gz
│   ├── b64d6a7f87765c2a7883dcaf1d026e16e3e7e4d1.nq.gz
│   ├── bb3fa240f88450900f28382afaf72348bcc1c0f7.nq.gz
│   ├── c01b8dc5a52e82bda32ff5c106406d3c9679174e.nq.gz
│   ├── d0b11cac991ab8428a0dfe8d0ab8cfbde8cb9cd2.nq.gz
│   ├── d7df801cda9cac8136d0e2dadc1ca9cf57637395.nq.gz
│   ├── f80b62f37b81ab99ac9f878b6fbe891c05f756da.nq.gz
│   └── fe10f9d8a3509add131c389c992c05ef884d0f59.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── e61facef4927a581a94bf4aebdd0609b4c1317c9.nq.gz
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

[scrapy/loginform](https://github.com/scrapy/loginform)

---
*Parsed on 2026-10-12 by [repolex](https://repolex.ai)*
