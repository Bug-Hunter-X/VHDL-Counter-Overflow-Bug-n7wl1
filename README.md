# VHDL Counter Overflow Bug

This repository demonstrates a common bug in VHDL code: integer overflow in a counter.

The `counter.vhdl` file contains a simple counter that increments on each rising clock edge. However, it uses an integer type without explicitly handling overflow. This could lead to unexpected behavior once the counter reaches its maximum value (15 in this case).

The `counter_fixed.vhdl` file provides a corrected version that demonstrates a solution for this issue.

## How to Reproduce the Bug

1. Synthesize and simulate the `counter.vhdl` code.
2. Observe the counter's behavior when it reaches the maximum value (15).
3. The counter's behavior will wrap around to 0 or exhibit unexpected behavior, depending on the synthesis tool.

## Solution

The solution involves using a more robust data type, such as `unsigned`, which handles overflow in a predictable way.  The `counter_fixed.vhdl` file shows a corrected version using `unsigned`. 