# Part 1

1. The bug was it was performing string concatenation as it was reading it as a string from DOM. Typecasting `num1` and `num2` with `Number()` fixed the issue.