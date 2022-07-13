# Regex-Tutorial

Regex is short for regular expression, which is a sequence of characters defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input.

## Summary

Matching an Email -   
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

The Regex I am breaking down is an Email regular expression.

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
`/^`([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`$/`
The highlighted part are the the anchors. Anchors are use to check matching starting or ending symbol of an input string. There two type of anchor, caret`^`,  which checks matching first character of the input string, and dollar sign`$`, which checks matching last character of the input string.

### Quantifiers
/^([a-z0-9_\.-]`+`)@([\da-z\.-]`+`)\.([a-z\.]`{2,6}`)$/

Quantifier specify how many instance of character, group or character class must be present in the input for a match to be found. If the `*`, `+`, `?`, `{`, `}` characters are encoutered in regular expression pattern. The regex engine interprets them as quantifier. 

The `+` quantifier matches the preceding element one or more times. It is equivalent to `{1,}`.`+` is a greedy quantifier whose lazy equivalent is `+?`.
The `{n,m}` quantifier matches the preceding element exactly _n_ times, but no more than _m_ times, where _n_ and _m_ are integers. `{2,6}` is a greedy quantifier whose lazy equivalent is `{2,6}?`. 
`[a-z.]`, `{2,6}` means that 2 to 6 characters matching inside brackets are expected, and the numbers inside the curly braces specify lower and upper limit number of characters are expected.

In this expression, `[a-z0-9_\.-]+` and `[\da-z\.-]+` means any character matching the characters inside the bracket is expected to appear at least once.

### Greedy and Lazy Match
The two version of quantifier are greedy and non-greedy(lazy). A greedy quantifier tries to match an element as many times as possible, where lazy quantifier tries to match an element as few times as possible. Greedy quantifier can be turn into lazy quantifier by adding a `?`.

### OR Operator
The or operator with in a regular expression is define using `|` element. For example, `(b|cd)ef` is a string that contains either `bef` or `cedf`.

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
