# Monkey-Go Language

## Introduction
Monkey-Go is an educational interpreter inspired by the monkey programming language, showcasing a dynamically-typed language with:
- Variables and basic data types
- Functions and closures
- Arrays and hash maps
- Built-in functions
- Control flow statements

## Quick Start
```
let greeting = "Hello, World!";
puts(greeting);
```
## Data Types

### Integers
```
let age = 25;
let negative = -10;
```

### Strings
```
let name = "Alice";
let message = "Hello " + name;
```

### Booleans
```
let isActive = true;
let isComplete = false;
```

### Arrays
```
let numbers = [1, 2, 3, 4, 5];
let mixed = [1, "hello", true];

// Accessing elements
let first = numbers[0];  // 1

// Modifying elements
numbers[0] = 10;  // [10, 2, 3, 4, 5]
```

### Hash Maps
```
let person = {"name": "John", "age": 30};

// Accessing values
let name = person["name"];
```

## Variables

### Declaration
```

let x = 10;
let name = "Alice";
let isValid = true;
```
### Assignment
```
let x = 5;
x = 10;  // Reassignment

let arr = [1, 2, 3];
arr[0] = 99;  // Modify array element

let hash = {"key": "value"};
hash["key"] = "new value";  // Modify hash value
```
## Functions

### Function Definition
```
let add = fn(a, b) {
    return a + b;
};

let greet = fn(name) {
    return "Hello, " + name + "!";
};
```

### Function Calls
```
let result = add(5, 3);  // 8
let message = greet("World");  // "Hello, World!"
```

### Higher-Order Functions
```
let apply = fn(f, x, y) {
    return f(x, y);
};

let result = apply(add, 2, 3);  // 5
```
## Control Flow

### If Expressions
```
let x = 10;
let result = if (x > 5) {
    "greater than 5"
} else {
    "less than or equal to 5"
};
```

### Conditional Assignment
```
let status = if (user.isActive) { "active" } else { "inactive" };
```
## Built-in Functions

### Array Functions

#### `len(array)` - Get array length
```
let arr = [1, 2, 3];
let length = len(arr);  // 3
```

#### `first(array)` - Get first element
```
let arr = [1, 2, 3];
let firstElement = first(arr);  // 1
```

#### `last(array)` - Get last element
```
let arr = [1, 2, 3];
let lastElement = last(arr);  // 3
```

#### `rest(array)` - Get all elements except first
```
let arr = [1, 2, 3, 4];
let remaining = rest(arr);  // [2, 3, 4]
```

#### `push(array, element)` - Add element to array (mutates original)
```
let arr = [1, 2, 3];
push(arr, 4);  // arr is now [1, 2, 3, 4]
```

### String Functions

#### `len(string)` - Get string length
```
let text = "hello";
let length = len(text);  // 5
```

### Output Function

#### `puts(...)` - Print values
```
puts("Hello, World!");
puts(42, true, [1, 2, 3]);
```
## Operators

### Arithmetic Operators
```
let a = 10;
let b = 3;

let sum = a + b;        // 13
let difference = a - b; // 7
let product = a * b;    // 30
let quotient = a / b;   // 3
```

### Comparison Operators
```
let x = 5;
let y = 10;

let equal = x == y;     // false
let notEqual = x != y;  // true
let less = x < y;       // true
let greater = x > y;    // false
```

### Logical Operators
```
let isTrue = !false;    // true
let negative = -42;     // -42
let positive = +42;     // 42
```

### Assignment Operators
```
let x = 10;
x = 20;                 // Simple assignment

let arr = [1, 2, 3];
arr[0] = 99;           // Index assignment
```
## Examples

### Factorial Function
```
let factorial = fn(n) {
    if (n <= 1) {
        return 1;
    } else {
        return n * factorial(n - 1);
    }
};

let result = factorial(5);  // 120
```

### Array Processing
```
let numbers = [1, 2, 3, 4, 5];

// Double all numbers
let i = 0;
let doubled = [];
while (i < len(numbers)) {
    push(doubled, numbers[i] * 2);
    i = i + 1;
}
// doubled is [2, 4, 6, 8, 10]
```

### Working with Hash Maps
```
let person = {
    "name": "Alice",
    "age": 30,
    "city": "New York"
};

// Update information
person["age"] = 31;
person["occupation"] = "Engineer";

puts("Name:", person["name"]);
puts("Age:", person["age"]);
```
## Language Grammar

### Expressions
- Literals: integers, strings, booleans, arrays, hash maps
- Identifiers: variable names
## Language Grammar

### Expressions
- Literals: integers, strings, booleans, arrays, hash maps
- Identifiers: variable names
- Prefix expressions: `!expr`, `-expr`, `+expr`
- Infix expressions: `left + right`, `left == right`, etc.
- Call expressions: `function(arg1, arg2)`
- Index expressions: `array[index]`, `hash[key]`

### Statements
- Let statements: `let identifier = expression;`
- Return statements: `return expression;`
- Expression statements: `expression;`
- Prefix expressions: `!expr`, `-expr`, `+expr`
- Infix expressions: `left + right`, `left == right`, etc.
- Call expressions: `function(arg1, arg2)`
- Index expressions: `array[index]`, `hash[key]`

### Statements
- Let statements: `let identifier = expression;`
- Return statements: `return expression;`
- Expression statements: `expression;`
```
// Modifying values
person["age"] = 31;
```
