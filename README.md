#### JavaScript Display Possibilities

|Display | Possibilities |
|----|----|
|innerHTML|Writing into an HTML element|
|document.write()|Writing into the HTML output |
|window.alert()|Writing into an alert box|
|console.log()|Writing into the browser console|

#### innerHTML

```bash
  document.getElementById("demo").innerHTML = 5 + 6;
  document.getElementById("demo").innerHTML = "Hello JavaScript"; 
```
#### document.write()

```bash
  document.write(5 + 6);
```

#### window.alert()

```bash
  window.alert(5 + 6);
  alert(5 + 6);
```

#### console.log()

```bash
 console.log(5 + 6);
```

## Data Types

Javascript is a dynamically typed language and hence though there are data types, variables are not bound to them.

|Data Type | Description |
|----|----|
|number| Represents numbers like integers, floating-values etc|
|string| Represents one or more characters|
|bigint| Represents integers of arbitrary length|
|boolean| Represents either true or false|
|Arrays| arrays are written with square brackets|
|object| objects are written with curly braces {}|
|undefined| a variable without a value, has the value undefined
|null| Represents unknown values|


## JavaScript Identifiers / Names

- A letter (A-Z or a-z)
- A dollar sign ($)
- Or an underscore (_)
- ``Numbers are not allowed as the first character in names``
- ``Hyphens are not allowed in JavaScript. They are reserved for subtractions.``
- ``JavaScript is Case Sensitive``
- ``JavaScript does not interpret LET or Let as the keyword let.``
```
let $ = "Hello World";
let $$$ = 2;
let $myMoney = 5;

let _lastName = "Johnson";
let _x = 2;
let _100 = 5;


```
- ``If you put a number in quotes, the rest of the numbers will be treated as strings, and concatenated.``
```
let x = 2 + 3 + "5"; // output 55
```
## JavaScript Character Set
- JavaScript uses the Unicode character set.

## 4 Ways to Declare a JavaScript Variable:
- var
- let
- const
- nothing
- ``The var keyword is used in all JavaScript code from 1995 to 2015.``
- ``The let and const keywords were added to JavaScript in 2015.``


## Let
- ``Variables defined with let cannot be Redeclared.``
- ``Variables defined with let must be Declared before use.``
- ``Variables defined with let have Block Scope.``
- ``Redeclaring a variable in the same block is NOT allowed``
- ``Variables declared inside a { } block cannot be accessed from outside the block:``

```
let x = "John Doe";
let x = 0; // SyntaxError: 'x' has already been declared 
// we cannot Redeclared let variable
```

#### Var Hoisting
* Variables defined with var are hoisted to the top and can be initialized at any time. 
* Meaning: You can use the variable before it is declared:

```
carName = "Volvo";
var carName;  // means before decalring variable we can use 

```

#### let Hoisting
*  Variables defined with let are also hoisted to the top of the block, but not initialized
* Using a let variable before it is declared will result in a ReferenceError

```
carName = "Saab";
let carName = "Volvo"; 
// ReferenceError: can't access lexical declaration 'carName' before initialization
```


## CONST
- ``Variables defined with const cannot be Redeclared.``
- ``Variables defined with const cannot be Reassigned.``
- ``Variables defined with const have Block Scope.``
- ``const variables must be assigned a value when they are declared:``

```
 const PI = 3.141592653589793; // Correct
PI = 3.14;      // This will give an error
PI = PI + 10;   // This will also give an error 
```

Incorrect

``` 
const PI;
PI = 3.14159265359;
```

### When to use JavaScript const?
* A new Array
* A new Object
* A new Function
* A new RegExp

#### Constant Objects and Arrays
``It does not define a constant value. It defines a constant reference to a value. ``

 ### Because of this you can NOT:
 - Reassign a constant value
 - Reassign a constant array
 - Reassign a constant object

 ### Because of this you can NOT:
 - Change the elements of constant array
 - Change the properties of constant object

 ```
 // You can create a constant array:
const cars = ["Saab", "Volvo", "BMW"];

// You can change an element:
cars[0] = "Toyota";

// You can add an element:
cars.push("Audi");
 ```
### But you can NOT reassign the array:

```
const cars = ["Saab", "Volvo", "BMW"];
cars = ["Toyota", "Volvo", "Audi"]; 

```

#### const Hoisting
*  Variables defined with const are also hoisted to the top of the block, but not initialized
* Using a const variable before it is declared will result in a ReferenceError

```
carName = "Saab";
const carName = "Volvo"; 
// ReferenceError: can't access lexical declaration 'carName' before initialization
```

#### JavaScript Comparison Operators

| Operator | Description |
|----|----|
|==|equal to|
|===| equal value and equal type |
|!=|not equal|
|!==|not equal value or not equal type|
|>|greater than|
|<|less than|
|>= |greater than or equal to|
|<=|?|

#### JavaScript Type Operators


| Operator | Description |
|----|----|
|typeof|Returns the type of a variable|
|instanceof |Returns true if an object is an instance of an object type|

### Extracting String Parts

- ``JavaScript counts positions from zero. ``
- ``First position is 0. && Second position is 1. ``

* slice(start, end)
* substring(start, end)
* substr(start, length)

## slice()
* slice() extracts a part of a string and returns the extracted part in a new string.
* The method takes 2 parameters: the start position, and the end position (end not included).

```
let str = "Apple, Banana, Kiwi";
str.slice(7,13); // Banana
```
If a parameter is negative, the position is counted from the end of the string.

This example slices out a portion of a string from position -12 to position -6: 

```
let str = "Apple, Banana, Kiwi";
let part = str.slice(-12, -6); // Banana

```
If you omit the second parameter, the method will slice out the rest of the string

```
let part = str.slice(7);
str.slice(7); // Banana, Kiwi
```
or, counting from the end:

```
let part = str.slice(-12); // Banana, Kiwi
```

## substring()
* substring() is similar to slice().
* The difference is that substring() cannot accept negative indexes.

```
let str = "Apple, Banana, Kiwi";
let part = str.substring(7, 13);
```
If you omit the second parameter, the substring will slice out the rest of the str

```
let part = str.slice(7);
str.slice(7); // Banana, Kiwi

```

## substr()
* substr() is similar to slice().
* The difference is that the second parameter specifies the length of the extracted part.

```
let str = "Apple, Banana, Kiwi";
let part = str.substr(7, 6); // Banana, Kiwi
```
If you omit the second parameter, the substr will slice out the rest of the str

```
let part = str.slice(7);
str.substr(7); // Banana, Kiwi

```
If the first parameter is negative, the position counts from the end of the string.

```
str.substr(7); // kiwi
```

## Replacing String Content
- `` The replace() method does not change the string it is called on.``
- ``The replace() method returns a new string ``

The replace() method returns a new strin ``
* The replace() method replaces a specified value with another value in a string:

```
let text = "Please visit Microsoft!";
let newText = text.replace("Microsoft", "W3Schools");
// Please visit W3Schools!
```

## Regular expression

`` Regular expressions are written without quotes. ``

To replace all matches, use a regular expression with a /g flag (global match):

```
let text = "Please visit Microsoft and Microsoft!";
let newText = text.replace(/Microsoft/g, "W3Schools");
```





