# repo-review

```
repo-review/
│
├── src/
│   ├── ingestion/           # file discovery, repo loading
│   ├── parsing/             # tree-sitter + structure extraction
│   ├── symbols/             # node + symbol builders
│   ├── enrichment/          # pyright, ruff, etc.
│   ├── relationships/       # call graph, import graph
│   ├── graph/               # CKG core (Node, Edge, CodeGraph)
│   ├── aggregator/          # merge + confidence logic (VERY IMPORTANT)
│   ├── flow/                # control flow (CFG-lite)
│   ├── context/             # LLM context builder
│   ├── llm/                 # prompts, refactor loop
│   └── utils/               # shared helpers (keep minimal)
│
├── tests/
│
├── scripts/                 # CLI entrypoints, experiments
│
├── data/                    # sample repos / fixtures
│
├── pyproject.toml
└── README.md
```
