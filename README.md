# Repolex Knowledge Graph of magmax/python-readchar

RDF knowledge graph data for [magmax/python-readchar](https://github.com/magmax/python-readchar), parsed by [repolex](https://repolex.ai).

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
rlex download magmax/python-readchar
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── cba1fa062e44a5c6a3045bb1c68e8a91fa6f746d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── cba1fa062e44a5c6a3045bb1c68e8a91fa6f746d
│           └── chunk-001.nq.gz
├── blob
│   ├── 047f31d1a23390cdd7dd848d608fa3663afa4e62.nq.gz
│   ├── 053519004be966267094f8ae7f1ea6419ab15074.nq.gz
│   ├── 0c45b407025e05a3b1601536ba83b461e446e94c.nq.gz
│   ├── 0dde25d164af4d0a905a3950f9768586a3a5348e.nq.gz
│   ├── 1115eaa5d924a5521a47a685da903461d28176a9.nq.gz
│   ├── 200bb4438a5a3136c58326303b04046097448a84.nq.gz
│   ├── 2d0448c32c7db1186ac3f6698495f237905d7401.nq.gz
│   ├── 3283724c54f14712429399360c1678bdac3396d2.nq.gz
│   ├── 37f456fdb60c1e0afa7072f2aa05d5e40391f76d.nq.gz
│   ├── 4b52d33d7e0ed2472832388e1477a01c9d7da805.nq.gz
│   ├── 55a3623f138fba06e4d73f418f4b76d820c84ce0.nq.gz
│   ├── 5b4a12b2c007e27c6bc3ba8a207fa747ff3677a7.nq.gz
│   ├── 5def95deb0240272d9d998037e45356b571fd1c2.nq.gz
│   ├── 6011b6c43cce6fd9fba3be9a6e97698db475eea2.nq.gz
│   ├── 66937d171e48ca37b57383850b2c26f2c36e7701.nq.gz
│   ├── 77e8a58f196b45f520d576a3fc08701edd4f3dfb.nq.gz
│   ├── 8864a3dda62f47f2c268751a5d866c004a9fd6f6.nq.gz
│   ├── 8a896bb5b1560a562f2b732f1486ca1132f80162.nq.gz
│   ├── 8f45fe13c4109a92f86bf2c5e00aad716b81ded6.nq.gz
│   ├── a3cdbcd33c4be58d7beaf06ba92d437bc2330ddc.nq.gz
│   ├── b8a830312787a87c5f0e41cbfe9034ad355d9d57.nq.gz
│   ├── c2a31142eac711b0bf5dd4bf7a3c8e7141a5a33d.nq.gz
│   ├── c712d2595247bf32129c8609dcf822e238412a20.nq.gz
│   ├── cd1203430732462798cb9547cf13739eb6be547e.nq.gz
│   ├── d91a55ff748e6e38a516ef323f7f573c66c3b230.nq.gz
│   ├── e0264e8ce63d67ee88c40dad0a1e96b770e2b346.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e84fc0a014225c69c9da7ab5e0cb3389447dc54c.nq.gz
│   ├── e89683091b345eebadc00ef2f7fc75908741a7d8.nq.gz
│   ├── eb96a851dfc5ad747276aad41430f788d7b29770.nq.gz
│   ├── ec7901aeb06aeab71be133ca6ab8f84f2f73959c.nq.gz
│   ├── ed083400884b5e184ec92996f01b069ceb77bb8a.nq.gz
│   ├── f2baafdf8a5fba1bd1262ce79becb9efac7a3f31.nq.gz
│   ├── f43c620146cb21e9c5ffa02c82267d6e07df0ef2.nq.gz
│   ├── f49cc3c03c0aaf0d35252e43c8b10f0ebb28f421.nq.gz
│   ├── f58464d2b7ad428d35fd84301113f7cdabf3b14a.nq.gz
│   ├── f744efef04b44567b25cc6cac13fc145fecc094b.nq.gz
│   └── feb0f8420dc0bc974e6fca4b28e78f377de592e4.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── cba1fa062e44a5c6a3045bb1c68e8a91fa6f746d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 46 files
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

[magmax/python-readchar](https://github.com/magmax/python-readchar)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
