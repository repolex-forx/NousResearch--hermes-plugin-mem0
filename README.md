# Repolex Knowledge Graph of NousResearch/hermes-plugin-mem0

RDF knowledge graph data for [NousResearch/hermes-plugin-mem0](https://github.com/NousResearch/hermes-plugin-mem0), parsed by [repolex](https://repolex.ai).

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
rlex download NousResearch/hermes-plugin-mem0
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3fc36950b2b7c19cdd81c6de99f10d2cbed850af
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 3fc36950b2b7c19cdd81c6de99f10d2cbed850af.nq.gz
│   └── repolex
│       └── 3fc36950b2b7c19cdd81c6de99f10d2cbed850af
│           └── chunk-001.nq.gz
├── blob
│   ├── 00f2d38d8063d0c6b219c0081e51888063b0c55e.nq.gz
│   ├── 637aae098d4fc6915f8a488d87cda2b3177b53b7.nq.gz
│   ├── 75410e73319c72cd3e991a501c5455eb78f38375.nq.gz
│   ├── 884d8037157be754a606c79d8431d5d25e96c04e.nq.gz
│   ├── 88f8fdd5efd6b4e1b3e11a7ca86e1100bbc3f004.nq.gz
│   ├── 8f55496e305d41f0d0f5512a6252f742b9b5cb14.nq.gz
│   ├── b6d86500aece08bd4f82e0274ebe94d56bf36a8d.nq.gz
│   ├── bf58c1a4c5f6aae3d45ff5023ae0978f17648bae.nq.gz
│   ├── c6ae10acca8dda674d1ffe732c523e5a31572d72.nq.gz
│   ├── c6ced627fc1df41b6fe960c2b6fb145582e0651b.nq.gz
│   └── d4c770e6841845969c546e2e459f1260dca67c41.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 3fc36950b2b7c19cdd81c6de99f10d2cbed850af.nq.gz
├── filetree
│   └── 3fc36950b2b7c19cdd81c6de99f10d2cbed850af.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 19 files
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

[NousResearch/hermes-plugin-mem0](https://github.com/NousResearch/hermes-plugin-mem0)

---
*Parsed on 2026-09-30 by [repolex](https://repolex.ai)*
