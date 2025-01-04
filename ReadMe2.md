### **C Programming Question Bank with Answers**

---

## **Very Short Answer Questions (1-2 marks)**

1. **What is C language?**  
   - C is a procedural programming language developed by Dennis Ritchie in 1972. It is widely used for system programming and applications.

2. **Define a variable in C.**  
   - A variable is a named memory location used to store a value that can change during program execution.

3. **What is the use of `printf` and `scanf` in C?**  
   - `printf`: Used for outputting data to the console.  
   - `scanf`: Used for taking input from the user.

4. **What is an identifier in C?**  
   - An identifier is the name given to variables, functions, arrays, or other user-defined elements in a program.

5. **What are keywords in C? Give examples.**  
   - Keywords are reserved words in C with predefined meanings, e.g., `int`, `float`, `if`, `return`.

---

## **Short Answer Questions (3-5 marks)**

1. **Explain the structure of a C program.**  
   - A C program generally consists of:
     1. **Preprocessor directives**: Includes libraries (e.g., `#include <stdio.h>`).
     2. **Main function**: Entry point of the program.
     3. **Statements**: Logical operations within functions.
     Example:
     ```c
     #include <stdio.h>
     int main() {
         printf("Hello, World!");
         return 0;
     }
     ```

2. **Differentiate between `while` and `do-while` loops.**  
   | **Feature**        | **`while`**                          | **`do-while`**                      |
   |--------------------|--------------------------------------|--------------------------------------|
   | **Execution**      | Condition is checked first.         | Executes at least once before check.|
   | **Syntax**         | `while (condition) { ... }`         | `do { ... } while (condition);`     |

3. **Write a program to calculate the sum of numbers from 1 to N using a loop.**
   ```c
   #include <stdio.h>
   int main() {
       int n, sum = 0;
       printf("Enter a number: ");
       scanf("%d", &n);
       for (int i = 1; i <= n; i++) {
           sum += i;
       }
       printf("Sum = %d\n", sum);
       return 0;
   }
   ```

4. **What are pointers? Mention their uses.**  
   - A pointer is a variable that stores the memory address of another variable.
   - Uses:
     - Dynamic memory allocation.
     - Passing arguments by reference to functions.
     - Accessing arrays and strings efficiently.

5. **Explain file modes in C.**  
   - `"r"`: Open for reading. File must exist.
   - `"w"`: Open for writing. Creates a new file or truncates an existing one.
   - `"a"`: Open for appending data to the file.
   - `"r+"`, `"w+"`, `"a+"`: Modes for both reading and writing.

---

## **Long Answer Questions (6-10 marks)**

1. **Explain the different data types in C with examples.**  
   **Basic Data Types**:  
   | **Type**  | **Description**               | **Example**         |
   |-----------|-------------------------------|---------------------|
   | `int`     | Integer                       | `int a = 10;`       |
   | `float`   | Floating-point numbers        | `float pi = 3.14;`  |
   | `char`    | Single character              | `char c = 'A';`     |
   | `double`  | Double-precision float        | `double d = 3.1415;`|

2. **Write a program to find the largest number in an array.**
   ```c
   #include <stdio.h>
   int main() {
       int n;
       printf("Enter the number of elements: ");
       scanf("%d", &n);
       int arr[n];
       printf("Enter %d numbers: ", n);
       for (int i = 0; i < n; i++) {
           scanf("%d", &arr[i]);
       }
       int max = arr[0];
       for (int i = 1; i < n; i++) {
           if (arr[i] > max) {
               max = arr[i];
           }
       }
       printf("Largest number = %d\n", max);
       return 0;
   }
   ```

3. **Explain the concept of dynamic memory allocation with examples.**  
   - Dynamic memory allocation allows allocating memory during runtime.
   - Functions:
     - `malloc`: Allocates memory and returns a void pointer.
     - `calloc`: Allocates memory for an array and initializes all bytes to zero.
     - `realloc`: Resizes previously allocated memory.
     - `free`: Frees allocated memory.
   Example:
   ```c
   #include <stdio.h>
   #include <stdlib.h>
   int main() {
       int *ptr, n;
       printf("Enter the number of elements: ");
       scanf("%d", &n);
       ptr = (int *)malloc(n * sizeof(int));  // Allocate memory
       for (int i = 0; i < n; i++) {
           ptr[i] = i + 1;  // Initialize array
           printf("%d ", ptr[i]);
       }
       free(ptr);  // Free memory
       return 0;
   }
   ```

4. **Write a program to demonstrate file handling: Writing and Reading from a file.**
   ```c
   #include <stdio.h>
   int main() {
       FILE *fptr;
       char filename[] = "example.txt";
       char data[] = "Welcome to C programming!";
       
       // Writing to the file
       fptr = fopen(filename, "w");
       if (fptr == NULL) {
           printf("Error opening file!\n");
           return 1;
       }
       fprintf(fptr, "%s", data);
       fclose(fptr);

       // Reading from the file
       char buffer[100];
       fptr = fopen(filename, "r");
       if (fptr == NULL) {
           printf("Error opening file!\n");
           return 1;
       }
       fscanf(fptr, "%[^\n]", buffer);
       printf("Data read from file: %s\n", buffer);
       fclose(fptr);
       return 0;
   }
   ```

5. **Explain arrays in C. Write a program to reverse an array.**  
   - **Arrays**:
     - A collection of elements of the same data type.
     - Stored in contiguous memory locations.
   - **Program**:
   ```c
   #include <stdio.h>
   int main() {
       int n;
       printf("Enter the size of the array: ");
       scanf("%d", &n);
       int arr[n];
       printf("Enter %d elements: ", n);
       for (int i = 0; i < n; i++) {
           scanf("%d", &arr[i]);
       }
       printf("Reversed Array: ");
       for (int i = n - 1; i >= 0; i--) {
           printf("%d ", arr[i]);
       }
       return 0;
   }
   ```

---

This question bank provides a balance of theoretical and practical questions with answers for comprehensive preparation. Let me know if you'd like additional examples or explanations!
