# Part 2
### 1. **Would print '3'.**
This is because `var` is function scope. `i` will reach the value of `3` before it exits the loop condition (of `i < prices.length`), meaning `i` would be 3.

### 2. **150** 
As `discountedPrice` it would update throughout the for-loop and is function-scoped, it would be the updated value from the last iteration of the `for` loop. This would be `(1-0.5)*300` which is 150.

### 3. **150**
Taking the `discountedPrice` value above, it would be `Math.round(150 * 100) / 100` which is 150.

### 4. **[50,100,150]**
This is because the function takes the discounted prices (`prices[i]*0.5` in this case) and pushes them into the `discounted` array, meaning the function would return an array of the discounted prices.

### 5. **Error**

This is because `let` is block scope, and since it is declared in the loop, the call `console.log(i)` at line 12 is outside its scope, which would result in an error.

### 6. **Error**

Once again, `discountedPrice` was declared within the for-loop. As it is block-scope, it cannot be referenced outside the scope of the loop. Therefore, the `console.log(discountedPrice)` call in line 13 would result in an error.

### 7. **150**

The `finalPrice` variable was declared at the beginning of the function, therefore it is referencable within the entire function. As the values are updated within the for-loop, the `finalPrice` at the end of the function would be the `finalPrice` (discounted) value of last element in `prices`, which would be 150.

### 8. **[50,100,150]**

Once again, the function takes the discounted prices (by applying `prices[i]*0.5`) and pushes them into the `discounted` return array, which would return an array of the discounted prices.

### 9. **Error**

As mentioned in question 5, `let` is block scope, therefore referencing `i` outside the loop when it is declared and iterates through the for-loop, would error.

### 10. **3**

This is because `length` is a `const` value declared as length of [50,100,150], which is 3.

### 11. **[50,100,150]**

As the array is declared a `const`, it can be populated (as through the loop); however, it cannot be assigned to a different array. Therefore, the function would return [50,100,150] as expected.

### 12. **(A-E answered below)**

- A: `student.name` (dot notation) or `student["name"]` (using brackets)
- B: `student["Grad Year"]`
- C: `student.greeting()`
- D: `student["Favorite Teacher"].name`
- E: `student.courseLoad[0]`


### 13. **(A-H answered below)**

- A: **string `32`** (as it would convert `2` into a string and concatenate it to the string `3`)
- B: **number `1`** (would convert `3` into a number, then subtract `2` from `3` to result in `1`)
- C: **3** (`null` is treated as 0 in arithmetic)
- D: **3null** (`null` would be coverted into a string and concatenated to `'3'`)
- E: `4` (`true` is treated as `1`, therefore it would be `1+3 = 4`)
- F: `0` (`false` and `null` are both `0`, therefore it would be `0+0=0`)
- G: `3undefined` (as `undefined` would be converted to a string and concatenated to `3`)
- H: `NaN` (`3` can be converted to a number but `undefined` cannot, which results in `NaN`)


### 14. **(A-F answered below)**
- A: `true` (`2` is converetd to a number, and `2 > 1` is `true`)
- B: `false` (As both `'2'` and `'12'` are strings, it compares their first character, and as `2` is greater than `1` (from `12`), it would return false)
- C: `true` (as it is a loose equality,`'2'` would be converted to a number, and `2 == 2` is `true`)
- D: `false` (as it is a strict equality, since `'2'` and `2` are different types (of string and number respectively), the output is `false`)
- E: `false` (as `true` is converted to the number 1, and `1 == 2` is false)
- F: `true` (as it is a strict equality, `Boolean(2)` is `true`, and as `true === true` is `true`)

### 15. `==` loose equality vs. `===` strict equality
`==` is more "loose" equality; it performs any type conversions necessary (e.g. `1 == '1'` would be `true` as it would convert `'1'` to a number). `===` is a "strict" equality which does not perform any type conversions (hence `1 == '1'` would be `false`)

### 17. Result of [2,4,6]

The result would be `[2,4,6]`. `modifyArray` takes in an array `[1,2,3]`, as well as function `doSomething`. Within the function, it loops over values of `modifyArray`, applies `doSomething` (which would multiply value by 2) on each value, and pushes it to a `newArr` array, which is then returned at the end of the function. Therefore, the result would be an array of all values in `[1,2,3]` doubled, which is `[2,4,6]`.

### 19. 1, 4, 3, 2
The output displayed would be 1, 4, 3, 2 (as 2 is displayed after 1 second timeout).