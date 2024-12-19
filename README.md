# VHDL Counter Bug and Solution

This repository demonstrates a common error in VHDL counters: improper overflow handling and potential off-by-one errors.  The `buggy_counter.vhd` file contains the buggy code. The `fixed_counter.vhd` provides a corrected version.

## Bug Description
The original VHDL counter implementation might not increment correctly or exhibit unexpected behavior when reaching the upper bound of its range.  This is due to a potential off-by-one error and a lack of robust overflow handling.

## Solution
The corrected version (`fixed_counter.vhd`) addresses the potential off-by-one error by ensuring the counter correctly wraps around from the maximum value to zero.  It also incorporates more robust overflow handling to prevent unintended behavior.

## How to reproduce the bug:
1. Synthesize and simulate `buggy_counter.vhd`.
2. Observe the counter's behavior as it approaches and exceeds its maximum value (15 in this case).
3. Compare this behavior to the corrected version (`fixed_counter.vhd`).
