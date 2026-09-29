# Repolex Knowledge Graph of cspotcode/outdent

RDF knowledge graph data for [cspotcode/outdent](https://github.com/cspotcode/outdent), parsed by [repolex](https://repolex.ai).

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
rlex download cspotcode/outdent
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3124b5584fbb3b25688751660fe6812a42bfb852
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 3124b5584fbb3b25688751660fe6812a42bfb852.nq.gz
│   └── repolex
│       └── 3124b5584fbb3b25688751660fe6812a42bfb852
│           └── chunk-001.nq.gz
├── blob
│   ├── 0024a101397a73520455c180a6de47dd18ad86e6.nq.gz
│   ├── 0d64e2363b51b2f237bd0f516b2667c51b21c951.nq.gz
│   ├── 0dc1fe8fa58fc1b886282ede5400e9b52dfe4ab5.nq.gz
│   ├── 1687e18904d9d1bf6832a62368bf94ae89247d97.nq.gz
│   ├── 18a3a4af19d73d50f95fe48a328e22d363e5d616.nq.gz
│   ├── 1f3d0e8b15f85d2383787eb2074c818ae3521065.nq.gz
│   ├── 21932bd99e67c19974230661fed3a3934fb4f7ce.nq.gz
│   ├── 2dd6396230dcdd35588d96f7e2c9367286971336.nq.gz
│   ├── 4dff1aa1d8beced6af1c77185672601bc2f79645.nq.gz
│   ├── 588782f840ea36edd50416160b51f49a2a58d3f3.nq.gz
│   ├── 58f47960db603a1c7aec8e44af1481e122e89ddb.nq.gz
│   ├── 6225e834790043504c334fb690c5a897539a0b3d.nq.gz
│   ├── 68e326ab66152e099e4e5e1bbd9cce8451999a0f.nq.gz
│   ├── 6ad84f04cb634e227a6b8bd48b3794e7dfba67ce.nq.gz
│   ├── 749ae81486e75fc2cb512cef24ede076f3cc7bf8.nq.gz
│   ├── 7727b7d407f85fe5dfdc8e3d75d71f986632b53d.nq.gz
│   ├── 7b55ef3b1c4129e26d6b842b0462a6455845c975.nq.gz
│   ├── 8a3573b05cf2b369252f658b8d77134fc057a5b8.nq.gz
│   ├── 9154822b19c6074290fd72a43860e00973de6d8d.nq.gz
│   ├── a4896134b99f385ea937af2a203872ac1f346230.nq.gz
│   ├── a9b203a6ecba9d50313ac70e21c836713442d0b2.nq.gz
│   ├── b470d61944bfc635a41861376467206f7f2c8136.nq.gz
│   ├── b758837b73a5df1f9d20069c48f9f4104c647c82.nq.gz
│   ├── bfe4d90f35de2988be5424941ffa96e80d56e3ca.nq.gz
│   ├── ca9659f11236b3c74816f6411bb0aa22f8aa77c1.nq.gz
│   ├── d9c7f1e6976e3f0733062605999d4fada4ddacbc.nq.gz
│   ├── e19b1b1dffdfcb020f1a4f36c31a6ba78781288c.nq.gz
│   ├── e3ebd8acca3bda10c63e8eb0b99b2dc070536b74.nq.gz
│   └── fa39ac7a44408e99270dcb973280e16300805f14.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 3124b5584fbb3b25688751660fe6812a42bfb852.nq.gz
├── filetree
│   └── 3124b5584fbb3b25688751660fe6812a42bfb852.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 39 files
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

[cspotcode/outdent](https://github.com/cspotcode/outdent)

---
*Parsed on 2026-09-29 by [repolex](https://repolex.ai)*
