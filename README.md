# VHDL Multiplier Bug: Incorrect Signed Number Handling

This repository demonstrates a common error in VHDL code involving the incorrect handling of signed numbers in a multiplier. The original code uses the `UNSIGNED` type, which causes unexpected behavior when dealing with signed numbers. The solution showcases the proper use of the `SIGNED` type to correctly handle signed arithmetic.

## Bug Description
The `bug.vhdl` file contains a VHDL implementation of an 8-bit multiplier that incorrectly handles signed numbers.  It converts signed inputs to unsigned and then performs multiplication leading to incorrect results when negative numbers are involved.

## Solution
The `bugSolution.vhdl` file demonstrates the correct implementation using the `SIGNED` type. This ensures that the multiplication operation properly handles the signs of the input numbers.

## How to reproduce the bug
1. Simulate `bug.vhdl` using a suitable VHDL simulator (e.g., ModelSim, GHDL).
2. Apply both positive and negative test cases to inputs `a` and `b`.
3. Observe that the results are incorrect for negative input combinations.

## How to fix the bug
1. Replace `UNSIGNED` with `SIGNED` in the VHDL code to represent signed inputs `a` and `b`. 
2. Ensure that the `result` signal is also declared as `SIGNED` to properly reflect the signed output.
