# My Regex Tutorial

What is Regex - you ask? Regex is short for regular expressions. What is it used for - you ask? Regex, or regular expression is a means to search through text. You can find certain text, characters and replace them, validate your text, such as email or URL validation. You can even group find and replace from your text.

## Summary

This regex, or regular expression is for validating and matching a URL `^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$`


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
*   The `^` of an expression matches at the start of the string and the `$` matches at the end of the string

[https://www.google.com/photos]

The use of the first component `^(https?:\/\/)` matches with the `https://` or `http://` since the question mark `?` precedes the `s`, leaving this character as optional in the search.

The use of the second component ` ([\/\w \.-]*)*\/?$` matches with `//www.google.com/photos` The question mark `?` right before the dollar sign `$` allows for the match of `photos` in the URL as that allows for optional search patterns after the slash `/` no match is found if the question mark `?` is removed from the expression component or until `photo` in the URL is removed from the string.

### Quantifiers

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
