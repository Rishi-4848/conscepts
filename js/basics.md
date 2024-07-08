>  **In javascript data types are categorized into two types :**
     
     * Primitive Data Types
     * Non-Primitive Data types

#   Primitive Data Types :
   
###   1. Number :
     
     * Representing both integer and float numbers.
     * Example :  let age = 25 ;  const price = 12.23 ;

### 2. String :

     * Represents a sequence of characters.
     * Example : let name = 'rishi' ; const greet = 'hello';

### 3. Boolean :
     
     * Represents logical values like 'true' and 'false'.
     * Example :  let isActive = false ; let isAvailable  = true;

### 4. undefined :
     
     * Represents a variable that is declared , but not yet assigned a value.
     * Example : let k ; console.log(k) ; => undefined

### 5. Null :
     
     * Represents the intentional absence of a object value.
     * Example : let obj =null;

### 6. NaN :
    
    * Represents a value that is not a legal value.
    * Example let value  = Math.sqrt(-1) => NaN



#  Non-Primitive Data Types :
    
### 1. Object :

    * Represents a collection of key-value pairs.
    * Example :

```
let obj = {
    name : 'rishi'
    age : '23'
}
```    

### 2. Array ;
    
    * Represents a order list of values.
    * Example : let numbers = [2,5,1,3,7,8]

### 3. Function :
    
    * Represents a block of code designed to perform a particular task.
    * Example :

```
function greet(){
    console.log( "hii.. ! Rishi")
}

```


# Variable Declaration : 
   
 > **we can declare a variable in three different ways :**

    
### 1. Var :
   
    * Scope : var is a function scope variable declared with 'var'. it is accesable with in the function it is declared or globally if 
             it is declared globally.

    * Hoisting : Variables declared with var are hoisted to the top of their scope. This means you can use a var variable before its 
                declaration, though it will be undefined until the declaration is encountered.

    * Assignment : Variables declared with 'var' can be reassigned a new value in its scope , without redeclaring the variable.    


### 2. Let :
   
    * Scope : let is block-scoped. This means that a variable declared with let is only accessible within the block  it was declared in.

    * Hoisting : Variables declared with 'let' are not hoisted .Using the variable before the declaration results in a ReferenceError.

    * Assignment :  Variables declared with 'let' can be reassigned a new value in its scope , without redeclaring the variable.  

### 3. Const :
   
    * Scope : const is block-scoped, similar to let.

    * Hoisting : Variables declared with const are not hoisted . Using the variable before the declaration results in a ReferenceError.

    * Assignment : Variables declared with const must be assigned an initial value at the time of declaration, and their value cannot be 
                   reassigned. However, the contents of objects and arrays declared with const can be modified.



# Loops :


### 1. For Loop : 
   
 > **The for loop  is a control flow statement that allows you to execute a block of code a specified number of times.**

 Example :

 ```
 const fruits = ['apple', 'banana', 'cherry'];

for (let i = 0; i < fruits.length; i++) {
  console.log(fruits[i]);
}

 ```


 ### 2. While Loop :

 > **The while loop  is another control flow statement that allows you to execute a block of code as long as a specified condition is true.**

 Example :

 ```
const fruits = ['apple', 'banana', 'cherry'];
let index = 0;

while (index < fruits.length) {
  console.log(fruits[index]);
  index++;
}

 ```


### 3. for of loop :

> **The for...of loop  provides a simpler and more readable way to iterate over iterable objects, such as arrays, strings, maps, sets, and other collections**

Example ;

```
const person = {
  name: 'Alice',
  age: 25,
  city: 'Wonderland'
};

// Using Object.keys()
for (const key of Object.keys(person)) {
  console.log(key);
}

// Using Object.values()
for (const value of Object.values(person)) {
  console.log(value);
}

// Using Object.entries()
for (const [key, value] of Object.entries(person)) {
  console.log(`${key}: ${value}`);
}


```


### 4.for in loop :

> **The for...in loop  is used to iterate over the enumerable properties of an object. It loops through the property names (keys) of an object, allowing you to execute a block of code for each property.**

Example :

```
const person = {
  name: 'Alice',
  age: 25,
  city: 'Wonderland'
};

for (const key in person) {
  if (key === 'age') {
    continue; // Skip the 'age' property
  }
  console.log(`${key}: ${person[key]}`);
  if (key === 'city') {
    break; // Exit the loop after 'city'
  }
}

```


# Conditionals :

### 1. If Else :

> **The if...else statement is used to execute a block of code based on a specified condition. It allows you to make decisions in your code and execute different blocks of code based on different conditions.**

