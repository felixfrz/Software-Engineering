# The String Data Type
 
This article is about one of JavaScript's primitive data types, String. Strings are what we'll use to represent textual data. This means that strings are useful in representing things like messages, names, poems, and so on. A string is a sequence of characters.

## When you finish this article, you should be able to:

* Write strings using correct syntax
* Use `.length` to obtain a count of the number of characters that comprise a string
* Index a string to refer to a single character
* Concatenate strings together
* Writing a valid string

Strings are always wrapped by a pair of single quotation marks `(')` or by a pair of double quotation marks `(")`. Between the enclosing quotation marks, we can put any characters! Here are a six examples of strings:

```
"potato";
"London";
"felixfrz@gmtsoftware.tech";
"Follow the yellow brick road, please!";
"365 days a year";
"";
```

Above, notice that we are free to mix in any characters into a string. This includes spaces, numerics, punctuation, and other symbols. The sixth string above is the empty string; it contains zero characters!

You are probably wondering why we are allowed to use either single or double quotes when denoting a string - why is this useful? Maybe we want a string that contains quotation marks:

```
// valid strings
'Shakespeare wrote, "To be or not to be"';
"That's a great string";
```

```
//invalid string
'That's a bad string'
```
If we want to use a single quote as a character of a string, we simply need to enclose the string in double quotes, and vice versa.

## Calculating length
Since a single string can contain any number of characters, we may find it useful to count the number of characters in a string using `.length`:
```javascript
console.log("ramen".length); // => 5
console.log("go home!".length); // => 8
console.log("".length); // => 0
```
## Indexing a string
Strings consist of multiple characters. These characters are numbered by **indices** starting at `0`. So in the string `'software'`, `'s'` is at index `0`, `'o'` is at index `1`, `'f'` is at index `2`, `'t'` is at index `3`, and so on. We can look at particular characters of a string by using `[]` and specifying an index:
```javascript
console.log("software"[0]); // => 's'
console.log("software"[1]); // => 'o'
console.log("software"[2]); // => 'f'
console.log("software"[3]); // => 't'
console.log("software"[10]); // => undefined
console.log("software"[-3]); // => undefined
```
In general, when we index a string using the expression `string[i]`, we get back the **single character** at position `i`. Looking at the last two examples above, if we use an invalid index with a string, the value returned is `undefined`. This makes sense because there is no character at the given position! It's also worth mentioning that an index should always be a number.

## The classic "off by one" error
Bear in mind that indices begin at 0 and not 1! Forgetting this nuance can lead to incorrect code for both new and experienced programmers alike. Let's hone in on an important distinction: the index of the last character of a string is always one less than it's length.

```javascript
console.log("cat".length); // => 3
console.log("cat"[3]); // => undefined
console.log("cat"[2]); // => 't'
```
In other words, although the `length` of `'cat'` is 3, the index of the last character (`'t'`) is 2.

## Using indexOf
We can also calculate the index of a given character within a string by using `indexOf`:

```javascript
console.log("bagel".indexOf("b")); // => 0
console.log("bagel".indexOf("a")); // => 1
console.log("bagel".indexOf("l")); // => 4
console.log("bagel".indexOf("z")); // => -1
```
If we attempt to search for a character that is not present in a string, `indexOf` will return -1. This makes sense because we know that -1 is not a valid string index. The smallest index possible is 0!

If we search for a character that appears more than once in a string, `indexOf` will return the index of the first occurance of that character.

We can also use `indexOf` to search for a substring of characters. Under this circumstance, `indexOf` will return the index where the substring begins in the main string:

```javascript
console.log("door hinge".indexOf("oor")); // => 1
console.log("door hinge".indexOf("hi")); // => 5
console.log("door hinge".indexOf("hint")); // => -1
```
## Concatenation
Concatenation is just a fancy word for joining strings together into a single string. To concatenate strings, we use the `+` operator:

```javascript
console.log("hello" + "world"); // => 'helloworld'
console.log("goodbye" + " " + "moon"); // => 'goodbye moon'
```
## What you've learned
* a `String` is a data type that contains multiple characters enclosed in quotation marks
* `string.length` returns the number of characters in the `string`
* each character of a string is associated with a number index; the first character of a string is at index 0
* we can use `string.indexOf(char)` to obtain the index of `char` within `string`; if `char` is not found, then -1 is returned
* we can use `+` to concatenate multiple strings, combining them into a single string