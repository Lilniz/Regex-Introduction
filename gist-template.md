# Regex Learning Introduction!
Welcome to a brief introductory guide to learning Regex! We'll be quickly diving into the world of Regex, or as it's fully called, Regular Expression. Regular Expression allows a user or program to search with finer, or more specific, detail. Like google search will respond with the words you've type, Regex can be far more particular and precise! 

## Summary
Here we'll take a quick example of a search for an email-matching Regex! It may seem confusing, at first, but by the end of this small tutorial you'll be able to recognize nearly all aspects of Regular Expressions! 

* Matching an Email: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

To better navigate to what you wish to know, just click on the specific link below!

## Table of Contents
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
* The anchor component of a Regular Expression are the characters which start and end the string. 
* As we begin the Regex (a literal) it must be encased in `/ /` to denote the expression. 
* Afterwards is when the Anchors come into play. The `^` character, and `$` character are our wrapping anchors.
* Anything that comes after our `^` will be recognized as the literal, and you will close that string with the` $` character.
* Exaggerated look to see where these characters sit: `/  ^   ([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})   $  /`
* Failure to do so may result in your whole file laced with red errors!

### Quantifiers
* The quantifiers are how you set terms for your matching/searching. There are many to remember!
* The `*` character will match the pattern 0 or more times.
* The `+` will match the pattern at least 1 or more times.
* The `?` will match the pattern 0 to 1 time.
* The `{}` wrappers are unique in that they offer 3 separate ways to set your limits. Example: `{2,6}`
    * The first `{}` option is `{n}`: this matches the pattern the exact amount of times expressed.
    * The second `{}` option is `{n,}`: this matches the pattern at least the amount of times expressed.
    * The third `{}` option is `{n, x}`: this matches the patter from a minimum (n) to a maximum (x) of times expressed.
* A tip using any quantifier is utilizing the ? afterwards, will ensure the matches are returned as few as possible.

### Grouping Constructs
* The grouping constructs allows for you to further complicate searches. As you see, we have `{}`, `[]`, and even `()`, but only one is a construct!
* `()` are how we group things together! You can have multiple of these, and even within each other. These are called subexpressions.
* `([a-z0-9_\.-]+)` is an example showing that we want to ensure one part of our search look for multiple parameters.
    * And the `+` will ensure we match this pattern at least 1 time, or more!
* If you didn't guess how the above example is read, we'll explain it below.
* Our `[a-z ]` is looking for any letter of a to z.
* Our `[ 0-9 ]` is looking for any number of 0 to 9.
* Our `[ _/.-]` is looking for any of these specific characters.
* A hint, this does matter as they all fall into the same `()`.
* To ensure subexpressions follow one after the other in a specific order, just add `:` to the middle. Like this: `(0-9):(a-z)`

### Bracket Expressions
* The bracket expressions are ways to represent a range of characters you need to matchm and outline the characters you want to include.
* They can be used simply with `[]`, and as an example we might make one look like `[coding]`.
    * This will try to find any matches relating to the characters present above, regardless of position, and is a bit broad.
* If you want to find a range between character/letters `[b-e]` will find strings which include these letters (still, a lot).
* Other ways to utilize bracket expressions are via numbers, `[1-4]`, or special characters, `[-_]`.
    * Hint: Brackets are case sensitive for the letter characters.
* You can place many search parameters together within these brackets, as seen in our Regex: `[a-z0-9_\.-]`
    * This will find any lowercase letter, any number, and the 4 special characters, as a string within our file!

### Character Classes
* Character classes are what define a set of characters. The most common being `.`, `\d`, `\w`, and `\s`.
    * We use back slashes for these!
* The `.` class will match any character except a `\n`.
* The `\d` class will work just as a bracket expression `[0-9]`.
* The `\w` class will match and alphanumeric alphabet, including `_`. 
    * It is equivalent to `[A-Za-z0-9_]`.
* The `\s` will match whitespace characters... spaces, tabs, line breaks.
* A hint for character classes. If you wish to try and find the inverse, capitalize your letter within the class.
    * Example: `\D`, `\W`, `\S`.

### The OR Operator
* This is a quick section! The or operator is just the straight line `|`!
* `|` will function as a way to allow positions within our grouping constructs (which are specific), to change!
* `|` in a string of `(123)`, where it will find only results having that exact string, can be varied.
    * `(1|2|3)` can now return results which any order of those 3 numbers are found together!

### Flags
* Flags are a way to add additional search functionality without placing them within our /^ $/ (being and ending slashes).
* These flags are placed at the end of the Regular Expression after the closing slash!
* There are 6 optional flags but 3 are the main ones to know.
    * `g` is the first flag. It is a global search which tests the Regex against all possible matches in a string.
    * `i` is the second flag. It is a case-INsensitive search which case is ignored while attempting to match a string.
    * `m` is the third flag. It is a multi-line search which multiple line input strings will be treated as such.

### Character Escapes
* Another quick section, character escapes within a Regex allow a character that would normally be searched literally.
* The character escape is a `\`, (back slash)!
    * Example: `({ )` begins a quantifier but you can add the back slash to allow the search to ignore that!
        * `(\{ )` will allow for the `{` to be searched instead as a special character and not a way to group other parameters!
* The `\` and other special characters lose their significance within a bracket expression!

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
Lee Boettcher is an aspiring Full Stack Web Developer with a years worth of study (via bootcamp) already under his belt. Although the quick paced learning expanded his knowledge quickly, he understands that mastery comes with years of application and study!

GitHub [Profile](#https://github.com/Lilniz)