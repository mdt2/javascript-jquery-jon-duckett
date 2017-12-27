# Highlights

### 1: The ABC of Programming:

**A: What is a script and how do I create one?**
+ Start with the big picture by
  1. Define the goal
  2. Design the script
  3. Code each step
+ Use a flowchart

**B: How do computers fit in with the world around them?**
+ Objects are things
  + They have their own properties, events, methods
+ Properties are characteristics that have a name and value
  + Ex: "hotel": "Hilton"
+ Events trigger a section of code
+ Methods are the things people need to do with objects
  + Ex: change the value (method) of the property name "rooms" when someone books (event) a room

**C: How do I write a script for a webpage?**
+ The location of <script> in the HTML affects where the JS is written into the page
  + Can affect loading time of pages
  + Better place to put <script> would be right before the closing body tag
+ Member operator is the dot between an object and a method.
  
### 2: Basic JavaScript Instructions

**Statements**
+ End with a semi-colon
  + Variables, calling a functions
  
**Shorthands for variables**
+ Examples:
  + `var price = 4;
  var quantity = 14;`
  
  + `var price, quantity;
  price = 4;
  quantity = 14;`
  
  + `var price = 4, quantity = 14`
+ Variables should be named with camelCase (or, less common, underscores)

**Creating arrays**
+ Use array literals instead of constructor arrays
  + `colors = ['black', 'white'];` not `colors = new Array('white','black);`

### 3: Functions, Methods, and Objects

**Functions**
+ *Parameters* act like variable names inside a function, they are part of the function declaration
  + Used to provide a function with specific info it needs to perform the task
+ *Arguments* are like parameters, but they're the information you pass to the function upon calling it
  + Example:
  `function getArea(width, height)` width, height are parameters
  `getArea(3, 5)` 3, 5 are the arguments that are the width, height
  + Can also specify arguments through variable names
+ Functions can return 2+ values using arrays (ex p. 95)

+ Named vs. Anonymous functions
  + Function declarations are named functions
    + Can be called before the function is declared in the script
  + Function expressions are anonymous functions
    + Where you expect to see an expression, but there's a function
    + Ex: `var area = function(width, height) {};`
    + Anon functions are not processed until the interpreter goes through that statement
    + They can be altered based on code that runs before it

+ Immediately invoked function expressions (IIFE, pronounced iffy)
  + Called once
  `var area = ( function() {
    ...
  }());`
  + The *final parantheses* after the curly brace tell the interpreter: call this function immediately
  + The *grouping operators* before and after the function ensure the interpreter treats it as an expression
  + Use when the function code only needs to run once. Examples:
    + As an argument when a function is called
    + Assign value of property to object
    + Prevent conflicts between scripts that use same variable names
  + Variables declared in IIFE's are protected from other variables that have the same name (because of scope)

**Scope**
+ Local vs global variables
  + Local are created when the function runs, removed when function finishes task
    + Function runs twice? Variable can have different value each time
    + *Use whenever possible*
  + Global are stored in memory for as long as the web page is loaded
    + Can make script run slower

**Objects**
+ Variables are called properties
+ Functions are called methods
+ The name of the properties and methods is a *key* that corresponds to it's *value*

+ Creating objects
  + Object literal is easiest, most common
  `var hotel = {
    name: 'Hilton',
    rooms: 40
  };`
  + Constructor notation, create a new object and use dot notation to add properties/methods
  `var hotel = new Object();
  hotel.name = 'Quay';`
    + Create lots of objects: Can use a function as a template for creating objects
    `//The name of a constructor function starts with a capital letter
    function Hotel(name, rooms) {
      this.name = name;
      this.rooms - rooms;
      //"this" keyword is a reference to the object that the function is created inside
    }`

+ Dot notation to access properties or methods of objects
  `var hotelName = object.property/method name;`
  `var hotelName = hotel.name;`
  + Updating property values
  `hotel.name = 'Park';`
+ Square brackets
  ` var hotelName = hotel['name'];`
  + Used if property/method name uses special characters, name of property is a number, variable is used in place of property name
  + Update property of object
  `hotel['name'] = 'Park';`
  
**Numbers**
+ Integer: whole number
+ Real number: whole number, can contain fractional part
+ Floating point number: uses decimals to represent fractions
+ Scientific notation: really big or small numbers

+ Number object
  + toFixed() and toPrecision() return a string
  
**Date object**
+ Syntax/oder:
  Year: 4 digits
  Month: 0-11 (Jan is 0)
  Day: 1-31
  Hour: 0-23
  Mintes: 0-59
  Seconds: 0-59
  Milliseconds: 0-999
