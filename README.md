# LeetCode 118 – Pascal's Triangle

## Problem

Given an integer `numRows`, return the first `numRows` of **Pascal's Triangle**.

In Pascal's Triangle, each number is obtained by adding the two numbers directly above it.

The first and last elements of every row are always `1`.

## Example 1

**Input:**

```text
numRows = 5
```

**Output:**

```text
[
     [1],
    [1,1],
   [1,2,1],
  [1,3,3,1],
 [1,4,6,4,1]
]
```

## Example 2

**Input:**

```text
numRows = 1
```

**Output:**

```text
[[1]]
```

## Approach

We build Pascal's Triangle **row by row**.

For every new row:

* The first element is `1`.
* The last element is `1`.
* Every middle element is calculated by adding two adjacent elements from the previous row.

For example:

```text
Previous row: [1, 3, 3, 1]

New row:
1
1 + 3 = 4
3 + 3 = 6
3 + 1 = 4
1

Result: [1, 4, 6, 4, 1]
```

## Algorithm

1. Create an empty list to store the triangle.
2. Repeat until `numRows` rows are created.
3. Create a row containing `1`s.
4. Calculate the middle elements using the previous row.
5. Add the new row to the triangle.
6. Return the complete triangle.

## Complexity

* **Time Complexity:** `O(numRows²)`
  All elements in the triangle are generated.

* **Space Complexity:** `O(numRows²)`
  The complete Pascal's Triangle is stored as the result.

## Key Learning

This problem is a good example of **dynamic construction using a previous row**. It also helps in understanding nested lists and how values can be generated from previously calculated results.

## LeetCode Details

* **Problem Number:** 118
* **Problem Name:** Pascal's Triangle
* **Difficulty:** Easy
* **Language:** Python 3
* **File:** `solution.py`

## Topics

* Array
* Dynamic Programming

## Author

T.Nandhini
