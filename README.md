# Fundamentals of Programming in C++

## Introduction
🎯🎯🎯 This document provides a detailed explanation of the fundamental concepts of programming in C++. It covers essential topics such as data types, variables, operators, expressions, arrays, keywords, decision-making constructs, iteration, type casting, input-output statements, and functions. Each concept is defined thoroughly and explained in simple English with examples to make it easier to understand.

---

## 8. Iteration
🎯🎯🎯 Iteration constructs allow you to repeat actions multiple times. In C++, iteration is implemented using various loop structures, each suited to specific scenarios.

### 🔄 for Loop
The `for` loop is used when the number of iterations is known beforehand. It consists of three parts: initialization, condition, and increment/decrement.

**Syntax:**
```cpp
for (initialization; condition; increment) {
    // Code to execute repeatedly
}
```

**Example 1: Counting Numbers**
```cpp
for (int i = 1; i <= 5; i++) {
    cout << i << " ";
}
```
🎯🎯🎯 Output: `1 2 3 4 5`
Explanation: The loop initializes `i` to `1`, checks if `i <= 5`, executes the code block, and increments `i` after each iteration.

**Example 2: Iterating Through an Array**
```cpp
int numbers[] = {10, 20, 30, 40};
for (int i = 0; i < 4; i++) {
    cout << numbers[i] << " ";
}
```
🎯🎯🎯 Output: `10 20 30 40`
Explanation: The loop iterates through each index of the array `numbers`, printing its values.

---

### 🔄 while Loop
🎯 The `while` loop is used when the number of iterations is not fixed and depends on a condition being true.

**Syntax:**
```cpp
while (condition) {
    // Code to execute while condition is true
}
```

**Example:**
```cpp
int i = 0;
while (i < 5) {
    cout << i << " ";
    i++;
}
```
🎯🎯🎯 Output: `0 1 2 3 4`
Explanation: The loop starts with `i` equal to `0` and increments `i` until it reaches `5`, printing each value of `i`.

---

### 🔄 do-while Loop
The `do-while` loop guarantees that the code block executes at least once, as the condition is checked after the code runs.

**Syntax:**
```cpp
do {
    // Code to execute
} while (condition);
```

**Example:**
```cpp
int i = 0;
do {
    cout << i << " ";
    i++;
} while (i < 5);
```
🎯🎯🎯 Output: `0 1 2 3 4`
Explanation: The code block executes once before checking the condition (`i < 5`). It prints numbers from `0` to `4`.

---

### 🔄 foreach Loop (Range-Based for Loop)
Introduced in C++11, the `foreach` loop simplifies iteration over elements of a container, such as arrays or vectors.

**Syntax:**
```cpp
for (data_type element : container) {
    // Code to execute for each element
}
```

**Example:**
```cpp
int numbers[] = {1, 2, 3, 4, 5};
for (int num : numbers) {
    cout << num << " ";
}
```
🎯🎯🎯 Output: `1 2 3 4 5`
Explanation: This loop iterates over each element in the `numbers` array, printing its values.

---

### Key Differences Between Loop Types
🎯 Use the following table to understand when to use each loop:

| Loop Type     | When to Use                                      |
|---------------|--------------------------------------------------|
| `for`         | When the number of iterations is predetermined. |
| `while`       | When the condition determines the iterations.   |
| `do-while`    | When the code block must execute at least once. |
| `foreach`     | When iterating over containers (e.g., arrays).  |

### Summary
🎯🎯🎯 Loops are powerful constructs that allow efficient repetition of code. Use the `for` loop when the iteration count is fixed, the `while` loop for indefinite conditions, the `do-while` loop to ensure execution at least once, and the `foreach` loop for container traversal.

---

