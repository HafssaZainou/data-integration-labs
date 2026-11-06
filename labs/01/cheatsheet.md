### Strikethrough

**GitHub** · Two tildes(~) on each side cross text out.

```markdown
~~This text is crossed out.~~
```

~~This text is crossed out.~~

### Bold
**CommonMark** . Two asterisks(*) or underscores(_) on each side make the text bold.

```markdown
**This text is bold.**
__This text is also bold.__
```

**This text is bold.**  
__This text is also bold.__

### Italic
**CommonMark** . One asterisk(*) or underscore(_) on each side makes the text italic.

```markdown
*This text is italic.*
_This text is also italic._
```

*This text is italic.*  
_This text is also italic._

### Bold and Italic
**CommonMark** . Three asterisks(*) or underscores(_) on each side make the text bold and italic.

```markdown
***This text is bold and italic.***
___This text is also bold and italic.___
```

***This text is bold and italic.***  
___This text is also bold and italic.___

### Headings
**CommonMark** . One to six hash signs (#) at the beginning of a line, followed by a space, make a heading. One hash sign is the top level, six the lowest. Without the space (#Heading) or with seven hash signs, it stays plain text.

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

### Inline Code
**CommonMark** . Backticks (``) around a word or a phrase mark it as an inline code, a code within a sentence. The text within the backticks will not be rendered as Markdown.

```markdown
`This is inline code.`
```

`This is inline code.`

### Escaping Characters
**CommonMark** . One Backslash (\) right before a special formatting character escapes the character and shows its usual form not formatted.

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

### Paragraphs and Line Breaks
**CommonMark** . A single line break gets ignored, the lines will still be joined. A blank line starts a new paragraph. A backslash (\) or two spaces (  ) force a line break.

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
