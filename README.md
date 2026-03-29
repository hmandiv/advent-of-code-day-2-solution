# Advent of Code 2024 – Day 2: Red-Nosed Reports

This repository contains my solution for Advent of Code 2024 Day 2.

## Problem Summary

Each line represents a report containing a sequence of levels.

A report is considered **safe** if:

- the levels are either all increasing or all decreasing
- the difference between each pair of adjacent levels is between 1 and 3 inclusive

### Part 2 – Problem Dampener

A report is also considered safe if it is already valid, or if removing exactly one level makes it valid.

## Approach

### Part 1
- Parse the input into arrays of numbers
- For each report, examine adjacent pairs
- Track:
  - whether each difference is valid
  - whether the overall trend is increasing or decreasing
- Count reports where all differences are valid and the trend is consistent

### Part 2
- Reuse the Part 1 validation logic
- First check whether a report is already safe
- If not, create modified versions of the report by removing one level at a time
- Re-check each modified report using the same Part 1 logic
- Count reports that become safe after removing one level

## How to Run

```bash
node index.js
```