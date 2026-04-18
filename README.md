# Repolex Knowledge Graph of jaraco/configparser

RDF knowledge graph data for [jaraco/configparser](https://github.com/jaraco/configparser), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download jaraco/configparser
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d4a49e97b08883f8f89ace13f8f812f07f58ef2f
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── d4a49e97b08883f8f89ace13f8f812f07f58ef2f.nq.gz
│   └── repolex
│       └── d4a49e97b08883f8f89ace13f8f812f07f58ef2f
│           └── chunk-001.nq.gz
├── blob
│   ├── 0b9921ccebeea1e2dbbda7f0ee49fa7762f0aac3.nq.gz
│   ├── 0c0e0d35273a399e9e66ebb8d78b0616b5d910a3.nq.gz
│   ├── 13b6f5bf14fa08d76779fc260c730c0a84d9eb35.nq.gz
│   ├── 19213f62e4e1404dd02c46271c66f7d1d7e1067e.nq.gz
│   ├── 1bb5a44356f00884a71ceeefd24ded6caaba2418.nq.gz
│   ├── 26166669cc3685473d95860f21b9db315aa9f7c8.nq.gz
│   ├── 304196f81e11a168c9894f966e4a617ebf4ed53c.nq.gz
│   ├── 32027f5b4f051a81d67b3fd6d809b60531be2360.nq.gz
│   ├── 33cd742974ad8d8c7b1d45ff6387b9fcb62aabbb.nq.gz
│   ├── 35b98b1df96093e99fea65bec2187baff3c12514.nq.gz
│   ├── 3d33a599809ed91afd9367344297a51c53c06f2e.nq.gz
│   ├── 472c8b4c84f3770ce0940bddff6d8d276a4bfe8a.nq.gz
│   ├── 54f99acbfac68c2be8283174ea64f1730a795e49.nq.gz
│   ├── 5a4a7e9166ec3143f71b5e3875860802048554f3.nq.gz
│   ├── 5bdc232005af9be104a00437ae9bc64417a4c1cc.nq.gz
│   ├── 6fa480e44f38768722368d7a986607adacf41d99.nq.gz
│   ├── 7c23a376cee0cbacf596dc8ce00c964dcbf1b4de.nq.gz
│   ├── 84800f61a45ba0625e339f3bdf5976c0a4b1b585.nq.gz
│   ├── 89ff33961ba3d6f9cda89322a1fdbf1ac2e35513.nq.gz
│   ├── 922aa1f19856d5841e80b0a2370e0e5fa7c41512.nq.gz
│   ├── a9fdc324d6dd73c2bf5dd7ac42c8c86cda5d8fa9.nq.gz
│   ├── ac0ff69e22507b430cfb9a91d98e2451a3de52d9.nq.gz
│   ├── b6f972769e61a5e65f9f45015b363cc362487e55.nq.gz
│   ├── c1379265983859cbde11f047c7e41854e4c49af1.nq.gz
│   ├── c182cd739c26bb78c97082bb0d7834d94aadc8e4.nq.gz
│   ├── c4c22094a610c6651b7ec2f071d87fb225cdd2a3.nq.gz
│   ├── cfcfef23bfd49362a58cbb493043ece2aaaf0f2b.nq.gz
│   ├── d7fadafa23493c51ad0ff4896432ffb6ea703a01.nq.gz
│   └── dc8516ac20b3d38cf754fe8d804ffdffafc15ef0.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── d4a49e97b08883f8f89ace13f8f812f07f58ef2f.nq.gz
├── filetree
│   └── d4a49e97b08883f8f89ace13f8f812f07f58ef2f.nq.gz
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

## Source repository

[jaraco/configparser](https://github.com/jaraco/configparser)

---
*Parsed on 2026-04-18 by [repolex](https://repolex.ai)*
