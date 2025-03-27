+++
date = "2025-03-22T21:21:43+08:00"
draft = false
title = "Understanding Algorithms and Pseudocode"
tags = ["Algorithm", "Pseudocode"]
summary = "A beginner-friendly guide to understanding algorithms and pseudocode, with simple and complex examples."

[params]
math = true
+++


# Introduction

Algorithms are step-by-step instructions designed to solve problems. They are the foundation of programming and computer science. Whether you’re sorting numbers, searching for data, or making a game character move, algorithms are everywhere.

To express algorithms clearly, we often use **pseudocode**—a simplified way to write logic without focusing on specific programming language syntax.

In this post, we’ll explore both simple and complex algorithms using pseudocode.

---

# Simple Example: Finding the Maximum of Two Numbers

Let’s start with a basic problem: finding the larger of two numbers.

### **Pseudocode**:

```plaintext
Algorithm FindMax(A, B):
    If A > B Then
        Return A
    Else
        Return B
```

### **Explanation**:

1. Compare `A` and `B`.
2. Return the larger one.

### **Example Execution**:

- Input: `A = 5, B = 9`
- Output: `9`

---

# More Complex Example: Bubble Sort

Now, let’s look at something more challenging—**Bubble Sort**, an algorithm that sorts a list by repeatedly swapping adjacent elements if they are in the wrong order.

### **Pseudocode**:

```plaintext
Algorithm BubbleSort(Array):
    N = length of Array
    Repeat N-1 times:
        For i from 0 to N-2:
            If Array[i] > Array[i+1] Then
                Swap(Array[i], Array[i+1])
```

### **Explanation**:

1. Loop through the list multiple times.
2. Compare adjacent elements.
3. Swap them if they are in the wrong order.
4. Repeat until the list is sorted.

### **Example Execution**:

#### Input:

`[5, 3, 8, 4, 2]`

#### Iterations:

1. `[3, 5, 4, 2, 8]`
2. `[3, 4, 2, 5, 8]`
3. `[3, 2, 4, 5, 8]`
4. `[2, 3, 4, 5, 8]` (Sorted!)

### **Complexity**:

- Worst case: **O(n²)**
- Best case (already sorted list): **O(n)**

---

# Conclusion

Algorithms range from simple comparisons to complex sorting techniques. Learning to express them in pseudocode makes it easier to understand their logic before implementing them in programming languages.

Want to learn more? Try implementing these in Python, Java, or C++!

