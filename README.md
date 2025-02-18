# Uncommon Off-by-One Error in VHDL Counter

This repository demonstrates a subtle off-by-one error that can occur in VHDL counters, particularly when dealing with the upper limit of the count range.  The `buggy_counter.vhd` file contains the buggy code, while `corrected_counter.vhd` provides a solution.

## Description
The bug lies in the way the counter handles the rollover condition. When the `internal_count` reaches 15, the code resets it to 0. However, this might lead to unexpected behavior or a timing issue depending on the specific hardware implementation and clock cycle. The `corrected_counter.vhd` shows an alternate implementation to avoid potential issues. 

## How to reproduce the bug
1. Synthesize and simulate `buggy_counter.vhd`. 
2. Observe the counter's behavior at the upper limit of its range (15).
3. Compare to the expected behavior.

## Solution
The solution avoids the potential timing issue by using a different condition.  The `corrected_counter.vhd` file presents a more robust approach. 