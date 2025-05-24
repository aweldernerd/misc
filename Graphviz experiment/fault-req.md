
```markdown
# Fault Tree Diagram Example

Below is an example of a fault tree diagram represented in DOT language:

```dot
digraph FaultTree {
    rankdir=TB;
    node [shape=ellipse];

    // Top-level fault
    TopFault [label="System Failure", shape=box, style=filled, color=red];

    // Intermediate events
    Event1 [label="Power Failure"];
    Event2 [label="Hardware Failure"];
    Event3 [label="Software Failure"];

    // Basic events
    Basic1 [label="Battery Depleted"];
    Basic2 [label="Generator Malfunction"];
    Basic3 [label="CPU Overheat"];
    Basic4 [label="Memory Corruption"];
    Basic5 [label="Bug in Code"];

    // Connections
    TopFault -> {Event1 Event2 Event3};
    Event1 -> {Basic1 Basic2};
    Event2 -> {Basic3 Basic4};
    Event3 -> Basic5;
}
```

To visualize this fault tree diagram, save the DOT code to a `.dot` file and use Graphviz tools like `dot` to generate an image:

```bash
dot -Tpng fault_tree.dot -o fault_tree.png
```
```

 may indicate a worn bearing.
