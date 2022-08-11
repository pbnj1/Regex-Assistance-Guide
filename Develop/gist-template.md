# Regex Assistance Guide

Regex - or regular expression (sometimes referred to as rational expression) is a sequence of characters that refers to a specific pattern in text.  Often times these patterns might be used by string search algorithims.  This guide will help explain how to use a certain regex pattern and hex value. 

## Summary

The following expression will be used as part of this guide for evaluation and training: 

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

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

### Anchors:  ^ Code snipet : /^#   


    Anchors do not match any specific character in regex.  Insteady, they match a position before or after characters.   

            example:  /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

                    ^ – The caret anchor matches the beginning of the text.
                    $ – The dollar anchor matches the end of the text.

### Quantifiers


    Quantifiers match a number of instances of a character, group, or character class in a string.

            example:  /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

                  A number in curly braces {3} is the simplest quantifier. When you append it to a character or character class, it specifies how many characters or character classes you want to match.  An easier example would be B{4} - indicating that B should be repeated 4 times.  

### Grouping Constructs


    Grouping Constructs use the ( ) to gather the regex on the inside of the paranthesis.  This grouping will be treated as a single unit.  It will then be used as an array 

            example:  /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

                Everything in the paranthesis is captures as part of a subsection in this example.  


### Bracket Expressions

    Bracket Expressions [ ] is utilized to match a set of characters from within the bracket.  

            example:  /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

                [a-f0-9] is the bracketed component with the search looking to match any character between the brackets. 


### Character Classes

    Character Classes match characters that are enclosed within brackets.

            example:  /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

                [a-f0-9] in this bracket expression we have character classes to be searched between a-f and between 0-9.  

### The OR Operator

    The OR operator is a comparison operator like in standard javascript with the | sign.

            example:  /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

                The or sign | breaks the expression into two groups [a-f0-9]{6} and [a-f0-9]{3}


### Flags

    Flags are used with various qualities to affect the search.  

            example:  /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

                There are no flags in this search.  However the 6 flags include:
                    
                    i - With this flag the search is case-insensitive
                    g - With this flag the search looks for all matches, without it – only the first match is returned.
                    m - Multiline mode
                    s - Enables “dotall” mode, that allows a dot . to match newline character \n
                    u - Enables full Unicode support. The flag enables correct processing of surrogate pairs.
                    y - “Sticky” mode: searching at the exact position in the text

### Character Escapes

    Character escapes are performed with the backslash \

            example:  /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

                There are no character escapes in our code exmaple - however if present it would togle on/off the character vs. literal status of the character in front of it. 

## Author

Tutorial by Pete Wang.

I am a student of software development and am inspired to help use technology to improve quality of life, to reduce global climate consequences of inaction, and build a better kinder society.  


[Github](https://github.com/pbnj1)

