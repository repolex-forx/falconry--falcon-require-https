# Repolex Knowledge Graph of falconry/falcon-require-https

RDF knowledge graph data for [falconry/falcon-require-https](https://github.com/falconry/falcon-require-https), parsed by [repolex](https://repolex.ai).

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
rlex download falconry/falcon-require-https
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1c1fd26aa72b6057748a9919b9638987749bb7d8
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 1c1fd26aa72b6057748a9919b9638987749bb7d8
│           └── chunk-001.nq.gz
├── blob
│   ├── 00d5bdb98fa77fe9f2204b221944430e80dd8b94.nq.gz
│   ├── 1491bc04ffc0bf6470d5f83d87367ba44725bae4.nq.gz
│   ├── 1b06114f6254e3bd2bcd86dfeca7f65abe26f176.nq.gz
│   ├── 1cabd0a0cbea2591a0c77d900f414f9cea3d2f42.nq.gz
│   ├── 35ecfdf9ea4ed542c4af11976b01fef4040c387f.nq.gz
│   ├── 590e1a9c92afe2a3575f51c0fb1efdfa6509aef0.nq.gz
│   ├── 62fd8545262062ba8c63e89a55880af598b39bc4.nq.gz
│   ├── 74ce1a9da37230cc659b0dbde4c077693a7e4d32.nq.gz
│   ├── 75b8d08d19e31044ccfdfc94ed4b2456beeea9c9.nq.gz
│   ├── 777fd9d78c6876ae2ded137b6a58a7b3a95d9231.nq.gz
│   ├── 7d9e5047764e25ce8fe65efa3b8d25f7ec34caae.nq.gz
│   ├── 95ecfeaf8ca102f5a16ea18e8eaf27d8451af31e.nq.gz
│   ├── 98ab153bc6b3efc3085bb0764ba7995c898d8c5e.nq.gz
│   ├── a7d8a7aae05cecf5dad04af80df212e1b6877b3e.nq.gz
│   ├── aef3e2dfffd2894baf187c7090728f156140e01c.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 1c1fd26aa72b6057748a9919b9638987749bb7d8.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 24 files
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

[falconry/falcon-require-https](https://github.com/falconry/falcon-require-https)

---
*Parsed on 2026-10-12 by [repolex](https://repolex.ai)*
