# Repolex Knowledge Graph of zopefoundation/zope.exceptions

RDF knowledge graph data for [zopefoundation/zope.exceptions](https://github.com/zopefoundation/zope.exceptions), parsed by [repolex](https://repolex.ai).

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
rlex download zopefoundation/zope.exceptions
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── dc273c2b6184d34095d932de7e025adbac1a2979
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── dc273c2b6184d34095d932de7e025adbac1a2979
│           └── chunk-001.nq.gz
├── blob
│   ├── 01ea5ad01e0f489f6e715d36c2483715dd52df33.nq.gz
│   ├── 1c4ba0faded35618be2f6775404930d756c3faaa.nq.gz
│   ├── 2596a596db536ea35996d5d7cabb3da57d8bb7d0.nq.gz
│   ├── 2f9314c225b56dd08167a460ebc16eb80f0ae1ff.nq.gz
│   ├── 36a0f514cb1f7f1678402db463143e289b77599b.nq.gz
│   ├── 45908f89f4bfee2d70e5aff1e903843dbaf84c53.nq.gz
│   ├── 525e4b0a9f04a0531373d04aad0fc3c4bc5ddbda.nq.gz
│   ├── 52baa1532dda8f90a66056da855543c138264d90.nq.gz
│   ├── 56fecdb72a75c4118ba880431beb7a936ff2cef0.nq.gz
│   ├── 5871ed63f7ab13739d604b7adf488aa8d6bb883d.nq.gz
│   ├── 792d6005489ebee62cde02066f19c5521e620451.nq.gz
│   ├── 79859e06010bf4967c5b4b044afea6ef39742938.nq.gz
│   ├── 8a1cde635fcfe005cc4438d504940505395236a7.nq.gz
│   ├── 9fcaddf7faf5cb3fc3dc5dcbbda5279891afd248.nq.gz
│   ├── a2f3bdc5c3790ab06761dd24540231876c588f1e.nq.gz
│   ├── a61ec7239c9bcda67d1e9107c90a4672b30457a1.nq.gz
│   ├── a75c3c672a3c4890acce3bf46d23be3b379b9306.nq.gz
│   ├── b2c082c42f97ce4da4491d28095aeeae12244ebe.nq.gz
│   ├── b3f17bb1267ce2d9bd95d04179f81c38b9a0e6c9.nq.gz
│   ├── c4f7f5aa01133b71148227d3ab2704add2bcd8ee.nq.gz
│   ├── c634bd6257977ab9c6d5de4c242f1f303d0ed4e8.nq.gz
│   ├── c6bd097d4c43af91f5b22e95d4426b75756a67f8.nq.gz
│   ├── c9ff9eef775708599f80e94b02bc11a8a3727f06.nq.gz
│   ├── ca517f4eb0cec1c691c0c2b54cd5eb85e906f11b.nq.gz
│   ├── cefdfdf5bd45a16b0ca52c4aea30812b347a76f9.nq.gz
│   ├── dcda99b3bfc4d6f617cfc8cd959e1eafe0669887.nq.gz
│   ├── e1b8d521c00692c6543e5c0a1bc4f7e7b78a99ad.nq.gz
│   ├── e1f9ad7b3b48377bfbfaa1b380c384ddea24060f.nq.gz
│   ├── e3579011e1a5792ed2adb52fe79f1ac001b9c3bf.nq.gz
│   ├── e3b5190dfcf61adbc3bf88234a073497428a2e53.nq.gz
│   ├── e4b867329e05886a4818f86b117fca2102bc84bf.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f81cabf053fb4487bb3496afbc276556076bc3f2.nq.gz
│   └── fb44e5eeb39f6c823bc2c63a30fc076eef564f03.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── dc273c2b6184d34095d932de7e025adbac1a2979.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 42 files
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

[zopefoundation/zope.exceptions](https://github.com/zopefoundation/zope.exceptions)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