Example :

```
const number = 10;

if (number > 0) {
  console.log('The number is positive.');
} else if (number < 0) {
  console.log('The number is negative.');
} else {
  console.log('The number is zero.');
}

```


### 2. Switch :

> **The switch statement is used to perform different actions based on different conditions. It is an alternative to using multiple if...else if statements and can make your code more readable when you need to compare a single variable against multiple values.**

Example :

```
const fruit = 'banana';

switch (fruit) {
  case 'apple':
  case 'banana':
  case 'cherry':
    console.log('This is a fruit.');
    break;
  default:
    console.log('This is not a fruit.');
}

```


### 3.Ternary Operator :

>**The ternary operator, also known as the conditional operator, is a shorthand way to write an if...else statement in JavaScript.**

Example :

```
const number = 4;
const result = (number % 2 === 0) ? 'even' : 'odd';
console.log(result); // Output: even

```


# Operators:

### 1.Mathematical Operators:

 > **Mathematical operators are used to perform arithmetic operations.**

    * Addition (+): Adds two numbers.
    * Subtraction (-): Subtracts one number from another.
    *  Multiplication (*): Multiplies two numbers.
    *  Division (/): Divides one number by another.
    * Modulus (%): Returns the remainder of a division.
    * Exponentiation (**): Raises the first operand to the power of the second operand.

 Example :

 ```
const a = 10;
const b = 3;

console.log(a + b); // 13
console.log(a - b); // 7
console.log(a * b); // 30
console.log(a / b); // 3.3333333333333335
console.log(a % b); // 1
console.log(a ** b); // 1000

 ```   

### 2.Logical Operators :

 > **Logical operators are used to combine or invert boolean values.**
    
     * AND (&&): Returns true if both operands are true.
     * OR (||): Returns true if at least one of the operands is true.
     * NOT (!): Inverts the boolean value.


### 3.Comparison Operators :

 > **Comparison operators are used to compare two values and return a boolean value (true or false).**
     
     *  Equal (==): Checks if two values are equal (loose equality, type conversion allowed).
     *  Strict Equal (===): Checks if two values are equal (strict equality, no type conversion).
     *  Not Equal (!=): Checks if two values are not equal (loose inequality, type conversion allowed).
     *  Strict Not Equal (!==): Checks if two values are not equal (strict inequality, no type conversion).
     *  Greater Than (>): Checks if the left value is greater than the right value.
     *  Greater Than or Equal (>=): Checks if the left value is greater than or equal to the right value.
     *  Less Than (<): Checks if the left value is less than the right value.
     *  Less Than or Equal (<=): Checks if the left value is less than or equal to the right value.

 Example :

 ```
const num1 = 5;
const num2 = 10;

console.log(num1 == '5'); // true (loose equality)
console.log(num1 === '5'); // false (strict equality)
console.log(num1 != 10); // true (loose inequality)
console.log(num1 !== 10); // true (strict inequality)
console.log(num1 > num2); // false
console.log(num1 >= 5); // true
console.log(num1 < num2); // true
console.log(num1 <= 5); // true

 ```    


 # Functions :

 ### 1. How to declare a function?

  > **Use the function keyword followed by the function name and parentheses for parameters, then curly braces {} for the function body.**

  Example :

  ```
function greet(name) {
  console.log(`Hello, ${name}!`);
}

  ```

### 2. What are parameters, arguments?

> **Parameters are placeholders in the function definition. Arguments are the actual values passed into the function when it's called.**

Example :

```
function multiply(a, b) { // 'a' and 'b' are parameters
  return a * b;
}

multiply(3, 4); // 3 and 4 are arguments

```

### 3. What is return statement?

>  **The return statement ends the function execution and specifies the value to be returned to the function caller.**

Example:

```
function square(x) {
  return x * x; // Returns the square of 'x'
}

const result = square(5); // result will be 25

```

### 4.  How to call a function?

> **Simply use the function name followed by parentheses () with arguments inside if there are any.**

Example:

```
greet('Alice'); // Calling the 'greet' function with argument 'Alice'
```

### 5. What are the different types of functions?
     
     * Named function: Defined with a function name.
     * Anonymous function: Defined without a name (often assigned to variables or used as callbacks).
     * Arrow function: A concise way to write functions introduced in ES6.

Example :

```
// Named function
function sayHello(name) {
  console.log(`Hello, ${name}!`);
}

// Anonymous function assigned to a variable
const greet = function(name) {
  console.log(`Hello, ${name}!`);
};

// Arrow function
const add = (a, b) => a + b;

```













