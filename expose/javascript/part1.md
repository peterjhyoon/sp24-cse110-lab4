# Part 1
### 1. **20**

As `var` is function scope, this means values added would return 20.

### 2. **20**

Once again, as `var` is function scoped, the addition to modify `result` would be applied and displayed.

### 3. **20** 

As `let` is block scope, and the addition is within the same block as the declaration, `result` would be 20.

### 4. **Error**

As `let` is block scope, and the final result is outside the conditional block, it would error (as the variable was not declared in the same scope).

### 5. **Error**

As `const` is a constant variable that cannot be modified, it would error.

### 6. **Error**

The same reason as above for 5, const variables cannot be reassigned.
