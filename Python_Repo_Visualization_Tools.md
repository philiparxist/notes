# Python Repo Visualization Tools (Scrutinized)

| Tool | Analysis type | Works on whole repo? | Visualization type | Visual output | Strengths | Limitations |
|------|--------------|---------------------|--------------------|--------------|----------|-------------|
| PyCG | Static analysis | ✅ Yes (package-level) | Call graph (static) | DOT / Graphviz | Builds inter-module call graph using static analysis | Misses dynamic/runtime behavior; limited precision in complex Python |
| callflow-tracer | Runtime tracing | ⚠️ Partial (via entrypoint / batch) | Call graph + flamegraph + timeline | Interactive HTML / SVG | Interactive graphs, multiple layouts, profiling + filtering | Only shows executed paths |
| pycallgraphix | Runtime (instrumented) | ⚠️ Partial (manual selection) | Call graph (filtered) | PNG (Graphviz) | Lets you restrict graph to selected functions | Not automatic repo-wide coverage |
| python-call-graph | Runtime tracing | ⚠️ Partial (entrypoint only) | Call graph (execution) | Graphviz (PNG/SVG) | Simple and quick execution tracing | Not repo-aware; somewhat outdated ecosystem |
| VizTracer | Runtime tracing | ⚠️ Partial | Execution timeline + flamegraph | HTML / Chrome trace viewer | Strong temporal visualization (when calls happen) | Not a true call graph tool |
| PyTracer | Runtime profiling | ⚠️ Partial | Trace visualization (numerical / flow) | Interactive dashboard | Good for scientific / numerical tracing | Not general-purpose call graph tool |
| pyftrace | Runtime tracing | ⚠️ Partial | Textual call trace (tree-like) | CLI output | Lightweight, real-time tracing | No real visual graph (mostly text) |
| Graphviz | Rendering engine | — | Graph rendering (DOT graphs) | PNG / SVG | Standard backend for visual graphs | Not a generator (needs another tool) |
