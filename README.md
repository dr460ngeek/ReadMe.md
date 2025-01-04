### Full Revision Content for "Programming for Problem Solving Using C"

---

## **1. Introduction to C Language**
### **C Language Background**
- C was developed by Dennis Ritchie in 1972 at Bell Labs.
- Known for:
  - Efficiency and simplicity.
  - System-level programming (e.g., operating systems).
  - Portability and modularity.
- Features:
  - Procedural language.
  - Rich library support.
  - Support for pointers and direct memory access.

### **Structure of a C Program**
A basic C program structure:
```c
#include <stdio.h>  // Header file for standard I/O

int main() {        // Main function, program execution starts here
    printf("Hello, World!\n"); // Print statement
    return 0;       // Return 0 to indicate successful execution
}
```

Key components:
1. **Preprocessor directives** (`#include`): Include header files.
2. **Main function**: Entry point of every C program.
3. **Statements**: Program instructions.

### **Identifiers**
- Names used for variables, functions, and arrays.
- Rules:
  - Can contain letters, digits, and underscores.
  - Must begin with a letter or underscore.
  - Case-sensitive.
  - Cannot use reserved keywords.

### **Data Types**
- **Basic types**: `int`, `float`, `char`, `double`.
- **Derived types**: Arrays, Pointers, Structures, Unions.
- Example:
```c
int age = 21;       // Integer type
float salary = 50000.5; // Floating-point type
char grade = 'A';   // Character type
```

### **Variables and Constants**
- **Variable**: Storage location with a name.
  - Declaration: `int num;`
  - Initialization: `num = 5;`
- **Constant**: Fixed value that doesn’t change during execution.
  - Declared using `const`: `const int MAX = 100;`

### **Input/Output Statements**
- Input: `scanf` function.
- Output: `printf` function.
Example:
```c
#include <stdio.h>
int main() {
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);   // Input integer
    printf("You entered: %d\n", num); // Output integer
    return 0;
}
```

---

## **2. Arithmetic Operators and Expressions**
### **Operators in C**
1. **Arithmetic Operators**:
   - Addition (`+`), Subtraction (`-`), Multiplication (`*`), Division (`/`), Modulus (`%`).
2. **Relational Operators**:
   - Greater than (`>`), Less than (`<`), Equal to (`==`), Not equal to (`!=`).
3. **Logical Operators**:
   - AND (`&&`), OR (`||`), NOT (`!`).

### **Evaluating Expressions**
Expressions are evaluated using operator precedence:
- **Precedence**: Determines which operator is applied first.
  - Example: `3 + 4 * 5` is evaluated as `3 + (4 * 5)`.

### **Type Conversions**
- **Implicit Conversion (Type Promotion)**:
  - Smaller types (e.g., `int`) are converted to larger types (`float`).
- **Explicit Conversion (Casting)**:
  - Syntax: `(type) expression`
  - Example:
```c
int a = 10, b = 3;
float result = (float)a / b; // Casting a to float
```

---

## **3. Control Statements**
### **Conditional Statements**
1. **`if` Statement**:
   ```c
   if (condition) {
       // Code block
   }
   ```
2. **`if-else` Statement**:
   ```c
   if (condition) {
       // Code block if condition is true
   } else {
       // Code block if condition is false
   }
   ```
3. **`switch` Statement**:
   ```c
   switch (expression) {
       case value1:
           // Code block
           break;
       case value2:
           // Code block
           break;
       default:
           // Default code block
   }
   ```

### **Loops**
1. **`for` Loop**:
   ```c
   for (initialization; condition; increment) {
       // Code block
   }
   ```
2. **`while` Loop**:
   ```c
   while (condition) {
       // Code block
   }
   ```
3. **`do-while` Loop**:
   ```c
   do {
       // Code block
   } while (condition);
   ```

---

## **4. Functions**
### **User-defined Functions**
Syntax:
```c
returnType functionName(parameters) {
    // Code block
    return value; // Optional
}
```
Example:
```c
int add(int a, int b) {
    return a + b;
}
int main() {
    printf("Sum: %d\n", add(5, 3));
    return 0;
}
```

---

## **5. Arrays and Strings**
### **Arrays**
- Collection of elements of the same type.
- Declaration:
```c
int arr[5];
```
- Accessing elements:
```c
arr[0] = 10;  // Assign value
printf("%d", arr[0]);  // Access value
```

### **Strings**
- Array of characters ending with `\0`.
- Common functions:
  - `strlen()`: String length.
  - `strcpy()`: Copy string.
  - `strcat()`: Concatenate strings.
  - `strcmp()`: Compare strings.

---

## **6. Pointers**
- Pointer stores the address of another variable.
- Syntax:
```c
int *ptr, var;
ptr = &var;  // Assign address of var to ptr
```
- Accessing value:
```c
printf("%d", *ptr);  // Dereference pointer
```

---

## **7. File Handling**
### **Basic File Operations**
1. **Opening a File**:
   ```c
   FILE *fptr;
   fptr = fopen("filename.txt", "mode");
   ```
   Modes:
   - `"r"`: Read
   - `"w"`: Write
   - `"a"`: Append
2. **Reading/Writing Data**:
   ```c
   fprintf(fptr, "Hello, World!");  // Write
   fscanf(fptr, "%s", str);        // Read
   ```
3. **Closing a File**:
   ```c
   fclose(fptr);
   ```

---
