# Structured Text Format Documentation

This document explains the syntax and structure for the custom text format used to represent biblical verses and related notes.

## Reference for Indexing

The reference format is used to index and relate verses in notes. It allows cross-referencing between different parts of the text. Is denoted by `ref:` between two `---`.

Example:

```
---
ref: juan_1
---
```

## Structure

The following is the structure used for the text format:
**Every versicle goes in a new line** for git and scalability porposes, but this new lines in the file are ignored by parsers, for explicit new lines you need to use `\n`, in parsers this will add a `\n\t` as uses of new line in bible context requires.

### Italian text
Italian text can be used as in markdown: `_text_`

### Title
A title is denoted by a single `#` at the beginning of the line (Usually only used to name the chapter).

### Subtitle
A subtitle is denoted by a double `##` at the beginning of the line.

### Versicle Number
A versicle number is represented as `\*[0-9]{0,3} ` (RegEx), where the number can be one to three digits.

Example: `*123 `

### Versicle with Note Number
A versicle with an associated note number is written as `*[0-9]{0,3}\{\{.\}\} `(RegEx), where the dot indicates the note.

Example: `*123{{note}} `

#### Vesicle with Note Number and next
Example: `*123{{s. note}} `

#### Vesicle with Note Number and nexts
Example: `*123{{ss. note}} `

### Vercicle reference

Example: Génesis 1:1 = `*/genesis-1-1`

### Vercicle range reference

Example: Génesis 1:1/10 = `*/genesis-1-1/10`

#### Versicle and nexts reference

Example: Génesis 1:1 ss. = `*/genesis-1-1-ss`

### Chapter reference

Example: Génesis 1 = `*/genesis-1`

For more details, please refer to the [example.rdcf](./example.rdcf).
