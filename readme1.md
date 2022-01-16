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
let text1 = "Hello World!";
let text2 = text1.toUpperCase(); // HELLO WORLD!
```
JavaScript String toLowerCase()

```
let text1 = "Hello World!";       // String
let text2 = text1.toLowerCase();  // text2 is text1 converted to lower 

```
## Converting to Upper and Lower Case

concat() joins two or more strings:

```
let text1 = "Hello";
let text2 = "World";
let text3 = text1.concat(" ", text2); // Hello World!
```
## JavaScript String trim()
 *The trim() method removes whitespace from both sides of a string:
```
