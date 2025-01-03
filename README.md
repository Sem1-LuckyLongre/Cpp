
# C++ Unit 2

This guide covers fundamental C++ concepts with detailed explanations, examples, and tips on operators, data types, control structures, and more.

---

## 1. **Operators (Arithmetic, Logical, Bitwise, Assignment)**

### **Arithmetic Operators**

- **`+` (Addition)**: Adds two operands.
- **`-` (Subtraction)**: Subtracts second operand from the first.
- **`*` (Multiplication)**: Multiplies two operands.
- **`/` (Division)**: Divides the numerator by the denominator.
- **`%` (Modulus)**: Returns the remainder of division.

#### **Example:**
```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10, b = 5;
    cout << "Addition: " << (a + b) << endl;
    cout << "Subtraction: " << (a - b) << endl;
    cout << "Multiplication: " << (a * b) << endl;
    cout << "Division: " << (a / b) << endl;
    cout << "Modulus: " << (a % b) << endl;
    return 0;
}
```

---

### **Logical Operators**

- **`&&` (AND)**: Returns true if both operands are true.
- **`||` (OR)**: Returns true if at least one operand is true.
- **`!` (NOT)**: Reverses the logical state of its operand.

#### **Example:**
```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 5, b = 10, c = 0;

    if (a > 0 && b > 0) {
        cout << "Both a and b are positive." << endl;
    }

    if (a > 0 || c > 0) {
        cout << "At least one of a or c is positive." << endl;
    }

    if (!c) {
        cout << "c is zero." << endl;
    }

    return 0;
}
```

---

### **Bitwise Operators**

- **`&` (AND)**: Performs bitwise AND operation.
- **`|` (OR)**: Performs bitwise OR operation.
- **`^` (XOR)**: Performs bitwise XOR operation.
- **`~` (NOT)**: Performs bitwise NOT operation.
- **`<<` (Left Shift)**: Shifts bits to the left.
- **`>>` (Right Shift)**: Shifts bits to the right.

#### **Example:**
```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 5, b = 3; // Binary: a = 0101, b = 0011

    cout << "a & b: " << (a & b) << endl;  // Output: 1 (0001)
    cout << "a | b: " << (a | b) << endl;  // Output: 7 (0111)
    cout << "a ^ b: " << (a ^ b) << endl;  // Output: 6 (0110)
    cout << "~a: " << (~a) << endl;        // Output: -6 (Two's complement)
    cout << "a << 1: " << (a << 1) << endl; // Output: 10 (1010)
    cout << "a >> 1: " << (a >> 1) << endl; // Output: 2 (0010)

    return 0;
}
```

#### **Tricks:**
- **Check even/odd:** `(x & 1) == 0` checks if `x` is even.
- **Swap without temp variable:** `a = a ^ b; b = a ^ b; a = a ^ b;`
- **Masking:** Use `&` with a mask to extract specific bits.
- **Set bits:** Use `| mask` to set specific bits.
- **Shift for multiplication/division by 2:** Use `<<` and `>>` for efficient power-of-2 operations.

---

### **Assignment Operators**

- **`=` (Simple Assignment)**: Assigns the value of the right operand to the left operand.
- **`+=`, `-=`**, etc.: Compound assignment operators.

#### **Example:**
```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 5, b = 3;

    a += b; // Equivalent to a = a + b;
    cout << "After Assignment: " << a << endl;
    return 0;
}
```

---

## 2. **Arrays (Single-dimensional)**

### **Definition**

An array is a collection of elements of the same type, stored in contiguous memory locations.

#### **Example:**
```cpp
#include <iostream>
using namespace std;

int main() {
    int arr[5] = {1, 2, 3, 4, 5};

    for (int i = 0; i < 5; i++) {
        cout << "Element " << i << ": " << arr[i] << endl;
    }
    return 0;
}
```

### **Advantages**

- Efficient memory usage for storing data.
- Allows direct access to elements.

### **Disadvantages**

- Fixed size; cannot grow dynamically.

---

## 3. **Type Casting**

### **Definition**

Type casting is the conversion of one data type to another.

- **Implicit Casting**: Automatic conversion by the compiler.
- **Explicit Casting**: Manual conversion using cast operators.

#### **Example:**
```cpp
#include <iostream>
using namespace std;

int main() {
    double d = 9.8;
    int i = static_cast<int>(d); // Explicit casting
    cout << "Converted value: " << i << endl;
    return 0;
}
```

---

## 4. **Expressions (Operator Precedence and Evaluation)**

### **Definition**

An expression combines variables, operators, and values to produce a result. Operator precedence determines the order of operations.

#### **Example:**
```cpp
#include <iostream>
using namespace std;

int main() {
    int result = 10 + 5 * 2; // Precedence: Multiplication first
    cout << "Result: " << result << endl;

    result = (10 + 5) * 2; // Parentheses change precedence
    cout << "Result with Parentheses: " << result << endl;
    return 0;
}
```

---

## 5. **Control Structures**

### **Decision Making Constructs**

- **`if`**, **`else`**: Used for conditional branching.
- **`switch`**: Allows multi-way branching based on multiple conditions.

#### **Example:**
```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 5;
    if (a > 0) {
        cout << "Positive number" << endl;
    } else {
        cout << "Negative number" << endl;
    }
    return 0;
}
```

---

### **Iteration (Loops)**

- **`for` loop**: Iterates a fixed number of times.
- **`while` loop**: Iterates while a condition is true.
- **`do-while` loop**: Iterates at least once, then continues while a condition is true.

#### **Example:**
```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 0; i < 5; i++) {
        cout << "Iteration " << i << endl;
    }
    return 0;
}
```

---

## 6. **Functions**

### **Definition**

A function is a block of code that performs a specific task and can be called multiple times.

#### **Example:**
```cpp
#include <iostream>
using namespace std;

void greet() {
    cout << "Hello, World!" << endl;
}

int main() {
    greet();
    return 0;
}
```

---

## 7. **Input-Output Statements**

- **`cin`**: Used to get input from the user.
- **`cout`**: Used to display output.

#### **Example:**
```cpp
#include <iostream>
using namespace std;

int main() {
    int num;
    cout << "Enter a number: ";
    cin >> num;
    cout << "You entered: " << num << endl;
    return 0;
}
```

---

## Conclusion

This guide provides an in-depth explanation of key C++ concepts, including operators, arrays, functions, control structures, and input-output operations. It includes examples, tips, and best practices to help enhance your understanding of C++ programming.

