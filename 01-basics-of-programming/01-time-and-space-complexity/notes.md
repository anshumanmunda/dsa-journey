# Time Complexity

## Overview

Time complexity is a fundamental concept in programming, often misunderstood as the literal time it takes for code to run.

---

## 1. Misconception vs. Reality

| Aspect | Description |
|--------|-------------|
| **Misconception** | Time complexity = total execution time (e.g., 5 seconds) |
| **Reality** | Time complexity = **rate of increase in time** relative to **input size** |
| **Definition** | Measures how execution time grows as input data increases |

---

## 2. Why "Seconds" Are Unreliable

| Factor | Impact |
|--------|--------|
| **Hardware** | MacBook (5 sec) vs. Old CPU (15 sec) for same 500 lines |
| **Operating System** | Performance varies across Windows, macOS, Linux |
| **Server Speed** | Slow/busy servers increase execution time |
| **External Monitoring** | Interviewers don't use stopwatches |

---

## 3. Visualising Time Complexity

- **X-axis:** Input Size
- **Y-axis:** Time
- **The slope (θ/angle)** = Rate of Increase = Actual Time Complexity

> Example: 500 elements → 1 sec (Mac) vs. 2 sec (Pentium)  
> 2,000 elements → 4 sec (Mac) vs. much higher (Pentium)

---

## 4. Calculating Operations: Example

```python
# Printing a name n times
for i in range(1, n + 1):
    print("Anshuman")
```
Operation Breakdown (per iteration):

Step	Operation
1	Initialisation (i = 1)
2	Comparison (i < n+1)
3	Execution (print)
4	Increment (i = i + 1)
Calculation:

Operations per loop: ~3

For 5 iterations: 5 × 3 = 15 operations

For n iterations: n × 3 operations → 3n

### Simplified (ignoring constants): O(n)
``Three Rules of Calculation``

1. Worst Case	Assume the most difficult input possible
2. Remove Constants	Drop numbers that don't change with input size
3. Ignore Lower Bounds	Keep only the fastest-growing term


---
# Understanding Space Complexity

## Overview

**Space complexity** refers to the total amount of memory or storage space that a piece of code takes to run until its completion. Just like time complexity, it is expressed using **Big O notation (O)** to describe how the memory requirements grow as the input size increases.

---

## 1. The Space Complexity Formula

Space complexity is not just about the variables you create; it is the sum of two specific types of memory usage.

### Formula

> **Space Complexity = Auxiliary Space + Input Space**

| Component | Definition | Simple Example |
|-----------|------------|----------------|
| **Input Space** | The memory required to store the initial data (input) given to the program | A list of numbers provided to a function to be sorted |
| **Auxiliary Space** | The **extra space** or temporary variables created by the developer to solve the problem | Creating a new dictionary to count occurrences or a variable to store a sum |

---

## 2. Practical Example: Adding Three Numbers

Consider a simple task: finding the sum of three numbers `x`, `y`, and `z`.

### Method A: Using an Extra Variable (Recommended)

```python
x = 5
y = 10
z = 15

# 'total' is the extra space used to solve the problem
total = x + y + z 
print(total)
```
- Input Space: The memory used for x, y, and z

- Auxiliary Space: The memory used for the total variable