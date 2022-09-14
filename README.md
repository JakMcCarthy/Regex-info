# Regex Tutorial

Regex-Tutorial.md

A regular expression, abbreviated as regex, defines a search pattern for a character sequence such as matching an email, matching a URL, matching an HTML tag, etc. When they are used in search algorithms or in code can be used to validate code, find specific patterns of characters in a string. Regular expressions can also be used to find and replace a character or character sequence.

## Summary

I will be discussing
`/^\w+([\.-]?\w+)_@\w+([\.-]?\w+)_(\.\w{2,3})+$/`
which is a regular expression used to verify that an email address has been entered as requested and not any other string that doesn't belong there.
I will explain how the characters in each part of the regex are doing a specific action which when all put together will enable the regex to determine if a string that is entered is an email or just a piece of code that does not belong there.

## Table of Contents

-   [Anchors](#anchors)
-   [Quantifiers](#quantifiers)
-   [OR Operator](#or-operator)
-   [Character Classes](#character-classes)
-   [Flags](#flags)
-   [Grouping and Capturing](#grouping-and-capturing)
-   [Bracket Expressions](#bracket-expressions)
-   [Greedy and Lazy Match](#greedy-and-lazy-match)
-   [Boundaries](#boundaries)
-   [Back-references](#back-references)
-   [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

In the above summary, the regex is used for matching an email. The anchors are the ^ at the begining and the $ at the end. This means the entire input string not just part of it will match the regex.

### Quantifiers

Qualifiers determine how many times specific characters/character groups should be shown for a match to take place.
That will specify the match has been made.

`\w+` matches 1 or more word characters (a-z, A-Z, 0-9 and underscore)

source: https://www.codeguage.com/courses/regexp/quantifiers

### OR Operator

The above regex used to make email matches does not contain and OR operator. A regex OR operator is | and it's used make matches on the left or the right of the operator.

### Character Classes

The \d character classes matches a single digit, the /w a word, and /s space character. They are refered to as shorthand character classes.

`\w+([.-]?\w+)*` is used to match the username in the email, before the @ sign, beginning with at least one character (a-z, A-Z, 0-9 and underscore), followed by more word characters or . or -

### Flags

This email matching example does not contain any flags.

A flag is written with a single lowercase alphabet character. There are a total of six flags in javaScript each with it's own purpose.

source: https://www.codeguage.com/courses/regexp/flags

### Grouping and Capturing

A way to treat multiple characters as one unit is by using grouping and capturing. This is done by using parentheses.
These are the groups in the email matching regex above:
`([\.-]?\w+) ([\.-]?\w+) (\.\w{2,3})`

### Bracket Expressions

Bracket expressions are used to match any character by entering the character/characters inside square brackets. Here is and example from the above email matching regex.

`[\.-]`

For more examples ee table at:
https://www.ibm.com/docs/it/netcoolomnibus/7.4?topic=library-bracket-expressions

### Greedy and Lazy Match

The terms greedy match and lazy match refer to the following:
Greedy match - the regular expresssion will match as many occurences of as it can of a certain pattern.
Lazy match - the regular expression makes the fewest possible matches of an occurance.


### Boundaries

In a string, boundaries are the postitions, like walls, between characters.
Word boundary - `/b`- where the word (any sequence ofthe `/w`char class) begins or ends.

There are none in the email matching regex above.

### Back-references

Back referencing in regex identifies groups that have matched previously and looks for the exact match again. Looking for repeated words in text is an example of back referencing where a pattern can be used that pinpoints a single word.

None in this email matching example.

### Look-ahead and Look-behind

Look ahead and look behind are used when looking to match something based on the content before or after. This is commonly called a look around.

## Author

Created By Jackson McCarthy, UCONN Coding Bootcamp.

https://github.com/JakMcCarthy/Regex-info

## Study Group

Susan, Jackson, Chris P., Sarah, Ricky, Aaron