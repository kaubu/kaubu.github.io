## Delete all duplicate lines
Code: `^(.*)(\r?\n\1)+$` -> Replace with `\1`
Replace with ` ` (nothing) in order to remove every singe line that ever had more than one copy, rather than removing the copy
## Delete all lines with XYZ string
Code: `.*XYZ.*\r?\n` -> Replace with empty string
## Replace new lines with X
Can replace new lines with `, ` to make a python list, for example.

Code: `[\r\n]+` -> replace with `X`
## Remove lines ending with XYZ
Code: `[^%]*XYZ` -> Replace with empty string

This will leave a lot of empty lines.
## Remove empty lines
Code: `^(?:[\t ]*(?:\r?\n|\r))+` -> replace with nothing

## Surround each line with characters X and Y
Code: `^(.*)$` -> Replace: `X\1Y`

For example:
* to surround everything in brackets, replace with: `\(\1\)`
* to surround everything in curly brackets, replace with: `{\1}`

## Delete first and last characters of each line
### Delete first character
Code: `^.?(.*)` -> Replace: `\1`
### Delete last character
Code: `.{1}$` -> Replace: ` ` (nothing)

## Delete everything after X
Code: `X.*` -> Replace: ` ` (nothing)

## Insert at the start of each of line
Code: `^(.*)` -> Replace: `{text}\1`
## Insert at the end of each line
Code: `(.*)$` -> Replace: `\1{text}`

## Miscellaneous
### Capture everything within "{number} [word1 word2 word3, etc] "
`\d \[.+\] `
### Capture verbs that end in a single l
#### Linux
`.*[aeiou]ling\n` – Gerund or Present Participle

`.*[aeiou]led\n` – Simple Past tense
#### Windows
`.*[aeiou]ling\r\n` – Gerund or Present Participle

`.*[aeiou]led\r\n` – Simple Past tense

### Delete Wikipedia citations

`\[..?\]` → Replace: ` ` (nothing)
