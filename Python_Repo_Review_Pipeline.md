                 ┌────────────────────┐
                 │   Python Repo      │
                 └─────────┬──────────┘
                           │
        ┌──────────────────▼──────────────────┐
        │        1. FILE INGESTION            │
        │  (fd / ripgrep / traversal)         │
        └──────────────────┬──────────────────┘
                           │
        ┌──────────────────▼──────────────────┐
        │   2. STRUCTURAL PARSING LAYER       │
        │   Tree-sitter + CST extraction      │
        └──────────────────┬──────────────────┘
                           │
        ┌──────────────────▼──────────────────┐
        │   3. SYMBOL & OUTLINE BUILDER       │
        │   functions, classes, imports       │
        └──────────────────┬──────────────────┘
                           │
        ┌──────────────────▼──────────────────┐
        │   4. ENRICHMENT LAYER               │
        │   (semantic + diagnostics tools)    │
        └──────────────────┬──────────────────┘
                           │
        ┌──────────────────▼──────────────────┐
        │   5. RELATIONSHIP BUILDING          │
        │   call graph + import graph         │
        └──────────────────┬──────────────────┘
                           │
        ┌──────────────────▼──────────────────┐
        │   6. EVIDENCE AGGREGATOR            │
        │   merges + assigns confidence       │
        └──────────────────┬──────────────────┘
                           │
        ┌──────────────────▼──────────────────┐
        │   7. CODE KNOWLEDGE GRAPH (CKG)     │
        │   nodes + edges + confidence        │
        └──────────────────┬──────────────────┘
                           │
        ┌──────────────────▼──────────────────┐
        │   8. FLOW + ISSUE ANALYSIS          │
        │   CFG-lite + ruff + vulture + bandit│
        └──────────────────┬──────────────────┘
                           │
        ┌──────────────────▼──────────────────┐
        │   9. LLM CONTEXT BUILDER            │
        │   graph slicing + ranking           │
        └──────────────────┬──────────────────┘
                           │
        ┌──────────────────▼──────────────────┐
        │   10. LLM REFACTOR ENGINE           │
        │   suggestions + patches             │
        └──────────────────────────────────────┘
