# JS Design Patterns Book, Conspects

## Each pattern should have those descriptions

*   Pattern name and a description
*   Context outline – the contexts in which the pattern is effective in responding to the users needs.
*   Problem statement – a statement of the problem being addressed so we can understand the intent of the pattern.
*   Solution – a description of how the user’s problem is being solved in an understandable list of steps and perceptions.
*   Design – a description of the pattern’s design and in particular, the user’s behavior in interacting with it
*   Implementation – a guide to how the pattern would be implemented
*   Illustrations – a visual representation of classes in the pattern (e.g. a diagram)
*   Examples – an implementation of the pattern in a minimal form
*   Co-requisites – what other patterns may be needed to support use of the pattern being described?
*   Relations – what patterns does this pattern resemble? does it closely mimic any others?
*   Known usage – is the pattern being used in the wild? If so, where and how?
*   Discussions – the team or author’s thoughts on the exciting benefits of the pattern

## The following are important when creating A NEW DESIGN PATTERN

* **How practical is the pattern?:** Ensure the pattern describes proven solutions to recurring problems rather than just speculative solutions which haven’t been qualified.
* **Keep best practices in mind:** The design decisions we make should be based on principles we derive from an understanding of best practices.
* **Our design patterns should be transparent to the user:** Design patterns should be entirely transparent to any type of user-experience. They are primarily there to serve the developers using them and should not force changes to behavior in the user-experience that would not be incurred without the use of a pattern.
* **Remember that originality is not key in pattern design:** When writing a pattern, we do not need to be the original discoverer of the solutions being documented nor do you have to worry about our design overlapping with minor pieces of other patterns. If the approach is strong enough to have broad useful applicability, it has a chance of being recognized as a valid pattern.
* **Patterns need a strong set of examples:** A good pattern description needs to be followed by an equally strong set of examples demonstrating the successful application of our pattern. To show broad usage, examples that exhibit good design principles are ideal.

## Anti-Patterns


* Describe a bad solution to a particular problem which resulted in a bad situation occurring
* Describe how to get out of said situation and how to go from there to a good solution

_“These notes are about the process of design; the process of inventing physical things which display a new physical order, organization, form, in response to function.…every design problem begins with an effort to achieve fitness between two entities: the form in question and its context. The form is the solution to the problem; the context defines the problem”_
    
### Example os Anti-Patterns are
    
    
* Polluting the global namespace by defining a large number of variables in the global context
* Passing strings rather than functions to either setTimeout or setInterval as this triggers the use of eval() internally.
* Modifying the Object class prototype (this is a particularly bad anti-pattern)
* Using JavaScript in an inline form as this is inflexible
* The use of document.write where native DOM alternatives such as document.createElement are more appropriate. document.write has been grossly misused over the years and has quite a few disadvantages including that if it's executed after the page has been loaded it can actually overwrite the page we're on, whilst document.createElement does not. We can see here for a live example of this in action. It also doesn't work with XHTML which is another reason opting for more DOM-friendly methods such as document.createElement is favorable.

# Categories of Design Patterns

_“A design pattern names, abstracts, and identifies the key aspects of a common design structure that make it useful for creating a reusable object-oriented design. The design pattern identifies the participating classes and their instances, their roles and collaborations, and the distribution of responsibilities._ 

* **Creational Design Patterns**

    _Creational design patterns focus on handling object creation mechanisms where objects are created in a manner suitable for the situation we're working in_

    * Constructor
    * Factory
    * Abstract
    * Prototype
    * Singleto
    * Builder
    
* **Structural Design Patterns**

    _Structural patterns are concerned with object composition and typically identify simple ways to realize relationships between different objects._
    
    * Decorator
    * Facade
    * Flyweight
    * Adapter
    * Proxy
    
    
* **Behavioral Design Patterns**

    _Behavioral patterns focus on improving or streamlining the communication between disparate objects in a system_

    * Iterator, 
    * Mediator, 
    * Observer
    * Visitor

## A brief note on classes

There are no classes in ES5, but since ES6 a syntactic sugar of Class is introduced
 
 ```javascript
 // A car "class"
 function Car( model ) {
  
   this.model = model;
   this.color = "silver";
   this.year = "2012";
  
   this.getInfo = function () {
     return this.model + " " + this.year;
   };
  
 }
 ```
 
 We can then instantiate the object using the Car constructor we defined above like this:
 
 ```javascript
 var myCar = new Car("ford");
  
 myCar.year = "2010";
  
 console.log( myCar.getInfo() );
 ```
 
 # Design Pattern Categorization
 
 ### Creational
 
 | Creational |	  Based on the concept of creating an object.
 | ------------------  |   ------------------------------------------ |
 |   **Class**    | | 
 | Factory Method  | This makes an instance of several derived classes based on interfaced data or events. |
 |   **Object**    | |
| Abstract Factory |	Creates an instance of several families of classes without detailing concrete classes. |
| Builder |	Separates object construction from its representation, always creates the same type of object. |
| Prototype |	A fully initialized instance used for copying or cloning. |
| Singleton |	A class with only a single instance with global access points. |
 

### Structural

| Structural |  Based on the idea of building blocks of objects.
| ------------------  |   ------------------------------------------ |
| **Class**| |
|   Adapter |	Match interfaces of different classes therefore classes can work together despite incompatible interfaces. |
| **Object**| |
|   Adapter |	Match interfaces of different classes therefore classes can work together despite incompatible interfaces. |
|   Bridge	| Separates an object's interface from its implementation so the two can vary independently. |
|   Composite |	A structure of simple and composite objects which makes the total object more than just the sum of its parts. |
|   Decorator |	Dynamically add alternate processing to objects. |
|   Facade |	A single class that hides the complexity of an entire subsystem. |
|   Flyweight |	A fine-grained instance used for efficient sharing of information that is contained elsewhere. |
|   Proxy |	A place holder object representing the true object. |

