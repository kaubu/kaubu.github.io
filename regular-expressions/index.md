## Delete all duplicate lines
Code: `^(.*)(\r?\n\1)+$` -> Replace with `\1`
## Delete all lines with XYZ string
Code: `.*XYZ.*\r?\n` -> Replace with empty string
## Replace new lines with X
Can replace new lines with `, ` to make a python list, for example.

Code: `[\r\n]+` -> replace with `X`
