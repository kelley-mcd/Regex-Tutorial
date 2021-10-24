# Gist: Matching an Email Using Regex

The regular expression (regex) I will be using for this homework assignment is the Matching an email regex shown here:
 `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. 

## Summary

The regex used for matching an email can be very useful for many coders and web developers throughout their work. Being able to access email addresses without having to skim each line of data is very useful and efficient especially when dealing with a lot of data. 

In this tutorial I will go through and breakdown the entire matching an email regex and explain each part that goes into making it and how it works.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Escapes](#character-escapes)

## Regex Components

Each regex is encased in literals (``) and slashes (//) so that is a clear indication of when you are working with a regex and is worth noting. Below I will go into detail of the specific parts that make up the regex we are working with.

### Anchors

Each regex begins and ends with an anchors ^ and $ respectivly. Any charachter that comes after the ^ indicates that it is where the regex starts searching for the items it needs to fulfill the requirements. The $ signifies that it is the end of the regex and that everything that comes before it is part of the regex and will be searched for when using it.

We can see that our regular expression has all of these requirements so far, so we know it is indeed a regex.

### Quantifiers

Quantifiers define the minimum and maximum of a specific section of the regex. In our case, the quantifiers are `{2,6}`. They are located at the end of the regex so that tells us that the email addresses we are looking for do not have a limit of how long they are BEFORE the `.`. After the `.` the regex is only looking for something that is between 2 and 6 characters long. For example, .com and .edu are endings to email addresses that are most commonly used.

### Grouping Constructs

By looking at our regex, we can tell that there are three separate groups within our one regex. We know this because there are three groupings of parentheses (()) used throughout the expression. They are as shown:
   - [a-z0-9_\.-]
   - [\da-z\.-]
   - [a-z\.]
The order of these groups is very important because all email addresses are/ need to be set up the same way: blahblahblah@blah.blah. The first section needs to come first, second needs to come second, and third needs to come third. This is the case because the parentheses require the expression to act in order respectively.

### Bracket Expressions

The brackets represent the actual string that the expression is looking for. It is a way to group the characters together and separate the anchors from the actual items the regex is looking for.

### Character Escapes

Character escapes are to be taken literally. For example, in our matching an email regex: 
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
We can see that there are 5 separate character escapes. 

They are:
   - \.
   - \d
   - \.
   - \.
   - \.

The backslash ( \ ) in all of the ( \. )  is meant to tell the regex to take the (.) literally and search for that as one of the characters in the email addresses. It is aknowledging that email addresses can contain periods (.) in the naming part of the email (for example: kell.mcd@gmail.com is a valid email that would be picked up by the regex because the period os quite literally there in the name.)

The same goes for where ( \. ) is found in the rest of the regex, it can, quite literally, contain a period (.). 

The ( \d ) character escape represents any number 0-9

## Author

Kelley McDonnell is currently enrolled in the UNH Coding Bootcamp and is to graduate with a certificate in coding in December 2021.

GitHub: https://github.com/kelley-mcd
