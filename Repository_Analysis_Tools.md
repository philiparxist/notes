# 🧰 Repository Analysis Tools (Unified Table - Extended)

| Section | Tool | What it Gives You | Strengths | Limitations | Use? |
|--------|------|------------------|----------|------------|------|

## 🌳 Parsing & Structural Extraction
| Parsing | Tree-sitter | Concrete syntax tree (functions, classes, imports, works on broken code) | Handles invalid code, fast, precise spans | No semantics or resolution | ✅ Core foundation |
| Parsing | tree-sitter-analyzer | File outlines, symbol hierarchy, summaries | Ready-made extraction, LLM-friendly | Small project, limited depth | 🟡 Copy parts only |
| Parsing | libcst | Concrete syntax tree with formatting | Safe transformations, precise structure | Requires valid code | 🟡 Use later (refactoring) |
| Parsing | parso | Error-tolerant Python parser | Handles incomplete/invalid code | Less structured than CST tools | 🟡 Optional fallback |
| Parsing | tree_sitter_languages | Prebuilt Tree-sitter grammars | Easy setup, no manual compilation | Less flexible customization | ✅ Practical addition |
| Parsing | typed_ast | AST with type comment support | Useful for legacy/type-comment code | Limited modern relevance | 🔴 Niche |

## 🧠 Semantic Analysis & Type Inference
| Semantics | pyright | Cross-file symbol resolution, types, references | Fast, scalable, strong inference | Needs mostly valid code | ✅ Primary semantic engine |
| Semantics | jedi | Name resolution, references | Lightweight, easy integration | Weak cross-file understanding | 🟡 Optional |
| Semantics | astroid | Rich AST + inference | Deep understanding (pylint backend) | Breaks on invalid code | 🟡 Optional |
| Semantics | mypy | Type checking, type flow | Mature ecosystem | Slower, strict | 🟡 Optional |
| Semantics | pyre | Type checking (Meta) | Fast at scale | Setup complexity | 🟡 Optional |
| Semantics | pytype | Advanced type inference (Google) | Handles dynamic patterns better | Slower, less common | 🟡 High-value optional |

## 📞 Call Graph & Dependency Analysis
| Graph | pyan3 | Function call graph | Simple baseline | Incomplete, AST-based | 🟡 Baseline |
| Graph | pycg | Advanced call graph (research) | Better coverage than pyan3 | Still imperfect, less maintained | 🟡 Strong optional |
| Graph | grimp | Module import graph | Clean dependency mapping | No function-level detail | ✅ Core |
| Graph | CodeGraph CLI | Nodes + edges graph model | Matches your architecture | Experimental | 🟡 Inspiration |
| Graph | snakefood | Dependency graph | Simple import analysis | Outdated | 🔴 Avoid |

## 🧪 Diagnostics & Static Checks
| Diagnostics | ruff | Linting, syntax errors, refactor hints | Extremely fast, modern | Limited deep semantics | ✅ High value |
| Diagnostics | pylint | Deep linting, code smells | Thorough | Slow, noisy | 🟡 Optional |
| Diagnostics | bandit | Security analysis | Finds vulnerabilities | Narrow focus | 🟡 Valuable signal |
| Diagnostics | vulture | Dead code detection | Great for refactoring signals | Heuristic-based | 🟡 Valuable signal |
| Diagnostics | flake8 | Linting framework | Widely used | Fragmented, slower | 🔴 Replaced by ruff |

## 🧠 Advanced / Research-Level Analysis
| Advanced | scalpel | CFG + call graph + alias analysis | Deep program analysis | Heavy, complex | 🔴 Experimental |
| Advanced | codeql | Queryable semantic code graph | Extremely powerful queries | Complex setup, heavy | 🟡 Advanced use |

---
