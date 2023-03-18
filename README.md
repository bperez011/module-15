# module-17 REGEX  

##What Is a Regex?

A regex, which is short for regular expression, is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input.

For example, the following regular expression can be used to verify that user input is a valid email address:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/


##User Story

AS A web development student
I WANT a tutorial explaining a specific regex
SO THAT I can understand the search pattern the regex defines

##Acceptance Criteria

GIVEN a regex tutorial
WHEN I open the tutorial
THEN I see a descriptive title and introductory paragraph explaining the purpose of the tutorial, a summary describing the regex featured in the tutorial, a table of contents linking to different sections that break down each component of the regex and explain what it does, and a section about the author with a link to the author’s GitHub profile
WHEN I click on the links in the table of contents
THEN I am taken to the corresponding sections of the tutorial
WHEN I read through each section of the tutorial
THEN I find a detailed explanation of what a specific component of the regex does
WHEN I reach the end of the tutorial
THEN I find a section about the author and a link to the author’s GitHub profile

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
- [gist repo link](#gist repo link)

## Regex Components

### Anchors

- The first thing seen in the matching email snippet above is `^`.  This means beginning so it means email should start with `([a-z0-9_\.-]+)` expression. 
If it’s `^The`, it searches any strings that start with The. 
- The last thing seen is `$`. It means end, so email should end with `([a-z\.]{2,6})` expression. If it’s `end$`, it searches any strings that end with end.


### Quantifiers

- `*` is one or more - `cde*` means cde followed by zero e to more e 
- `+` is one or more - same as above 
- `?` is zero or one - `cde?` means it does not matter if e is contained or not, it matches both `cd` and `cde`  
- `{}` - if `cde{2}`, `cdee` matches.  


### OR Operator

- `|` means or. For example if `abc|xyz`, both `abc` and `xyx` match.
- `[]` functions the same as above. 

### Character Classes

- `\d` matches a single digital character
- `\w` matches one word character, it does not matter if the character is a letter or digital character
- `\s` mathes a white space
- `.` matches any character

### Flags

Flag is `/` and it means to create a regex between the slashes. As it is seen at the beginning and the end in the example of matching email regex, the flag is also seen in the search bar when you want to search for a regex. 
- `/g` means global search and dot return after the first search. 

### Grouping and Capturing

- `()` means to create a capturing group. For example,  if `c(ba)`, only `cba` matches. It does not matter if it is in the middle of a string like fdsd`cba`sfdsf.
- `?:` means to disable a capturing group. When `a(?:bc)`, both `abc` and `a` match.


### Bracket Expressions

- `[]` means it matches anything contained in brackets. `[abc]` matches `a`, `b` and `c`. It is the same expression as `a|b|c` 

- `[a-c]` is the same expression as above. 

- `[a-fA-F0-9]` matches any letter from `a` to `f`, `A` to `F` and `0` to `9`).

- `[^a-zA-Z]` matches any letter without `a` to `z` and `A` to `Z`. 


### Greedy and Lazy Match

- Greedy search

  - The quantifiers `( * + {})` explained above are called greedy operators, so they expand the match as far as they can through the provided text. It will try to match the longest possible string. 


- Lazy search 
  - `?` is used for this mode. `/".+?"/g` is used to match any characters between `“”` mark. For example if a sentence is `”Coding” is fun.`, only `Coding` which is between the double quotation marks is searched.  


### Boundaries

- `\b` is used to search a whole word. For example if `\bapple\b`, only `apple` will match, no `greenapple` or `redapple`. 

### Back-references

- `([abc])\1` means to match any first letter in the capturing group. For example, it searches for consecutive characters such as `aa`, `aaaaaa`, `bb`, `bbbbbb` and `cc`, `cccccc`. It does not limit how many letters continue.

### Look-ahead and Look-behind

- `d(?=g)` only `d` followed by g matches, for example, `d`g but not dt. G in `d`g is not included in the match.  

- `(?<=f)g` means only `g` preceded by f matches. For example, g in `g`f matches but f is not included in the match.

### gist repo link

@
