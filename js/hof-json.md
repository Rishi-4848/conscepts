# JSON :

### 1. What is JSON?
     
     * JSON (JavaScript Object Notation) is a lightweight data interchange format.
     * It is easy for humans to read and write, and easy for machines to parse and generate.

### 2. Different Methods in JSON:
    
    * JSON.stringify(): Converts a JavaScript object to a JSON string.
    * JSON.parse(): Converts a JSON string to a JavaScript object.

 Example :

 ```
let obj = {name: "Alice", age: 25};
let jsonString = JSON.stringify(obj); // '{"name":"Alice","age":25}'
let parsedObj = JSON.parse(jsonString); // {name: "Alice", age: 25}

 ```   

### 3.Difference Between Normal Object and JSON Object:

    * Normal Object: A JavaScript object used in code
    * let obj = {name: "Alice", age: 25};
    * JSON Object: A string representation of a JavaScript object
    * '{"name":"Alice","age":25}'

### 4.  How to Convert Normal Object to JSON Object and Vice Versa:

    * Convert Normal Object to JSON Object:
    * let obj = {name: "Alice", age: 25};
    * let jsonString = JSON.stringify(obj); // '{"name":"Alice","age":25}'

    * Convert JSON Object to Normal Object
    *let jsonString = '{"name":"Alice","age":25}';
    *let obj = JSON.parse(jsonString); // {name: "Alice", age: 25}



# Higher order Functions :


### 1. What is a Higher Order Function?

    * A function that takes another function as an argument, returns a function, or both.

Example :

```
function higherOrder(fn) {
  return function(x) {
    return fn(x);
  };
}
```

### 2. What is a Callback Function?

    * A function passed into another function as an argument to be executed later.

Example :

```
function greet(name) {
  console.log('Hello ' + name);
}
function processUserInput(callback) {
  let name = prompt('Please enter your name.');
  callback(name);
}
processUserInput(greet);

```

### 3. forEach:

    * Executes a provided function once for each array element.

Example :

```
[1, 2, 3].forEach(num => console.log(num));

```

### 4. map:

    * Creates a new array with the results of calling a provided function on every element.

Example :

```
let doubled = [1, 2, 3].map(num => num * 2); // [2, 4, 6]

```

### 5.filter:

    * Creates a new array with all elements that pass the test implemented by the provided function.

Example :

```
let evens = [1, 2, 3, 4].filter(num => num % 2 === 0); // [2, 4]

```

### 6.find:

    * Returns the first element in the array that satisfies the provided testing function.

Example :

```
let found = [1, 2, 3, 4].find(num => num > 2); // 3

```

### 7. reduce:

    * Executes a reducer function on each array element, resulting in a single output value.

Example :

```
let sum = [1, 2, 3, 4].reduce((acc, num) => acc + num, 0); // 10

```

### 8.every:

    * Tests whether all elements in the array pass the provided function.

Example :

```
let allEven = [2, 4, 6].every(num => num % 2 === 0); // true

```

### 9. some:

    * Tests whether at least one element in the array passes the provided function

Example :

```
let hasOdd = [1, 2, 3].some(num => num % 2 !== 0); // true

```

### 10. splice:

    * Changes the contents of an array by removing or replacing existing elements and/or adding new elements.

Example :

```
let arr = [1, 2, 3, 4];
arr.splice(2, 1, 'a'); // [1, 2, 'a', 4]

```

### 11.Shift:

     * Removes the first element from an array and returns that removed element.

Example :

```
let arr = [1, 2, 3];
let first = arr.shift(); // 1, arr is now [2, 3]

```

### 12. flat:

     * Creates a new array with all sub-array elements concatenated into it recursively up to the specified depth.

Example :

```
let arr = [1, [2, [3, 4]]];
let flattened = arr.flat(2); // [1, 2, 3, 4]

```

### 13. reverse:

    * Reverses an array in place.

Example :

```
let arr = [1, 2, 3];
arr.reverse(); // [3, 2, 1]

```

### 14. includes:

    * Determines whether an array includes a certain value among its entries.

Example:

