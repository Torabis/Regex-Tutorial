# Regex Tutorial / Email Matching

Regular expressions (often referred to as regex) are sequences of characters that define search patterns. These expressions can be used to find certain patterns of characters within a string or to find/replace character(s) within a string. Validating inputs is also a use for regex. 

## Summary

This tutorial will examine the regex shown below to match an email address. 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

This tutorial will discuss and explain each component of this regex. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
Anchors allow a match to succeed or fail depending on the current position in the string.

`^` The match must start at the beginning of the string or line.

`$` The match must occur at the end of the string or before \n at the end of the line or string.

### Quantifiers
Quantifiers match a number of instances of a character, group, or character class in a string.

`{n}` When you append it to a character or character class, it specifies how many characters or character classes you want to match.

`+` Matches one or more occurrences of the one-character regular expression.

### Character Classes
A character class allows you to match any symbol from a certain character set. 

`/d` The digit character class is denoted matches any single digit

`.` Is a special character class that matches any character except a newline

### Grouping and Capturing
By placing part of a regular expression inside round brackets or parentheses, you can group that part of the regular expression together. This allows you to apply a quantifier to the entire group or to restrict alternation to part of the regex.

we have 3 capture groups which allows us to have separate string rules apply to each.  `([a-z0-9_\.-]+)` separated by special character `@` followed by the second capture group `([\da-z\.-]+)`, and the third capture group `([a-z\.]{2,6})`.


### Bracket Expressions
bracket expressions match one character out of a set of characters, just like regular character classes. They use the same syntax with square brackets. A hyphen creates a range, and a caret at the start negates the bracket expression.

The first, `[a-z0-9_\.-]`, means that all the characters between a through z will be matched, as well as numeric characters between 0-9.

The second, `[\da-z\.-]`, checks for characters a-z and also checks for `\d` which is matching for digital digit. 

The third, `[a-z\.]`, - means that any characters between a through z will be matched and in addition a dot will be matched.

### Greedy and Lazy Match
Greedy and lazy qualifiers allow you to find the "greedy" (longest) and "lazy" (shortest) match. Our example shows `+` as the greedy match since it ensures a search of as many matches as possible for decimal numbers, alphabateical characters, and hyphens. 

### Back-references
[Regular-Expression.info](https://www.regular-expressions.info)<br />
[javascripttutorial.net](https://www.javascripttutorial.net)<br />
[w3schools.com](https://www.w3schools.com)<br />


## Author

[GitHub Profile](https://github.com/Torabis)
