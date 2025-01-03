
# 🚀 C++ UNIT II

## 📌 Table of Contents
1. [Operators](#operators)
2. [Data Types](#data-types)
3. [Variables](#variables)
4. [Arrays](#arrays)
5. [Functions](#functions)
6. [Control Structures](#control-structures)
7. [Pointers](#pointers)
8. [Memory Management](#memory-management)
9. [Object-Oriented Programming](#object-oriented-programming)
10. [Advanced C++ Concepts](#advanced-c-concepts)

## 🔧 Operators

### 1. Arithmetic Operators

#### Overview
Arithmetic operators perform mathematical operations on numeric values.

```cpp
int a = 10, b = 3;

// Basic Operations
int sum = a + b;        // Addition
int diff = a - b;       // Subtraction
int product = a * b;    // Multiplication
int quotient = a / b;   // Division
int remainder = a % b;  // Modulus
```

**Advanced Tricks**

```cpp
// Swap without temporary variable
a = a + b;
b = a - b;
a = a - b;

// Quick multiplication/division by 2
int x = 10;
x = x << 1;  // Multiply by 2
x = x >> 1;  // Divide by 2
```

### 2. Bitwise Operators

#### Bitwise Operations
```cpp
int a = 5;  // Binary: 0101
int b = 3;  // Binary: 0011

// Bitwise AND
int andResult = a & b;  // 1 (0001)

// Bitwise OR
int orResult = a | b;   // 7 (0111)

// Bitwise XOR
int xorResult = a ^ b;  // 6 (0110)

// Bitwise NOT
int notResult = ~a;     // Inverts all bits
```

#### Bitwise Tricks
```cpp
// Check if number is even
bool isEven = (number & 1) == 0;

// Set/Clear/Toggle specific bits
int setBit = number | (1 << k);
int clearBit = number & ~(1 << k);
int toggleBit = number ^ (1 << k);
```

### 3. Logical Operators
```cpp
bool x = true, y = false;

// Logical AND
bool andResult = x && y;  // false

// Logical OR
bool orResult = x || y;   // true

// Logical NOT
bool notResult = !x;      // false
```

### 4. Comparison Operators
```cpp
int a = 5, b = 10;

bool isEqual = (a == b);       // Equal to
bool notEqual = (a != b);      // Not equal to
bool greaterThan = (a > b);    // Greater than
bool lessThan = (a < b);       // Less than
bool greaterOrEqual = (a >= b);// Greater than or equal to
bool lessOrEqual = (a <= b);   // Less than or equal to
```

## 📊 Data Types

### Primitive Data Types
```cpp
// Integer Types
short shortInt = 32767;
int integer = 2147483647;
long longInt = 2147483648L;
long long bigInteger = 9223372036854775807LL;

// Floating Point Types
float decimalFloat = 3.14f;
double preciseDecimal = 3.14159;
long double extendedPrecision = 3.14159265358979L;

// Character Types
char singleChar = 'A';
wchar_t wideChar = L'B';

// Boolean
bool isTrue = true;
bool isFalse = false;
```

### Type Casting
```cpp
// Implicit Casting
int x = 10;
double y = x;  // Automatic conversion

// Explicit Casting
double z = 3.14;
int w = static_cast<int>(z);  // Truncates decimal
```

#### Type Conversion Tricks
```cpp
// String to Number
string numStr = "123";
int num = stoi(numStr);

// Number to String
int value = 456;
string strValue = to_string(value);
```

## 🔍 Variables

### Variable Scopes
```cpp
// Global Variable
int globalVar = 100;

void exampleFunction() {
    // Local Variable
    int localVar = 50;

    // Static Variable (retains value between function calls)
    static int staticVar = 0;
    staticVar++;
}
```

### Constant Variables
```cpp
// Compile-time constant
const int MAX_SIZE = 100;

// Runtime constant
constexpr double PI = 3.14159;
```

## 📦 Arrays

### 1D Arrays
```cpp
// Declaration and Initialization
int numbers[5] = {1, 2, 3, 4, 5};
int autoSizeArray[] = {10, 20, 30};

// Array Manipulation
void reverseArray(int arr[], int size) {
    for(int i = 0; i < size/2; i++) {
        swap(arr[i], arr[size-1-i]);
    }
}
```

### 2D Arrays
```cpp
// 2D Array Declaration
int matrix[3][3] = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};

// Traversing 2D Array
for(int i = 0; i < 3; i++) {
    for(int j = 0; j < 3; j++) {
        cout << matrix[i][j] << " ";
    }
}
```

## 🧩 Functions

### Function Basics
```cpp
// Simple Function
int add(int a, int b) {
    return a + b;
}

// Function with Default Arguments
int multiply(int a, int b = 1) {
    return a * b;
}

// Inline Function
inline int square(int x) {
    return x * x;
}
```

### Function Overloading
```cpp
// Multiple functions with same name, different parameters
int calculate(int a, int b) {
    return a + b;
}

double calculate(double a, double b) {
    return a * b;
}
```

## 🕹️ Control Structures

### Conditional Statements
```cpp
// If-Else
if (condition) {
    // Code block
} else if (another_condition) {
    // Another code block
} else {
    // Default block
}

// Switch Statement
switch(variable) {
    case 1:
        // Code for case 1
        break;
    case 2:
        // Code for case 2
        break;
    default:
        // Default case
}
```

### Loops
```cpp
// For Loop
for(int i = 0; i < 10; i++) {
    // Repeated code
}

// While Loop
while(condition) {
    // Repeated code
}

// Do-While Loop
do {
    // Code executed at least once
} while(condition);
```

## 🎯 Pointers

### Pointer Basics
```cpp
int x = 10;
int* ptr = &x;  // Pointer to integer

// Dereferencing
cout << *ptr;  // Prints 10

// Dynamic Memory Allocation
int* dynamicArray = new int[5];
delete[] dynamicArray;
```

## 🚧 Contribution
Contributions are welcome! Please read the Contributing Guidelines first.

## 📄 License
This project is licensed under the MIT License - see the LICENSE.md file for details.

## 🌟 Support
If you find this guide helpful, please give it a star! ⭐
