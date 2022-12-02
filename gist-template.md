# Regex Tutorial
This is a short introductory tutorial to regular expressions (regex) and the components used within them. By the end of this tutorial you should understand each character's purpose in the regex exapmle and what it is searching to match.

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.
The regex we are going to be looking at is used to match a URL. It may look intimidating, but we will break it down into individual parts so you can better understand their meaning. This tutorial is broken down into sections that will explain the parts of the regex example in groups. Here is the example:

Matching a URL: `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Character Escapes](#character-escapes)


## Regex Components

### Anchors
This expression starts and ends with anchors. The '^' anchor marks the beginning and the '$' anchor marks the ending of this expression. Anchor tags are important to the construction of a regex because they contain the code and set you up for success.

### Quantifiers
This expression uses two different quantifiers. The first is '?'. This character matches the preceding element either 0 or 1 times. This means that, for the url regex, 'https?' matches 'http' followed by zero or one 's'. When placed after parentheses, the question mark quantifier matching everything in the preceding parentheses either 0 or 1 time. In other words, this regex will match 'http(s)://' if it is there, but it could also not be present and the expression will continue to match what comes next. This is done for this particular regex because url's will sometimes have http(s):// at the front, but sometimes it will not. If the https:// is not included the rest of the address could still be valid.

The other qualifier used in this expression is {2,6}. This qualifier matches the preceding element at least 2 times, but not more than 6 times. The preceding element in this case is any lowercase letters and/or periods. This is used for what is typically the 'com' part of the url. The way the expression is written is broad enough to include less common alternatives such as 'me', 'info', or 'com.'.

### Grouping Constructs
Grouping constructs separate an expression in sub-expressions. The use of '()' breaks the regex down into separate parts that can be quantified individually while still contributing to the expression as a whole.

### Bracket Expressions
Brackets such as '[]' separate a set of characters that can be matched. In the url match regex above '[]' are used frequently to indicate what characters we are looking to match.

### Character Classes
The characters found between the '[]' brackets are what we are looking to match. The expression above uses several character classes. '\d' matches a digit. 'a-z' matches any lowercase letter. '\w' matches any word character. '\.' matches any periods and '\/' matches any forward slashes.

### Character Escapes
The '\' is used in regex to specify a character escape. THe character is matched literally or stands for a character escape class. The characters '\/' and \.' in this expression look to match the literal characters '/' and '.' The characters '\d' and '\w' are meta-characters that represent a class of characters. In this case it will match any digit and any word character respectively.

## Author

My name is Autumn. I am a coding bootcamp student. I am grateful for this opportunity to share the research I have done with others and I hope it helps you better understand regex so you can use it to enhance your own coding abilities.

[Github Profile](https://github.com/autumnlegere)
