# Strings :

### 1. Ways to Represent a String :
     
     * Double quotes: "example"
     * Single quotes: 'example'
     * Backticks (template literals): `example`


### 2. String Template Literal and Usage:
    
    * Template literals are enclosed by backticks (`).
    * They allow embedding expressions with ${}.
    * Example: `Hello, ${name}!`


### 3. Iterate Over Characters in a String Using a Loop:
    
example:

```
for (let i = 0; i < str.length; i++) {
  console.log(str[i]);
}

```

# Array :

### 1. How to Create a New Array Using []:
     
     * Declare an array with square brackets: let arr = [];
     * Initialize with values: let arr = [1, 2, 3];
     * Arrays can contain mixed data types: let arr = [1, "two", true];
     * How to Read the Values in an Array (Including Nested Levels):

### 2. How to Read the Values in an Array (Including Nested Levels):
     
     * Access values by index: arr[0]
     * Nested arrays: let nestedArr = [[1, 2], [3, 4]]; nestedArr[1][0] (accesses 3)
     * Use loops or methods like forEach to read values.
     *

### 3. How to Update the Values in an Array:
     
     * Direct assignment: arr[0] = 10;
     * Using methods like push, pop, shift, unshift: arr.push(4);
     * With loops: for (let i = 0; i < arr.length; i++) { arr[i] *= 2; }


### 4. How to Use Loops to Iterate Over an Array (for & for...of):   

Example :

```
for (let i = 0; i < arr.length; i++) {
  console.log(arr[i]);
}

```

### 5. How to Access Objects Inside an Array:
     
     * Array of objects: let arr = [{name: 'Alice'}, {name: 'Bob'}];
     * Access properties: arr[0].name (accesses Alice)
     * Loop through array: for (const obj of arr) { console.log(obj.name); }


### 6. How to Pass Arrays as a Parameter:
    
    * Function definition: function printArray(arr) { arr.forEach(console.log); }
    * Function call: printArray([1, 2, 3]);


### 7. How to Clone an Array Using Spread Operator (Shallow and Deep Copy):
    
    * Shallow copy: let arrCopy = [...arr];
    * Copies top-level elements only.
    * Deep copy (for nested arrays/objects): let deepCopy = JSON.parse(JSON.stringify(arr));
    * Recursively copies all nested elements.



# Objects :

### 1. How to Create a New Object Using {}:
    
    * Create an empty object: let obj = {};
    * Initialize with key-value pairs: let obj = {name: 'Alice', age: 25};
    * How to Add New Keys to the Object:


### 2. How to Add New Keys to the Object: 

    * Using dot notation: obj.city = 'New York';
    * Using bracket notation: obj['country'] = 'USA';
    * How to Remove Keys from the Object:


### 3. How to Remove Keys from the Object:

    * Use the delete operator: delete obj.age;


### 4. How to Use Nested Objects:

    * Define nested objects: let obj = {person: {name: 'Alice', age: 25}};
    * Access nested properties: obj.person.name;
    * How to Update the Value of a Key:

### 5. How to Update the Value of a Key:

    * Using dot notation: obj.name = 'Bob';
    * Using bracket notation: obj['age'] = 30;


### 6. How to Clone an Object Using the Spread Operator (Shallow and Deep Copy):
    
    * Shallow copy: let objCopy = {...obj};
    * Deep copy: let deepCopy = JSON.parse(JSON.stringify(obj));
    * How to Pass Objects as a Parameter:


### 7. How to Pass Objects as a Parameter:

    * Function definition: function printPerson(person) { console.log(person.name); }
    * Function call: printPerson({name: 'Alice', age: 25});
    * How to Return an Object from a Function:


### 8. How to Return an Object from a Function:
   
    * Define function: function createPerson(name, age) { return {name, age}; }
    * Return object: let person = createPerson('Alice', 25);
    * How to Return Only Select Information from an Object:

### 9. How to Return Only Select Information from an Object: 
    
    * Destructure and return: let {name, age} = obj; return {name, age};
    * Using Dot Notation with an Object:


### 10. Using Dot Notation with an Object:

    * Access properties: obj.name, obj.age, obj.value

### 11. Using Array Notation with an Object:

    * Access properties: obj['name'], obj['age'], obj['value']

### 12. Using for...in Loop to Access Properties Inside the Object:

Example :
  
```
for (let key in obj) {
  console.log(key, obj[key]);
}

```

### 13. How to Handle Nested Objects with Loops:

Example :

```
for (let key in obj) {
  if (typeof obj[key] === 'object') {
    for (let nestedKey in obj[key]) {
      console.log(nestedKey, obj[key][nestedKey]);
    }
  } else {
    console.log(key, obj[key]);
  }
}

```


### 14. How to Handle Arrays Inside of Objects:

Example :

```
let obj = {name: 'Alice', hobbies: ['reading', 'hiking']};
obj.hobbies.forEach(hobby => console.log(hobby));

```






















































