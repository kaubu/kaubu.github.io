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
