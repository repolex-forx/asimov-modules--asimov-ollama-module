# Repolex Knowledge Graph of asimov-modules/asimov-ollama-module

RDF knowledge graph data for [asimov-modules/asimov-ollama-module](https://github.com/asimov-modules/asimov-ollama-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-ollama-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── b24037e8995a22f12b2ed020d39dfa09aea504bf
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── b24037e8995a22f12b2ed020d39dfa09aea504bf.nq.gz
│   └── repolex
│       └── b24037e8995a22f12b2ed020d39dfa09aea504bf
│           └── chunk-001.nq.gz
├── blob
│   ├── 10b359dd05935c73efb064470f9ecda90f6d28aa.nq.gz
│   ├── 17903defa16e9015fb686762d2bd6c99d56147d2.nq.gz
│   ├── 2f0b2378842be4f2ce9a7742e16cbf508b9b5a5e.nq.gz
│   ├── 594b928051d632cb067863ad5f9838dad80cb386.nq.gz
│   ├── 6b23d61018f43b840f8d2ff3b45a1c02d76df38d.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 9cfbcbb94de1d56ac955902b3a17edf7103f5986.nq.gz
│   ├── 9fe50de16e59d550235aa6d7d15ee12ddf054414.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── b603c397ff2a1d890bd0983b2ad9aeda9bdef7ec.nq.gz
│   ├── bcab45af15a0f1b0166daf8cbf18b17cd8649277.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eda13577384817e3138d6c11a6d1d97f33448085.nq.gz
│   ├── ef68a2cd5d2762e045dfa8bd8dcd6b17886ca9a7.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   └── f1541891b473002bb5942941ee8ba570b649ab6b.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── b24037e8995a22f12b2ed020d39dfa09aea504bf.nq.gz
├── filetree
│   └── b24037e8995a22f12b2ed020d39dfa09aea504bf.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 28 files
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

[asimov-modules/asimov-ollama-module](https://github.com/asimov-modules/asimov-ollama-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
