# Repolex Knowledge Graph of pydantic/rust-jemalloc-pprof

RDF knowledge graph data for [pydantic/rust-jemalloc-pprof](https://github.com/pydantic/rust-jemalloc-pprof), parsed by [repolex](https://repolex.ai).

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
rlex download pydantic/rust-jemalloc-pprof
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 627104aa72ee2e0ca260db928154df1a46ee29ee
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 627104aa72ee2e0ca260db928154df1a46ee29ee
│           └── chunk-001.nq.gz
├── blob
│   ├── 02e100c24612ef17b42d53ab5020d615a9cdc54b.nq.gz
│   ├── 0a36411763cc42757460f84bd99ed5b5f81eff2b.nq.gz
│   ├── 1878b341beb5ed0df28351db039bdd5ff1e2e25d.nq.gz
│   ├── 1e6e4881a4decd70711ade8a39ba7bd518bc33a1.nq.gz
│   ├── 2ea171155d932189cc2ab63b1bde80744ca946cb.nq.gz
│   ├── 32ac9ddcd169d3f05a55fc294e9be441fefcdf8c.nq.gz
│   ├── 44041ad4e66365c9843c4c84e424f396a14c5bc9.nq.gz
│   ├── 5bbebe12f565afa5f8c5483233f96c7f5a87fd64.nq.gz
│   ├── 65a543bef994746c31c149a1230165fa162ec89f.nq.gz
│   ├── 6b66a00b1b6dd5892eba86d30a5cfbe908c0cd0f.nq.gz
│   ├── 705cb5be98e619b8d1f1a8e2db422596f8892d87.nq.gz
│   ├── 77e1fd0ac1b8ca7d9d8a8abbbd4b059940f2b689.nq.gz
│   ├── 888f1d836ea389f0e44b79ff97856c7bdb63eb98.nq.gz
│   ├── 8b1a081f0b45f088b8b5d4f019b2382b791f16d0.nq.gz
│   ├── 9ee9889c614ea8d4afb90cefde69242a76e61512.nq.gz
│   ├── a43d836339a5af524ad89310bfa9831f788896a8.nq.gz
│   ├── a650f383868eac14c16333c9d32308ecae2d4fce.nq.gz
│   ├── a758b29b14ad0882c53f2de8835cc1497e79b1d1.nq.gz
│   ├── a9d37c560c6ab8d4afbf47eda643e8c42e857716.nq.gz
│   ├── b36516035bbfbaa89670934c7f6c4f0c14674885.nq.gz
│   ├── d4e34423f5afd945d036cb57364f3f4c24a2680f.nq.gz
│   ├── d57083c354524d47820f8aa31b3b35532f2e3e13.nq.gz
│   ├── e50bd8bc4d60417b38ed460dc2e4c2dd1a533a5e.nq.gz
│   ├── ea8c4bf7f35f6f77f75d92ad8ce8349f6e81ddba.nq.gz
│   └── fcfab0ac37d71c886c8a0737f2d8073fa4eb81c6.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 627104aa72ee2e0ca260db928154df1a46ee29ee.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 31 files
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

[pydantic/rust-jemalloc-pprof](https://github.com/pydantic/rust-jemalloc-pprof)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
