# Assignment-Parameter-passing
### Summary: Passing Parameters to Functions

Passing parameters involves providing input to a function so it can operate dynamically based on given data. This improves reusability and flexibility.

#### **Key Terminologies**:
1. **Formal Parameter**: Variables defined in the function declaration (e.g., placeholders like `int x`).
2. **Actual Parameter (Argument)**: The actual value provided when the function is called (e.g., `increment(5)` where `5` is the argument).

- **Arguments** are inputs provided to a function.
- **Parameters** are the variables that receive these inputs inside the function.

---

### **Why Parameters Are Needed**
Without parameters, functions would rely on hardcoded values or variables declared inside the function, limiting flexibility. Parameters allow functions to handle various inputs, making them versatile.

---

### **Types of Parameter Passing**
1. **Pass by Value**:
   - A copy of the variable's value is passed to the function.
   - Changes inside the function don’t affect the original variable.
   - **Use Case**: When you want to protect the original data.

   **Example**:
   ```cpp
   void increment(int num) {
       num += 1; // Only modifies the copy.
   }
   ```

2. **Pass by Reference**:
   - The function receives the memory address of the original variable.
   - Changes inside the function directly modify the original variable.
   - **Use Case**: When the function needs to modify the original variable or work with large data structures efficiently.

   **Example**:
   ```cpp
   void increment(int &num) {
       num += 1; // Directly modifies the original variable.
   }
   ```

3. **Pass by Pointer**:
   - Similar to pass by reference but uses pointers explicitly.
   - The function accesses the variable using its memory address.
   - **Use Case**: When working with arrays or dynamic memory.

   **Example**:
   ```cpp
   void increment(int *num) {
       (*num) += 1; // Modifies the variable through its pointer.
   }
   ```

---

### **Key Differences: Call by Value vs. Call by Reference**
- **Call by Value**: Creates a local copy of the variable; changes are isolated.
- **Call by Reference**: Directly works with the original variable; changes are reflected outside the function.

---

### **Summary of Use Cases**
- **Pass by Value**: Use for small, independent data when you don’t want the function to modify the original value.
- **Pass by Reference**: Use when you need the function to modify the original data or when dealing with large objects.
- **Pass by Pointer**: Use when dealing with arrays or dynamic memory for better efficiency.
