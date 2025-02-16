# Incorrect Signal Initialization in VHDL

This repository demonstrates a common but subtle error in VHDL code: incorrect signal initialization.  The example shows a simple entity that registers input data. However, the internal signal `data_reg` is initialized to `x"00"`, which may not represent the intended reset state. This can lead to unexpected behavior, especially if the reset signal isn't actively asserted.

The `bug.vhdl` file contains the buggy code. The `bugSolution.vhdl` shows the corrected version.

## How to Reproduce

1.  Compile the `bug.vhdl` file using your preferred VHDL simulator.
2.  Simulate the code and observe the output. You might see unexpected values at the output before the first clock edge even if reset is asserted.

## Solution

Refer to `bugSolution.vhdl` for the corrected code. The improved initialization ensures a predictable default value.
