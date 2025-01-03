**Unit 2** 
### 1. **Data Types (Primitive vs. Reference Types)**

#### **Definition**  
Data types define the type of data a variable can hold.  
- **Primitive Data Types**: Basic types like `int`, `float`, `char`, and `bool`. They store values directly in memory.  
- **Reference Types**: Store the address of memory where the actual data resides, e.g., pointers and objects.

---

#### **Example**  
```cpp
#include <iostream>
using namespace std;

int main() {
    // Primitive data types
    int age = 20;       // Integer
    float pi = 3.14;    // Floating-point
    char grade = 'A';   // Character
    bool isPass = true; // Boolean

    // Reference type
    int num = 5;
    int* ptr = &num; // Pointer referencing the memory address of num

    cout << "Age: " << age << endl;
    cout << "Pi: " << pi << endl;
    cout << "Grade: " << grade << endl;
    cout << "Is Pass: " << isPass << endl;
    cout << "Pointer Value: " << *ptr << endl; // Dereferencing pointer
    return 0;
}
```

**Output**:  
```
Age: 20  
Pi: 3.14  
Grade: A  
Is Pass: 1  
Pointer Value: 5  
```

---

#### **Advantages**  
- **Primitive Data Types**:  
  - Easy to use and efficient in memory.
  - Ideal for simple calculations.  
- **Reference Types**:  
  - Allow dynamic memory allocation.
  - Enable working with complex data structures like linked lists and trees.

---

#### **Disadvantages**  
- **Primitive Types**: Limited to basic functionality.  
- **Reference Types**:  
  - Prone to errors like segmentation faults.
  - Require manual memory management (e.g., `new` and `delete`).

---

#### **Applications**  
- **Primitive Types**: Calculations, condition checking, and simple applications.  
- **Reference Types**: Dynamic data structures, object-oriented programming, and memory-intensive applications.

---

#### **Best Practices**  
- Use `const` for values that should not change.  
- Initialize variables before use.  
- Avoid dangling pointers by ensuring proper memory cleanup.

---

### 2. **Variables (Scope, Lifetime, and Memory Management)**

#### **Definition**  
A variable is a container to store data.  
- **Scope**: Defines where the variable is accessible (local, global, static).  
- **Lifetime**: Refers to how long a variable exists in memory.

---

#### **Example**  
```cpp
#include <iostream>
using namespace std;

int globalVar = 10; // Global variable

void function() {
    static int staticVar = 5; // Retains value across calls
    int localVar = 2;         // Local variable
    staticVar++;
    cout << "Static Var: " << staticVar << ", Local Var: " << localVar << endl;
}

int main() {
    function();
    function();
    return 0;
}
```

**Output**:  
```
Static Var: 6, Local Var: 2  
Static Var: 7, Local Var: 2  
```

---

#### **Advantages**  
- Organized code due to scope-based access.  
- Static variables improve efficiency in repetitive tasks.

---

#### **Disadvantages**  
- Excessive global variables lead to poor maintainability.  
- Improper memory management can cause leaks.

---

#### **Applications**  
- **Local Variables**: Temporary data processing in functions.  
- **Global Variables**: Configuration flags, constants.  
- **Static Variables**: Counters or flags retained across function calls.

---

#### **Best Practices**  
- Limit global variables.  
- Use descriptive names for clarity.  
- Ensure proper memory allocation and deallocation.

---

### 3. **Operators (Arithmetic, Logical, Bitwise, Assignment)**

#### **Definition**  
Operators perform operations on variables and values. They are categorized as:  
- **Arithmetic Operators**: `+`, `-`, `*`, `/`, `%`
- **Logical Operators**: `&&`, `||`, `!`
- **Bitwise Operators**: `&`, `|`, `^`, `~`, `<<`, `>>`
- **Assignment Operators**: `=`, `+=`, `-=`, etc.

---

#### **Example**  
```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 5, b = 3;

    // Arithmetic
    cout << "Sum: " << a + b << endl;

    // Logical
    cout << "Logical AND: " << (a > 2 && b < 4) << endl;

    // Bitwise
    cout << "Bitwise AND: " << (a & b) << endl;

    // Assignment
    a += b;
    cout << "After Assignment: " << a << endl;
    return 0;
}
```

**Output**:  
```
Sum: 8  
Logical AND: 1  
Bitwise AND: 1  
After Assignment: 8  
```

---

#### **Advantages**  
- Simplify coding with compact expressions.  
- Enable low-level operations (e.g., bitwise) for performance optimization.

---

#### **Disadvantages**  
- Complex expressions may reduce readability.  
- Bitwise operations are prone to errors if misunderstood.

---

#### **Applications**  
- **Arithmetic**: Calculations and algorithms.  
- **Logical**: Condition checking in loops and statements.  
- **Bitwise**: Cryptography, image processing, and embedded systems.  
- **Assignment**: Updating variable values.

---

#### **Best Practices**  
- Use parentheses for clarity in complex expressions.  
- Avoid mixing too many operator types in one statement.

---

### 4. **Expressions (Including Operator Precedence and Evaluation)**

#### **Definition**  
An expression combines variables, operators, and values to produce a result. Operator precedence determines the order of operations, and evaluation follows this order.

---

#### **Example**  
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

**Output**:  
```
Result: 20  
Result with Parentheses: 30  
```

---

#### **Advantages**  
- Expressions enable concise coding.  
- Operator precedence ensures predictable behavior.

---

#### **Disadvantages**  
- Misunderstanding precedence can lead to bugs.  
- Complex expressions may be harder to debug.

---

#### **Applications**  
- Used in conditional statements, loops, and calculations.

---

#### **Best Practices**  
- Use parentheses to make precedence explicit.  
- Simplify expressions for readability.

---

### 5. **Arrays (Single-dimensional)**

#### **Definition**  
An array is a collection of elements of the same type stored in contiguous memory locations.

---

#### **Example**  
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

**Output**:  
```
Element 0: 1  
Element 1: 2  
Element 2: 3  
Element 3: 4  
Element 4: 5  
```

---

#### **Advantages**  
- Efficient for managing multiple data of the same type.  
- Random access to elements.

---

#### **Disadvantages**  
- Fixed size; cannot grow dynamically.  
- Risk of accessing out-of-bound elements.

---

#### **Applications**  
- Storing lists, tables, and sequences of data.

---

#### **Best Practices**  
- Initialize arrays before use.  
- Use bounds checking to avoid errors.

---

Let me know if you'd like additional details or further topics covered in this format!

