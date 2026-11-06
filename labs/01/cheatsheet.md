## Text

### Headings
**CommonMark** · One to six hash signs (`#`) at the beginning of a line, followed by a space, make a heading. One hash sign is the top level, six the lowest. Without the space (#Heading) or with seven hash signs, it stays plain text.

```markdown
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6

### Paragraphs and Line Breaks
**CommonMark** · A single line break gets ignored, the lines will still be joined. A blank line starts a new paragraph. A backslash (`\`) or two spaces (`  `) force a line break.

```markdown
A blank line starts a new paragraph.

A single line break
...gets ignored, but a backslash\
or two spaces
force a line break.
```

A blank line starts a new paragraph.

A single line break
...gets ignored, but a backslash\
or two spaces  
force a line break.

### Italic
**CommonMark** · One asterisk (`*`) or underscore (`_`) on each side makes the text italic.

```markdown
*This text is italic.*
_This text is also italic._
```

*This text is italic.*  
_This text is also italic._

### Bold
**CommonMark** · Two asterisks (`*`) or underscores (`_`) on each side make the text bold.

```markdown
**This text is bold.**
__This text is also bold.__
```

**This text is bold.**  
__This text is also bold.__

### Bold and Italic
**CommonMark** · Three asterisks (`*`) or underscores (`_`) on each side make the text bold and italic.

```markdown
***This text is bold and italic.***
___This text is also bold and italic.___
```

***This text is bold and italic.***  
___This text is also bold and italic.___

### Strikethrough

**GitHub** · Two tildes (`~`) on each side cross text out.

```markdown
~~This text is crossed out.~~
```

~~This text is crossed out.~~

### Inline Code
**CommonMark** · Backticks (\``) around a word or a phrase mark it as inline code, a code within a sentence. The text within the backticks will not be rendered as Markdown.

```markdown
`This is inline code.`
```

`This is inline code.`

### Escaping Characters
**CommonMark** · One Backslash (`\`) right before a special formatting character escapes the character and shows its usual form not formatted.

```markdown
\*\*This text is bold.\*\*
\_\_This text is also bold.\_\_
\*This text is italic.\*
\_This text is also italic.\_
```

\*\*This text is bold.\*\*  
\_\_This text is also bold.\_\_  
\*This text is italic.\*  
\_This text is also italic.\_

## Lists

### Unordered, Ordered and Nested Lists
**CommonMark** · One aesterik (`*`), hyphen (`-`) or plus sign (`+`) followed by a space (` `) starts an unordered list. A number with a dot (`1.`) followed by a space starts an ordered list. To create a nested list the line has to be intended to line up with the text above. For unordered lists it's enouph to intend the line wiith one space (` `), for ordered lists it should be at least four spaces (`    `). GitHub shows the intended ordered lists as roman numbers.

```markdown
+ FAIR-Principles
  + Findable
  + Accessible
  + Interoperable
  + Reusable
- Open Source Softwares
  - LibreOffice
  - NextCloud
  - VSCodium
* Open-Source E-Books
  * [Automate The Boring Stuff With Python](https://automatetheboringstuff.com/)
  * [Eloquent JavaScript](https://eloquentjavascript.net/00_intro.html)

1. Find a dataset
2. Check the license
    1. Is it open?
    2. Is it FAIR?
3. Share and discuss it with your teammates
```

+ FAIR-Principles
  + Findable
  + Accessible
  + Interoperable
  + Reusable
- Open Source Softwares
  - LibreOffice
  - NextCloud
  - VSCodium
* Open-Source E-Books
  * [Automate The Boring Stuff With Python](https://automatetheboringstuff.com/)
  * [Eloquent JavaScript](https://eloquentjavascript.net/00_intro.html)

1. Find a dataset
2. Check the license
    1. Is it open?
    2. Is it FAIR?
3. Share and discuss it with your teammates

### Task Lists
**GitHub** · To create a task list a line either starts with empty square brackets (`[ ]`) to show that the task is unchecked or it starts with an `x` in between the square brackets (`[x]`) to show that the task is checked.

```markdown
- [x] Lab 1
- [x] Lab 2
- [ ] Lab 3
- [ ] Lab 4
```

- [x] Lab 1
- [x] Lab 2
- [ ] Lab 3
- [ ] Lab 4

### Inline Links
**CommonMark** · An inline link puts the URL in parantheses (`()`) right after the link text that is put in square brackets (`[]`). 

```markdown
I'm a student at [TH Köln – University of Applied Sciences](https://www.th-koeln.de/).
```

I'm a student at [TH Köln – University of Applied Sciences](https://www.th-koeln.de/).

###  Reference-Style Links
**CommonMark** · A reference-style link uses a label in square brackets (`[]`) and defines the URL elsewhere in the file. The definition will not be shown.

```markdown
The [course repository][course] has all slides. If you are looking for the labs check the [course repository][course] for the files.

[course]: https://github.com/breuert/data-integration
```

The [course repository][course] has all slides. If you are looking for the labs check the [course repository][course] for the files.

[course]: https://github.com/breuert/data-integration

### Relative Link to Another File
**CommonMark** · A link with a path instead of a URL references another file in the same repository. The path starts from the folder of the current file. Two dots (`..`) go up one folder.

```markdown
View the [README](../../README.md) of this repository.
View the [LICENSE](../../LICENSE.md) of this repository.
```

View the [README](../../README.md) of this repository.  
View the [LICENSE](../../LICENSE) of this repository.

