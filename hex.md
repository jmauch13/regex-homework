# Title
Matching a Hex Value

## Introduction
Hexadecimal is a system that uses 16 symbols.  
The symbols are '0' to '9' which represents values 0-9 and 'a'-'f' to represent the values 10-15.
One way to use the hex system is color codes.  As a hexadecimal representation of a color in RGB format, 
the format defines a color by the amount of red, green and blue, using values ranging from 00 to ff, indicating the intensity of the color.  
Hex color values are either three or six digits long, not including the'#'.
Examples of HEX color codes are:
```#FFFFFF```is Black
```#800080```is Purple
```#C0C0C0```is Silver

## Summary
This tutorial will focus on a regular expression (regex) to match any hexadecimal code in a string of characters.
The regex we will be looking at is:
```/^#?([a-f0-9]{6}|[a-f0-9]{3})$/```

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors
Anchors in a regular expression appear at the beginning and the end of the expression.
The anchors for our hex expression are ```^``` at the beginning of the expression and ```$``` at the end of the expression.

### Quantifiers
Quantifiers are the parts of a regular expression that take a specific number of characters from a search pattern.
We have two quantifiers in our expression, ```{6}``` and ```{3}```.
From our expression, ```[a-f0-9]{6}``` tells the computer to find a string containing the letters a-f and/or numbers 0-9.
The quantifier ```{6}``` returns the first six characters that match the expression.
The second part of the expression, ```[a-f0-9]{3}``` tells the computer to search for and return three characters that match the expression.

### OR Operator
In the hex regex, the ```|``` is used.  This is the OR Operator which means the code can be one of two things.
It's telling the computer to search for a hex code that's either six ```{6}``` or three ```{3}``` numbers or letters.

### Character Classes
Character classes are components within the regular expression that tells the computer what to look for.
Character classes are confined within brackets in hex expressions.  
There are two character classes, ```[a-f0-9]``` and ```[a-f0-9]``` meaning the computer is restricted to only 
returning letters and numbers within these parameters.

### Grouping and Capturing
Grouping in hex expressions is the expression contained in parenthesis.  The grouping treats multiple characters as a single unit.
In a hex expression, the grouping holds the bracket expressions, ```([a-f0-9]{6}|[a-f0-9]{3})```.

### Bracket Expressions
Bracket expressions in our regex shows the beginning of a character class or quantifier statement.
For hex expressions it is defined by a parenthesis.

### Greedy and Lazy Match
A greedy match tries to match an element as many times as possible.  A lazy match tries to match an element as few times as possible.
In the hex expression, we have a ```?``` which is a lazy quantifier.

## Author
My name is Jennie Mauch.  I am currently a full-stack developer student learning JavaScript, SQL and MERN.
Please visit me at https://github.com/jmauch13 to see more of what I'm building.