### Behavioral

|Behavioral |	  Based on the way objects play and work together. |
| ------------------  |   ------------------------------------------ |
| **Class** |    |
|   Interpreter |	A way to include language elements in an application to match the grammar of the intended language. |
|   Template Method |	Creates the shell of an algorithm in a method, then defer the exact steps to a subclass. |
| **Object** |   |
|   Chain of Responsibility |	A way of passing a request between a chain of objects to find the object that can handle the request. |
|   Command |	Encapsulate a command request as an object to enable, logging and/or queuing of requests, and provides error-handling for unhandled requests. |
|   Iterator |	Sequentially access the elements of a collection without knowing the inner workings of the collection. |
|   Mediator |	Defines simplified communication between classes to prevent a group of classes from referring explicitly to each other. |
|   Memento |	Capture an object's internal state to be able to restore it later. |
|   Observer |	A way of notifying change to a number of classes to ensure consistency between the classes. |
|   State |	Alter an object's behavior when its state changes. |
|   Strategy |	Encapsulates an algorithm inside a class separating the selection from the implementation. |
|   Visitor |	Adds a new operation to a class without changing the class. |

# JavaScript Design Patterns

The patterns to be explored are

* Constructor Pattern
* Module Pattern
* Revealing Module Pattern
* Singleton Pattern
* Observer Pattern
* Mediator Pattern
* Prototype Pattern
* Command Pattern
* Facade Pattern
* Factory Pattern
* Mixin Pattern
* Decorator Pattern
* Flyweight Pattern

## The Constructor Pattern 

In classical object-oriented programming languages, a constructor is a special method used to initialize a newly created object once memory has been allocated for it. In JavaScript, as almost everything is an object, we're most often interested in object constructors.

### Object Creation

#### 3 ways to create

```javascript
// Each of the following options will create a new empty object:
 
var newObject = {};
 
// or
var newObject = Object.create( Object.prototype );
 
// or
var newObject = new Object();
```

#### 4 ways to assign keys and values to object

```javascript
// ECMAScript 3 compatible approaches
 
// 1. Dot syntax
 
// Set properties
newObject.someKey = "Hello World";
 
// Get properties
var value = newObject.someKey;
 
 
 
// 2. Square bracket syntax
 
// Set properties
newObject["someKey"] = "Hello World";
 
// Get properties
var value = newObject["someKey"];
 
 
 
// ECMAScript 5 only compatible approaches
// For more information see: http://kangax.github.com/es5-compat-table/
 
// 3. Object.defineProperty
 
// Set properties
Object.defineProperty( newObject, "someKey", {
    value: "for more control of the property's behavior",
    writable: true,
    enumerable: true,
    configurable: true
});
 
// If the above feels a little difficult to read, a short-hand could
// be written as follows:
 
var defineProp = function ( obj, key, value ){
  var config = {
    value: value,
    writable: true,
    enumerable: true,
    configurable: true
  };
  Object.defineProperty( obj, key, config );
};
 
// To use, we then create a new empty "person" object
var person = Object.create( Object.prototype );
 
// Populate the object with properties
defineProp( person, "car", "Delorean" );
defineProp( person, "dateOfBirth", "1981" );
defineProp( person, "hasBeard", false );
 
console.log(person);
// Outputs: Object {car: "Delorean", dateOfBirth: "1981", hasBeard: false}
 
 
// 4. Object.defineProperties
 
// Set properties
Object.defineProperties( newObject, {
 
  "someKey": {
    value: "Hello World",
    writable: true
  },
 
  "anotherKey": {
    value: "Foo bar",
    writable: false
  }
 
});
 
// Getting properties for 3. and 4. can be done using any of the
// options in 1. and 2.
```

These methods can be used for inheritance as follows

```javascript
// Usage:
 
// Create a race car driver that inherits from the person object
var driver = Object.create( person );
 
// Set some properties for the driver
defineProp(driver, "topSpeed", "100mph");
 
// Get an inherited property (1981)
console.log( driver.dateOfBirth );
 
// Get the property we set (100mph)
console.log( driver.topSpeed );
```

### Basic Constructors

#### An example of constructor can be

```javascript
function Car( model, year, miles ) {
 
  this.model = model;
  this.year = year;
  this.miles = miles;
 
  this.toString = function () {
    return this.model + " has done " + this.miles + " miles";
  };
}
 
// Usage:
 
// We can create new instances of the car
var civic = new Car( "Honda Civic", 2009, 20000 );
var mondeo = new Car( "Ford Mondeo", 2010, 5000 );
 
// and then open our browser console to view the
// output of the toString() method being called on
// these objects
console.log( civic.toString() );
console.log( mondeo.toString() );
```

**The above is a simple version of the constructor pattern but it does suffer from some problems. One is that it makes inheritance difficult and the other is that functions such as toString() are redefined for each of the new objects created using the Car constructor. This isn't very optimal as the function should ideally be shared between all of the instances of the Car type.**

There is an alternative way that eliminates those problems

## Constructors With Prototypes

```javascript
function Car( model, year, miles ) {
 
  this.model = model;
  this.year = year;
  this.miles = miles;
 
}
 
 
// Note here that we are using Object.prototype.newMethod rather than
// Object.prototype so as to avoid redefining the prototype object
Car.prototype.toString = function () {
  return this.model + " has done " + this.miles + " miles";
};
 
// Usage:
 
var civic = new Car( "Honda Civic", 2009, 20000 );
var mondeo = new Car( "Ford Mondeo", 2010, 5000 );
 
console.log( civic.toString() );
console.log( mondeo.toString() );
```

Above, a single instance of toString() will now be shared between all of the Car objects.