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

## Regex Components

### Anchors
*   The `^` of an expression matches at the start of the string and the `$` matches for the end of the URL string

[https://www.google.com/photos]

The use of the first component `^(https?:\/\/)` matches with the `https://` or `http://` since the question mark `?` precedes the `s`, leaving this character as optional in the search.

The use of the second component ` ([\/\w \.-]*)*\/?$` matches with `//www.google.com/photos` The question mark `?` right before the dollar sign `$` allows for the match of `photos` in the URL as that allows for optional search patterns after the slash `/` no match is found if the question mark `?` is removed from the expression component or until `photo` in the URL is removed from the string.

### Quantifiers

* Quantifiers are symbolized by these characters `*`, `+`, `?` and `{}`

- The asterisk `*` will match a string in a simplest example `abc*`, will match `ab` and `c`, in case of `ab`, `abc` or even `abcc` but not the `b` in ‘b`abc`’

- The plus `+` will match a string in a simplest example `abc+`, will match the exact string `abc` or `abccc` but not the ‘b in `abc`’

- The question mark `?` will match a string in a simplest example `abc?`, will match the exact string `ab plus c` but only 1 `c`, for example or ‘`abc`cc’

- The curly braces `{ }` will match a string in a simplest example `abc{2}`, will match the exact string `abcc` but not a 3rd  or more `c` or a single c in case of `abc` or `abcccc`, these two will not match as conditioned by the number `2` in the curly braces `{2}`. You can set a range for this match `{2,5}` wherein you can match `abcc` or `abccccc` as long as your `c` range is within `2 to `5` characters long.


For the asterisk `*` quantifier, the URL http://www.google.com/-photos/dogs followed by the regex component expression `([\/\w \.-]*)*`. This component expression uses a combination of parts `/` matches in the slashes in a URL,  `\w`, matches with alpha numeric characters in case of URL string `www1` as well as `\.- `in case of string URL with `.com/dog-photos`. The inclusion of `.` and `-` allows for matches before those characters instead of only after those characters in the URL string. The exclusion of the asterisk `*`s would prevent any match to the URL to be found or the exclusion of the conditions in the `[]` would also prevention any matches from being found in the URL string.

### OR Operator

* the `|` or `[ ]` brackets

- An example of the `|` used for `a(b|c)` will match with `ab` or `ac` but not `aa`, `bb`, `cc`, `ba` or `ca`

- An example of the `[ ] ` used for `a[bc]` will match with `ab` or `ac` but not `aa`, `bb`, `cc`, `ba` or `ca`. 

- the brackets `[ ] ` seem to do the same thing as the `|` but there’s something about the way it groups these matches, I’m not sure. https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285 says “but not capturing `b` or `c`

### Character Classes

* Character classes `\d`, `\w`, and `\s`

- `\d` matches a number in any string, for example ab`2`c, `2` is found or de`56`fghi, `5` and `6` are  are found in this string.

- `\w` finds any letter, number and underscore, for example `2bc3_a`, or `a` `1` `_` by themselves is found.

- `\.` matches any type of character, event special characters like `&`, `$`, `*`, `>`, `/` and `.`

### Flags

* Flags are identified by slashes `/` which are used to set the boundaries of the regular expressions, regular expression can also be combined using the slashes.

### Grouping and Capturing

- Grouping and capturing is done with parathesis `( )` to create a capture group, for example a(bc) would only match with the with `abc`, not `a` or `bc`

- Grouping and capturing is done with parathesis `( )` to create a capture group, for example a(bc) would only match with the with `abc`, not `a` or `bc`.

- Using `a(?:bc)*` disables the capturing group, though the `abc` is still a match, `a` by itself or ‘`a`cf’ is still a match but only if the expression contains the asterisk `*`. Without the asterisk `*` only `abc` will be matched.

### Bracket Expressions

* Bracket expressions can be as the following `[abc]`, which will match with the string containing either `a,b or c` singularly like `a`, `b`, or `c`, but also `ab`, `bc` or `ac` for example. You can also use [a-c] which is the same as `[abc]`,Bracket expressions can be as the following `[abc]`, which will match with the string containing either `a,b or c` singularly like `a`, `b`, or `c`, but also `ab`, `bc` or `ac` for example. 

* You can also use [a-c] which is the same as `[abc]`, meaning, it will find a match `a` through `c`. Think of brackets as a search through a range or spectrum, `[a-zA-Z0-9]` this will find any characters, from lower case `a` to lowercase `z` as well as their uppercase characters, while also finding the numbers `0` through `9`.

### Greedy and Lazy Match

-	These are symbolized by `*`, `+` and `{ }`. These are greedy operators. For example, this expression `<.+>` will match with `<div> any text between </div>`, whereas the question mark `?` added to the expression will turn into a lazy one, `<.+?>`, making this only able to match, just the 2 `<div>` and `</div>` but none of the text in-between. 

## Author

I’m a student learning to code for full stack web development with 6 weeks left in the program. It’s been tough, and it’s been fun with moments of brilliance and getting thigs to work.

<br>

* David Crockett / <a href="https://github.com/CastroOlympias">CastroOlympias @ GitHub</a>

## Thoughts

I wanted to be thorough, but not over do it since I can easily over think things. I can get very detailed about any subject, even in the case of Regex, and don’t want to get lost in the weeds of trial and error. I hope this much is at least adequate to get the ball rolling, but either way. You have to put it into practice, so I do recommend some of these sources, to try it out. 
<br>
<br>
https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285 and https://regex101.com/. Here are some additional sample expressions to try out
<br>
<br>
•	Matching a Hex Value -- `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
<br>
•	Matching an Email -- `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
<br>
•	Matching a URL -- `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`
<br>
•	Matching an HTML Tag -- `/^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/`
