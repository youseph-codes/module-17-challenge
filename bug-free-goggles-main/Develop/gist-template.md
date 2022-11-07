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
`([a-z0-9_\.]+)` captures group one, which declares and matches with the user's email name.
`([\da-z\.-]+)` captures group two, which declares and matches with the email service.
`([a-z\.]{2,6})` captures group three, which matches with `.com`.

### Bracket Expressions
`[a-z0-9_\.-]` matches any alphabetic character from "a" to "z", any digit character from "0" to "9", and the use of an underscore, period, or a dash character ("-", "_", and "."). I'll also mention that the matches for alphabetical characters are case sensitive.
`[\da-z\.-]` does the job of matching a single digit from "0" to "9", any alphabetical and case sensitive character from "a" to "z", and the use of periods or dashes("." and "-").
`[a-z\.]` will match any alphabetical and case sensitive character from "a" to "z" as well as any use of the period character(".").

### Greedy and Lazy Match
`+`, as you remember from the quantifiers section above, is used in this instance of regex as what they call greedy matches. With the `+` quantifier, it's going to match as much as it could and returning what's needed.
`{}` is also used in this instance to match with `{2,6}` for the last group to capture.

## Author

Thanks for the read! Feel free to browse through some of my projects over at...
https://github.com/youseph-codes 