# "Matching an Emal" Regex Tutorial

In this tutorial, you'll learn about the use of regex match emails with this expression: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. You can find this useful when you are trying to validate emails using applications like Inquirer.

## Summary

We'll start by understanding what a regular expression is. A regular expression is a sequence of symbols and characters that translate to a particular search pattern, especially within a string. In this case, we will be using regex and how we can use it to matching an email.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors
I'll be breaking down these symbols/characters and its uses here.

`^` indicates the start of a string.
`$` indicates the end of a string.

There may be instances where you see `(m)` for a multine string, but that won't be enabled all the time. With that being said, the regex will end at `$`.
### Quantifiers
`+` serve the purpose of connecting the email name + the email service + `.com`.

`{2,6}` in this case, will enable a match range of 2 to 6 characters from a to z which is expressed as `[a-z\.]`. Before you scroll on, I'll explain what it means to have a match range. With regex, you have a few options to match a digit. You can match a number from 0 to 9 to another single choice. With a match range, you can match a range of digits with a character group. Keep this in mind for the character classes section below.

### Character Classes
`\d` matches a single character or symbol that is a digit between 0 and 9. If the character group allows any digit between said numbers, it will be replaced with a shorthand `\d`. For more clarification, a `\d` will replace a single digit like "5", but not "55".

### Grouping and Capturing
`([a-z0-9_\.]+)`

### Bracket Expressions
`[a-z0-9_\.-]`
`[\da-z\.-]`
`[a-z\.]`

### Greedy and Lazy Match
`+`
`{}`

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
