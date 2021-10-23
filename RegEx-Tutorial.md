# Title (replace with your title)

RegEx is known as "regular expression" which is a pattern to validate strings of character combinatinations. We will break it down how it works in your code. 

## Summary

This file will cover the components of RegEx expressions and how they are helpful to define patterns to match strings. 

ex: let string = 'Alexis';
console.log(/^A/.test(string));

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

Anchors help match a position of a character before or after the text. 

in the case of 

let string = 'Alexis';
console.log(/^A/.test(string));

the ^ Anchor is matching to the string 'Alexis' and the output is true

the $ Anchor searches for the end of the text

let string = 'Alexis;
console.log(/s$/test(string));

the dollar anchor is matching the last letter S to the consolelog 

### Quantifiers

Quantifiers match instances within a group, character or string class. 

When you use curly braces on a number it will look for the digit amount within the string and output it.

let string ='Its the year 2021'
let regexp = /\d{4}/; 

we are looking for 4 digits here 

console.log(result);

only 2021 (4 digits) will be the output

### Grouping Constructs

You can group expressions by using round brackets and parentheses, you can then apply a quanitifier to the whole set group within the regex function

Square brackets define character class

### Bracket Expressions

Brackets help match characters within the string. You can use hyphens to do more than a individual character.

'Alexis'.match(/[abcd]/) // -> matches 'a'

they will be case sensitive unless you use the i flag

'Alexis'.match(/[A-D]/i) // -> matches 'A'

### Character Classes

Allows you to match any symbol to a certain character within the set. 

\d to match a digit or character from 0-9
\s to match to a symbol within the string
\w to match to a word in alphabet 

let string = 'Alexis is 24';
let regexp = /\w\d/g

console.log(str.match(regexp));

Here there would be output 

### The OR Operator

This is a "OR" expression with the deonation of the verticle line "|" 

if we are trying to find a group in a string we do it like this. 

let regexp = /apple/banana/carrot/celery(script)?/gi;

let string = "First I ate an Apple then a Bananan then some Celery and Carrots";

alert(string.match(regexp));

the output will then be: apple,banana,carrot,celery

### Flags

Flags are parameters that help us search within a simple expression they are denoted by single characters.

i = ignores case sensitivity 
g = global search for all 
s = makes a wild character 
m = makes boundary of characters ^ and $ match every  line instead of the whole string
y = makes expression search from a index
u = makes expression see characters as code points up to 32 bit characters. 

### Character Escapes

backslash is used to escape the next character this allows us to reserve characters to match other ones. 

{} [] / \ + * . $ ^ | ? 

example: "(a|o|p)at\.?" => alexis owns a cool pc. 

alexis, owns, pc will be pulled. 

## Author

I'm a full stack engineer. 

https://github.com/alexisvfilmstuff