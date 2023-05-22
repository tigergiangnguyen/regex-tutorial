# 17 Computer Science for JavaScript: Regex Tutorial

Regular expressions (regex) are powerful tools for pattern matching and manipulating text. They are used in many programming languages to search, validate, and manipulate strings. Regular expressions are a sequence of character that creates a search pattern. They can be include literal and meta characters that servers a different purpose. Here is where I will be diving into regex and explain how they are use and the benefits.

## Summary

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Above is a regular expression provided. It is a pattern for validating an email addresses. This expression checks to see if a string fulfills the requirements for a basic email. In the sections below, I will be debugging this specific regex function and go over each special characters purpose.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

## Regex Components

Various components allows for pattern matching and manipulation of text that meets the regular expression. The components is what makes up for the regex function and is created in two ways. The one of the summary I will be explaining uses literal notation that wrapped in slash characters (`/`), another way to create a regex object is to a RegExp constructor. The constuctor function's parameters are not enclosed within slashes; instead, they use quotation marks.

### Anchors

Anchors define the position of a match within the text. They do not match any actual characters, but rather specific locations or boundaries. The caret anchor (`^`) matches that start of a line or string. The dollar sign anchor (`$`) matches the end of a line or string. It asserts that the preceding pattern is found at the line of the line or string. Anchors enforces the start and end of patterns of lines or strings.

### Quantifiers

Quantifiers are use to count the number of occurrences of next element or a pattern. It allows you to have the desired length of how many times it currents in a pattern. In the summary regex, `{2, 6}` is saying that the expression must have bewteen 2 and 6 characters, after `.` has a "org" or "com" is validate because it has more than 2 and no more than 6.
The `+` quantifier ensures that there is at least one character in the username.

### Grouping Constructs

A Group Constructs are a pattern paired in parentheses `()` and uses all components to the group as a whole. The email expression has three groups surrounded by parentheses and can be references like `\1`, `\2`, etc. The first grouping `([a-z0-9_\.-]+)` captures the username part of the email, the second grouping `([\da-z\.-]+)` captures the domain name, and last grouping `([a-z\.]{2,6})` captures the top-level domain such as ".org" or ".com".

### Bracket Expressions

Bracket expressions `[]` allows you to have a set of characters that can match the position in the text. It can be define in mutiple ways, the email expression has character ranges. For example `[a-z]`, is matching any lowercase letter from "a" to "z" and `[0-9]` is matching any digit from 0 to 9. The hyphen `[-]` used between alphanumeric characters to represent a range of those possible characters. The string `[_-]` can contain an underscore or hyphen which as called special characters.

### Character Classes

Character classes touches the same basic of bracket expression but including positive and negative character groups known. In the email expression, `.` matches any character expect the newline character `\n`. `\d` matches any arabic numeral digit and also can be changed to perform an inverse match by capitalizing the letter character.

### Character Escapes

Character escapes allows you to match specific characters that have special meanings. Using escapes can treat these characters as literal characters rather than disturbing the special meanings. In the email expression, Matching a literal dot character `\.` can match any characyer expect newline characters.

## Author

Contact and connect with me at my [Github](https://github.com/tigergiangnguyen)