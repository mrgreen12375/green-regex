# Regex Tutorial

Welcome to this tutorial on Regular Expressions. In this tutorial I will break down a Regex to give  more understanding on how Regex works. I will use a specific Regex and show each part of the expression. 

## Summary

The Regex below is an expression to check for valid URL

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Break Down](#break-down)

## Regex Components

### Anchors

Anchors are shown as `^` and `$`. The caret anchor `^` refers to the beginning of the string and the dollar anchor `$` refers to the end of the string. In-between these anchors we'll be looking for a series of characters to match the position before or after characters.

### Quantifiers

Quantifiers match a number of instances of a character, group, or character class in a string.

* `?` - Shows the character or patten is expected zero or one time
* `*` - Shows the character or pattern is expected zero or more itmes
* `+` - Shows the character or pattern is expected one or more times
* `{}` - Allows for selection of range.

### Character Classes

A character class is a set of characters inside square brackets. It specifies that the characters that will successfully match a single character from a given string.

Some examples in for this tutoral:

* `\d` - matches any digit
* `\w` - Matches any alphanumeric character

`[\da-z\.-]` `[a-z\.]` `[\/\w \.-]`

### Character Escapes

`\` is an escape code that with give a character it original meaning. 

For example if you want a period `.` to just be a period you would use the backslash. 

### Grouping and Capturing

Grouping constructs specify the subexpressions of a Regex and capture the substrings of a string. You can use grouping constructs to match a subexpression that is repeated in the string. You can use `()` to make the groupings. The example in this tutorial has 4 groupings. 

`(https?:\/\/)` `([\da-z\.-]+)` `([a-z\.]{2,6})` `([\/\w \.-]*)` 

### Bracket Expressions

Bracket expressions `[]` enclose characters to specify a match or a range of matches. Such as the aphabet `[a-z]`. `[a-z]` would match any lowercase character from a-z. 

`[\da-z\.-]` `[a-z\.]` `[\/\w \.-]`

### Break Down

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

* `^` - Match at the start of the string.

* `(https?:\/\/)?` - Expecting zero or one time, http s that may be there once or not at all, 2 forward slashes with the escape `\`. Looking for http:// OR https://.

* `([\da-z\.-]+)\.` - Bracket enclosing a range of matches. `\d` meaning any digit and `a-z`.

* `([a-z\.]{2,6})` - Bracket enclosing a range of matches. Letters `a-z` and 2 to 6 characters are expected. Looking for `com` for example. 

* `([\/\w \.-]*)*\/?` - Bracket enclosing a range of matches. `/` Matches any alphanumeric character including underscore `\w`, a period or a dash and a `/` which may occur one or more times as shown by the `?`.

* `$` Match at the end of the string.

## Author

Steven Green [Github](https://github.com/mrgreen12375)
