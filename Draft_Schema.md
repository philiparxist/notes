```python
class Node:
    id: str                  # stable hash: file + symbol + span
    name: str                # function / class / variable name
    type: str                # "module" | "class" | "function" | "variable"
    file: str
    span: tuple[int, int]    # line range (start, end)
    signature: dict | None   # args, return (if known)
    metadata: dict           # flexible extension (types, docs, etc.)
    sources: list[str]       # ["tree_sitter", "pyright", "jedi"]

class Edge:
    id: str
    src: str                 # node id
    dst: str                 # node id
    type: str                # "calls" | "imports" | "contains" | "uses" | "assigns"
    confidence: float        # 0.0 - 1.0
    sources: list[str]       # which tools produced this edge
    evidence: dict           # optional raw evidence (spans, AST nodes, etc.)

class FileNode:
    path: str
    nodes: list[str]         # node ids in file
    imports: list[str]       # raw imports
    metadata: dict

class CodeGraph:
    nodes: dict[str, Node]   # node_id → Node
    edges: dict[str, Edge]   # edge_id → Edge
    file_index: dict[str, FileNode]
    meta: dict               # repo-level metadata

Node.metadata = {
    "inferred_type": "DataFrame",
    "is_async": True,
    "decorators": ["staticmethod"],
    "docstring": "...",
    "complexity": 12
}
```
