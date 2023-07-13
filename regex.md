# Matching an Email: with regex

We will be breaking down Reqular expression with using an email expression. The expressions can help us find strings that match based on a search pattern instead of litral searches. For example if we want to find all the emails in a document but we don't want to search for each email, this allows us to find all the emails at once. This is when we would use a Reqular expression or for short regex. 


## Summary
In the document we will be breaking down a reqular expression. We will use an email expression to help complete this task. At first the series of charcters will look very confusing but after we break it down it will be very easy to understand. 
For exaple, if we want to find all the emails in a specific document, we would use a regular expressiong like the one below.
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
We start off with wanting any letter and number from a-z 0-9 and it can also contain _\+]-. that must be followed by the @ symbloe. Then any number from 0-9 which we use \d for short hand. We will cover this later in the docoument and any chracters a-z and  _\+]-. Then the string must contain . followed by any a-z characters and .. last it must me more then 2 charcters and no more than 6. 



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
^ and $ are both anchors.  The ^ anchor is the beginning of the regex. The $ is the end of the regex statement. When using anchors, it is imperative that case sensitivity is accounted for as it can not work if it doesnt match.  Since the ^ is at the beginning, anything that follows will be used to search unless it is stopped with a $.
### Quantifiers
Quantifiers set the limit for the string in which the regex will match. They will often include a minimum and maximum number of characters.
exaple of quantifiers are 
 *- matches the pattern zero or more times =
 +- matches the pattern one or more times 
 ?- matches the pattern zero or one time.
 {}- currly brackets can provide three different ways to limit for a match 
 {X} will only match exactly x number of times 
 {X, } will only match if it has a minimum X amount of characters.
 {x,x} The first x represents the minimum length and the second x will represent the max length. 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` {2,6} if we take a look at our email regex you will see after the last . we are are looking for at least 2 charcaters and no more than 6.

### Grouping Constructs
For each part of the string on the email regex we use 3 group constructs. The first one being ([a-z0-9_\.-]+) we want to find any thing that matches these characters. Then it must have the @ symbol. Then we use our next grouping contructs ([\da-z\.-]+) then after .([a-z\.]{2,6})` we have our last group constucts. We do this because it could be looking for different characters that match in different parts of the string or even a minimum and max limit on different parts of the string. 
### Bracket Expressions
Bracket excpressions allows us to set a range of characters the we want to match. For example [a-z0-9_\.-] we want to match with any letter and any number 0-9. Also, if there is an _ we want to match and if there is any /. or - we want to come back as a match. 
### Character Classes
character classes are a defined set of charactes. `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` if you notice in our statement we are using \. to create a new line statement and dont want to use the charcater class of . 
. matches any chararter except the newline character. 
\d is equivalent to the bracket epression [0-9]
\w is equivalent to the bracket expression [A-Za-Z0-9_]
\s matches with any single white space 


### The OR Operator
Using the or operator we can write [abc] as (a|b|C) because we are a using the | which is the or operator. The new statement now reads as we want a or b or c. 
### Flags
Flags are placed at the end of a regex and allow us to define additional functionality or limits.
g- Global search our regex should be tested against all posible matches in a string 
i- Case insensitive search this will ignore cases while attempting a match.
m- multi line search a multi line input should be treated as multiple lines. 
### Character Escapes
the backslash is the character escape. Like stated before we are using the character escape with \. because we want to define the . and not match any characters. We could also use this with \{ if we wanted to find a curly brace insted of an open curly brace. 
## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
