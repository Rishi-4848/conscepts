# SOLID PRINCIPLES

    Object Oriented Design plays a crucial role in writing flexible, scalable, maintainable and reusable code.
    Every Developer should know SOLID principles for good object oriented design in programming.


## **SOLID principle is a acronym of the the following five priciples:**
   
   * Single Responsibility Principle (SRP)
   * Open/Closed Principle
   * Liskov’s Substitution Principle (LSP)
   * Interface Segregation Principle (ISP)
   * Dependency Inversion Principle (DIP)


### Single Responsibility Principle (SRP) :
    
    This principle states that “A class should have only one reason to change” which means every class should have a single responsibility or single job or single purpose.

### Example:
  
```
  // created a seperate class for the user info

     class User(){
        constructor(name,email){
               this.name = name;
               this.email = email;
        }

        getUserInfo(){
            return `name : ${this.name} , email : ${this.email}`
        }
     }

  // created a seperate class for the user authentication

     class Auth(){
        constructor(password){
            this.password = password;
        }

        authenticate(inputPassword){
            return this.password === password
        }
     }

     const user1 = new user('rishi','rishi@gmail.com')
     const auth1 = new Auth('rishi1234')
  
  //output 

  console.log(user1.getUserInfo())
 // name : rishi , email : rishi@gmail.com

  console.log(auth1.authenticate('rishi1234'))
  // true
    
```

### Open/Closed Principle :
    
    This principle states that “Software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification” which means you should be able to extend a class behavior, without modifying it.

### Example:

```
// created a class shape

class Shape {
  calculateArea() {
    throw new Error('This method should be overridden!');
  }
}

//extended a rectangle class to shape class

class Rectangle extends Shape {
  constructor(width, height) {
    super();
    this.width = width;
    this.height = height;
  }

  calculateArea() {
    return this.width * this.height;
  }
}

//extended a circle class to shape class

class Circle extends Shape {
  constructor(radius) {
    super();
    this.radius = radius;
  }

  calculateArea() {
    return Math.PI * Math.pow(this.radius, 2);
  }
}

// Usage
const shapes = [
  new Rectangle(10, 20),
  new Circle(5)
];

// now each shape will try to acces its own calculate area method..

// we can add even more classes of shapes without modifying the existing code

shapes.forEach(shape => {
  console.log(shape.calculateArea());
});

```

### Liskov’s Substitution Principle (LSP) :

    according to this principle “Derived or child classes must be substitutable for their base or parent classes“. This principle ensures that any class that is the child of a parent class should be usable in place of its parent without any unexpected behavior.

### Example :

```

// created a bird class  with move method

class Bird {
  move() {
    console.log('I can move!');
  }
}

//flyingbird class is extended to bird class , so it can access the move method

class FlyingBird extends Bird {
  fly() {
    console.log('I can fly!');
  }
}

//sparrow is extended to flyingbird class , so it can access both flyingbird and bird classes

class Sparrow extends FlyingBird {}

// nonflyingbird class is extended to bird class , so it can access only bird class

class NonFlyingBird extends Bird {}

//penguin class is extended to nonflyingbird class 

class Penguin extends NonFlyingBird {
  swim() {
    console.log('I can swim!');
  }
}

// Usage

function makeBirdMove(bird) {
  bird.move();
}

const sparrow = new Sparrow();
const penguin = new Penguin();

makeBirdMove(sparrow); // I can move!
makeBirdMove(penguin); // I can move!

function makeBirdFly(flyingBird) {
  flyingBird.fly();
}

makeBirdFly(sparrow); // I can fly!

// Penguins are not passed to makeBirdFly, so no error occurs

```



### Interface Segregation Principle (ISP) :
    
    This principle is the first principle that applies to Interfaces instead of classes in SOLID and it is similar to the single responsibility principle. It states that “do not force any client to implement an interface which is irrelevant to them“.

### Example :
    
```
//  class coder with a method writecode()

class Coder {
  writeCode() {
    throw new Error('Method not implemented');
  }
}

// class tester with a method writeTestCases()

class Tester {
  writeTestCases() {
    throw new Error('Method not implemented');
  }
}

//class developer extended to coder , so it access  coder methods

class Developer extends Coder {
  writeCode() {
    console.log('Writing code');
  }
}

// class quality assurance extended to tester ,so it can access tester methods

class QualityAssurance extends Tester {
  writeTestCases() {
    console.log('Writing test cases');
  }
}

// Usage
const dev = new Developer();
const qa = new QualityAssurance();

dev.writeCode(); // Writing code

qa.writeTestCases(); // Writing test cases

```


### Dependency Inversion Principle (DIP) :
    
    The Dependency Inversion Principle (DIP) is a principle in object-oriented design that states that “High-level modules should not depend on low-level modules. Both should depend on abstractions“. Additionally, abstractions should not depend on details. Details should depend on abstractions.

### Example :

```

class IDeveloper{

    develop(){
        throw new Error('Method not implemented')
    }

 class FrontendDeveloper extends Ideveloper{
    
    develop(){
        console.log('developing frontend')
    }
 }   

 class BackendDeveloper extends IDeveloper{
     
     develop(){
        console.log('developing backend')
     }
 }
}

class Project {
    
    constructor(developers){
         this.developers = developers
    }

    develop(){
        this.developers.forEach(developer => developer.develop())
    }
}


const developers = [
    new FrontendDeveloper(),
    new BackendDeveloper()
]

const project = new Project(developers)

project.develop()
```


# CONCLUSION :

    *  Implementing the SOLID principles leads to software systems that are easier to maintain, test, and extend. 
    *  These principles guide developers in crafting code that is more intuitive and adaptable, ultimately leading to higher-quality        
        software and more efficient development processes. 
    *  Embracing SOLID principles is a step towards achieving sustainable and scalable software architecture.



## REFERENCES :
  
  * Reference Link 1 : [website](https://www.digitalocean.com/community/conceptual-articles/s-o-l-i-d-the-first-five-principles-of-object-oriented-design)
  * Reference Link 2 : [videolink](https://www.youtube.com/watch?v=HLFbeC78YlU&list=PL6n9fhu94yhXjG1w2blMXUzyDrZ_eyOme&index=1)
   
