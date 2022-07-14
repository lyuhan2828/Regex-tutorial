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
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)


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
Character class are also called character set. To tell regex engine to match out several characters, you can place characters you want to match between sqaure brackets. 
In most regex, the only special characters or metacharacters inside a character class are the closing bracket `]`, blackslash `\`, caret `^`, and hyphen `-`. 
In this expression `\d`, it matches any digits equivalent to `[0-9]`.

### Grouping and Capturing
Capturing groups are a way to treate multiple characters as a single unit. They created by placing the characters to be grouped inside a set of parentheses. For example the regular expression (dog) creates a single group containing the letters "d" "o" "g". The portion of the input string that matches the capturing group will be saved in memory for later recall (backreferences).

### Bracket Expressions
A bracket expression is a list of characters enclosed by `[` and `]`, It matches any single character in that list. If the first character of the list is the caret `^`, then it matches any character not in the list and it is unspecified whether it matches an encoding error.

For example `[a-z0-9_\.-]`, matches any single character that is not an opeing or closing parenthesis, and might or might not match an encoding error.

Punctuation characters; in the ‘C’ locale and ASCII character encoding, this is ! " # $ % & ' ( ) * + , - . / : ; < = > ? @ [ \ ] ^ _ ` { | } ~.
Hexadecimal digits: 0 1 2 3 4 5 6 7 8 9 A B C D E F a b c d e f.

## Author

Anna Liang is taking full-stack development course to do a career change.
Github: <a href="https://github.com/lyuhan2828/Regex-tutorial/blob/main/gist-template.md" target="_blank">Anna Liang</a>
