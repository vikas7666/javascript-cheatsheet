## JavaScript String Search
* String indexOf()
* String lastIndexOf()
* String startsWith()
* String endsWith()

- ``Both indexOf(), and lastIndexOf() return -1 if the text is not found: ``

### indexOf() 
- `` The indexOf() method returns the index of (the position of) the first occurrence of a specified text in a string: ``

```
let str = "Please locate where 'locate' occurs!";
str.indexOf("locate"); // 7
```
### lastIndexOf() 
- `` The lastIndexOf() method returns the index of the last occurrence of a specified text in a string: ``
```
let str = "Please locate where 'locate' occurs!";
str.indexOf("locate"); // 21 
```
Both methods accept a second parameter as the starting position for the search:
```
let str = "Please locate where 'locate' occurs!";
str.indexOf("locate", 15);  // 21 bcz in starting position locate came in 7 after 7 position this will show 15
```

```
let str = "Please locate where 'locate' occurs!";
str.indexOf("locate", 7);  // locate 7 in come in 7 position that's why if we pass 8 then we show 15
```

### search()

 `` The search() method searches a string for a specified value and returns the position of the match:``

```
let str = "Please locate where 'locate' occurs!";
str.search("locate");  // 7
``` 
### Did You Notice? 
  The two methods, indexOf() and search(), are equal? 
- The two methods are NOT equal. These are the differences:
- ``The search() method cannot take a second start position argument. ``
- ``The indexOf() method cannot take powerful search values (regular expressions).``

### String match()

- The match() method searches a string for a match against a regular expression, and returns the matches, as an Array object.

- `` If a regular expression does not include the g modifier (to perform a global search), the match() method will return only the first match in the string. ``


```
let text = "The rain in SPAIN stays mainly in the plain";
text.match(/ain/g);
```
Perform a global, case-insensitive search for "ain":

```
let text = "The rain in SPAIN stays mainly in the plain";
text.match(/ain/gi);  // ain,AIN,ain,ain  // g means global
```
### String includes()

- The includes() method returns true if a string contains a specified value.
```
let text = "Hello world, welcome to the universe.";
text.includes("world");
```
Check if a string includes "world", starting the search at position 12:

```
let text = "Hello world, welcome to the universe.";
text.includes("world", 12);  false
```
### String startsWith()

- The startsWith() method returns true if a string begins with a specified value, otherwise false:
* The startsWith() method is case sensitive.
* startsWith() is not supported in Internet Explorer.

```
let text = "Hello world, welcome to the universe.";
text.startsWith("Hello");  // true
```
- Check if a string includes "world", starting the search at position 12:

```
let text = "Hello world, welcome to the universe.";
text.includes("world", 12); // false
```
- string.startsWith(searchvalue, start)
```
 let text = "Hello world, welcome to the universe.";

text.startsWith("world", 5)    // Returns false 
```

### String endsWith()

- The endsWith() method returns true if a string ends with a specified value, otherwise false:
* The endsWith() method is case sensitive.
```
var text = "John Doe";
text.endsWith("Doe"); // true
```
- string.endswith(searchvalue, length)

Check in the 11 first characters of a string ends with "world":
```
let text = "Hello world, welcome to the universe.";
text.endsWith("world", 11); // true
