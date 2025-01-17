# Elixir Enum.reduce Bug

This repository demonstrates a subtle bug in using Elixir's `Enum.reduce` for conditional summation. The provided code intends to sum elements of a list that are greater than 3. However, it produces an incorrect result due to an oversight in how the accumulator is handled.

## Bug Description
The issue arises from the way the `if` statement within the `Enum.reduce` function updates the accumulator. If a number less than or equal to 3 is encountered, the accumulator remains unchanged. This can lead to an unexpected final sum if the initial value of the accumulator isn't appropriately considered.

## Solution
The solution involves a small adjustment to the `Enum.reduce` function to correctly handle the accumulator and produce the expected result.