```
let arr = [1, 2, 3];
let hasTwo = arr.includes(2); // true

```
     

### 15 .unshift:

    * Adds one or more elements to the beginning of an array and returns the new length of the array.

Example :

```
let arr = [2, 3];
arr.unshift(1); // [1, 2, 3]

```


# String Methods :


### 1. toLowerCase:

     * Converts a string to lowercase.

Example :

```
let str = "HELLO";
console.log(str.toLowerCase()); // "hello"

```

### 2. trim:

     * Removes whitespace from both ends of a string.

Example :

```
let str = "  hello  ";
console.log(str.trim()); // "hello"

```

### 3. trimEnd:

    * Removes whitespace from the end of a string.

Example :

```
let str = "hello   ";
console.log(str.trimEnd()); // "hello"

```

### 4. trimStart:

    * Removes whitespace from the beginning of a string.

Example :

```
let str = "   hello";
console.log(str.trimStart()); // "hello"

```

### 5. concat:

    * Combines two or more strings.

Example :

```
let str1 = "Hello";
let str2 = "World";
console.log(str1.concat(" ", str2)); // "Hello World"

```

### 6. endsWith:

     * Checks if a string ends with a specified substring.

Example :

```
let str = "Hello World";
console.log(str.endsWith("World")); // true

```

### 7. includes:

    * Checks if a string contains a specified substring.

Example :

```
 let str = "Hello World";
console.log(str.includes("World")); // true

```

### 8. indexOf:

     * Returns the index of the first occurrence of a specified value.

Example :

```
let str = "Hello World";
console.log(str.indexOf("o")); // 4

```

### 9. lastIndexOf:

     * Returns the index of the last occurrence of a specified value.

Example :

```
let str = "Hello World";
console.log(str.lastIndexOf("o")); // 7

```

### 10. padEnd:

     * Pads the end of a string with another string until it reaches a specified length.

Example :

```
let str = "Hello";
console.log(str.padEnd(10, "!")); // "Hello!!!!!"

```


### 11. padStart:

     * Pads the start of a string with another string until it reaches a specified length.

Example :

```
let str = "Hello";
console.log(str.padStart(10, "!")); // "!!!!!Hello"

```


### 12. repeat:

     * Repeats a string a specified number of times.

Example :

```
let str = "Hello";
console.log(str.repeat(3)); // "HelloHelloHello"

```

### 13. replace:

     * Replaces a specified value with another value in a string.

Example :

```
let str = "Hello World";
console.log(str.replace("World", "there")); // "Hello there"

```

### 14. slice:

     * Extracts a section of a string and returns it as a new string.

Example :

```
let str = "Hello World";
console.log(str.slice(0, 5)); // "Hello"

```

### 15. split:

     * Splits a string into an array of substrings based on a specified separator.

Example :

```
let str = "Hello World";
console.log(str.split(" ")); // ["Hello", "World"]

```

### 16. substring:

     * Returns a part of the string between the start and end indexes.

Example :

```
let str = "Hello World";
console.log(str.substring(0, 5)); // "Hello"

```


# Object Methods :

### 1. Object.values:

     * Returns an array of a given object's own enumerable property values.

Example :

```
let obj = {a: 1, b: 2, c: 3};
console.log(Object.values(obj)); // [1, 2, 3]

```

### 2. Object.keys:

     * Returns an array of a given object's own enumerable property names (keys).

Example :

```
let obj = {a: 1, b: 2, c: 3};
console.log(Object.keys(obj)); // ["a", "b", "c"]

```

### 3. Object.entries:

      * Returns an array of a given object's own enumerable property [key, value] pairs.

Example :

```
let obj = {a: 1, b: 2, c: 3};
console.log(Object.entries(obj)); // [["a", 1], ["b", 2], ["c", 3]]

```

### 4. Object.fromEntries:

    * Transforms a list of key-value pairs into an object.

Example :

```
 let entries = [["a", 1], ["b", 2], ["c", 3]];
let obj = Object.fromEntries(entries);
console.log(obj); // {a: 1, b: 2, c: 3}

```


# Reference Links ;
     
 * Reference link : [mdn-web-docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
