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



