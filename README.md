# Advent of Code 2024 – Day 2: Red-Nosed Reports

This repository contains my solution for Advent of Code 2024 Day 2.

## Problem Summary

Each line represents a report consisting of levels (numbers). A report is considered **safe** if:

- The levels are either strictly increasing or strictly decreasing
- The difference between adjacent levels is between 1 and 3 (inclusive)

### Part 2 (Problem Dampener)

A report is also considered safe if removing **one level** makes it valid according to the above rules.

---

## Approach

### Part 1
- Parse input into arrays of numbers
- Iterate through each report
- Check:
  - consistent direction (increasing or decreasing)
  - valid differences between adjacent values
- Count valid reports

### Part 2
- For each report:
  - First check if it is already safe
  - If not, remove one level at a time
  - Re-check using the same validation logic
- Count reports that become safe after removing one level

---

## How to Run

```bash
node index.js
```