## Delete all duplicate lines
Code: `^(.*)(\r?\n\1)+$` -> Replace with `\1`
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
Code: `.{1}$` -> Replace: `` (nothing)
