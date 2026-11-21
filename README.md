# Repolex Knowledge Graph of rust-cli/roff-rs

RDF knowledge graph data for [rust-cli/roff-rs](https://github.com/rust-cli/roff-rs), parsed by [repolex](https://repolex.ai).

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
rlex download rust-cli/roff-rs
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 309d82d9a159972c39b5163c4b56dba49870729e
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 309d82d9a159972c39b5163c4b56dba49870729e.nq.gz
│   └── repolex
│       └── 309d82d9a159972c39b5163c4b56dba49870729e
│           └── chunk-001.nq.gz
├── blob
│   ├── 001c7c4c1f66232430f6e324ea6a2d381fbd2af0.nq.gz
│   ├── 08d1666c277dabcde8b11114345606720a163134.nq.gz
│   ├── 1d4c5dc66f4e229b407587965d09da9816e06eac.nq.gz
│   ├── 27bf59a884cdc6948c686a9eb9b3f0fe99691c95.nq.gz
│   ├── 41fc80339f79d9684bb769e029f21e07d8e9b454.nq.gz
│   ├── 4211ae3842810ba7207dfc2148a5354e28276bda.nq.gz
│   ├── 444137478698fa3d555658a03f3ce6e7e55c5fc7.nq.gz
│   ├── 45aa9c9474191821191f84404c71a268fb40dd85.nq.gz
│   ├── 4a6a1abdd612113aea698f0f51e28cb675ea8ead.nq.gz
│   ├── 4c83870825b175289e12b044b613625e0ca60246.nq.gz
│   ├── 6a909d61914d43de4596c479dd79bda3baff7829.nq.gz
│   ├── 74da69b88f56f173030104d5389504b558b78e1b.nq.gz
│   ├── 755a367adcdf9144a6b5edd2d88ab58a95b90ca0.nq.gz
│   ├── 7aabc20fe1c2cbf46eba47bff8a507fed06fd6bc.nq.gz
│   ├── 8aa3bfca18674c22f7ee5915dfb3341f2231d7cc.nq.gz
│   ├── 8b52c565332035026546e531939d3382dc35da53.nq.gz
│   ├── 8f71f43fee3f78649d238238cbde51e6d7055c82.nq.gz
│   ├── 9722b0344855344783a7fa2ddc1f7aa2acf58282.nq.gz
│   ├── a2d01088b6ce55e837a6d193943580f978fb2d2e.nq.gz
│   ├── addbe4b73ba2b3bb614e78438d5d14dee633a018.nq.gz
│   ├── ba3fe01c82a71576d52fcd4e209b237c002332b5.nq.gz
│   ├── c51104f25e6f14d2893b8b1e52bdd90e17ded12b.nq.gz
│   ├── d02b16db44966a0b909ce73bce646270494810dc.nq.gz
│   ├── d880c30ba42cc032b95edff21ec6eff735d4587f.nq.gz
│   ├── e26844933530f88f78044e62d131690890fe16b9.nq.gz
│   ├── eb5a316cbd195d26e3f768c7dd8e1b47299e17f8.nq.gz
│   ├── f77799d568ff30a536808fefefed8617535f5fde.nq.gz
│   └── fc3f1775cce8f4b8b9e8687458e3d149a8f6d169.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 309d82d9a159972c39b5163c4b56dba49870729e.nq.gz
├── filetree
│   └── 309d82d9a159972c39b5163c4b56dba49870729e.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 38 files
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

[rust-cli/roff-rs](https://github.com/rust-cli/roff-rs)

---
*Parsed on 2026-11-21 by [repolex](https://repolex.ai)*
