# Title (replace with your title)

Regular Expression, regex, is a sequence of characters that are puzzle-like and they define a specific pattern. They do not require any code like javascript, react, etc. A downside to regex is that they look really confusing. Most people would see them and immediately look away and refuse to try to decode them. Each character has a value and when you put them together you can match any pattern. They are useful for searching things within a pattern but not literal characters. For example searching phone numbers by hand will be difficult if you have to deal with 50+ numbers. They will all have their own unique literal sequence. However regex comes in hand because it allows you to search things based off of their pattern. A phone number will be different and unique but they all have the same pattern, which is 10 numbers. However with regex you can use /d/d/d-/d/d/d-/d/d/d/d to get all numbers or list of literal characters that matches this.

## Summary

The regex expression that I will be describing today deals with an an html address.

/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

I will be going over the different patterns within this expression, and how to split it up for a easier way of thinking

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
For this Tutorial the regex component is 

/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

### Anchors
At the beginning of the expression you will notice a /. 
This forward slash will have the computer look at all the components on the inside. However the Anchor ^ will tell the computer that this is the start of the expression. The $ at the end will tell the computer that this is the end. Anchors will provide you information about the start of a line, string, word. They will also provide you information about the end of a line, string, and word.

### Quantifiers
Quantifiers are used to determine if there is one or more matches. These Quantifiers consist of * ? + 
Letters can also be used in quantifiers as like placeholders. For example { n }
means it matches exactly n times. So think of it as algebra, n could be x and that means that it can be anything. 

### Grouping Constructs
Grouping occurs when parenthesis are used. So for our practice code we see that there is regex within 4 parenthesis. This means that the expression itself can be broken down into 4 parts. The information between the parenthesis is put together by the outside elements.The first group has the 'https we recgonize this from URLs that we see daily. Therefore from the start we should know that we are dealing with an URL. Next to it looks like the letter V. However they are not they represent the // that comes after https:. Each of these groupings will be searching for various different things.

### Bracket Expressions
Anything within a bracket will have a specific critera. It may be that we are looking for something 0-9, A-Z, or a-z. The specific literal characters don't matter, but they need to match this field or requirement in order for the computer to even recgonize it. Within our example we see that [/da-z/.-] is within a bracket. Meaning that we are looking for something that follows these specific guidelines. /d means any number 0-9. 

### Character Classes
In order to understand Regex you have to start off with the basics and know what some of the characters mean.
/d is anything that is numbers 0-9.
/D is anything that is NOT a number 0-9.
/w is absolutely anything, a number, a letter. Uppercase or lowercase. Anything.
/W is anything that is NOT a number, or letter
/s basically takes role of any spaces within the pattern, indents, new lines, etc.
/S deals with anything that is not a whitespace character. 


### The OR Operator
The OR operator is represented by |. This that the pattern that we are looking for can be one specific thing OR it can be another. Meaning that this expression can go two different ways.

### Flags
Flags are kind of like rules for the computer. They have meanings and will tell the computer what to do. For example i will tell the computer to ignore the casing. g will search for all occurences globally in your environment

### Character Escapes
Our example code does not have any Character Escapes but they are kind of like flags. They have hidden meanings and will basically tell the computer what to do. The only difference is that their meanings are much more complicated to remember/understand

## Author

https://github.com/turnerjeniah8/regexTutorial 
