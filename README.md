# jsof
JSON-Flat AKA Nestable-CSV.

## Purpose
To combined the best of JSON and CSV.
JSOF is meant to be a compact yet nestable format. 

## Warning
- It is meant for recurring data with fixed nested structures.
- It is not meant for data that is nested recursively.

## Data types
Same as JSON

## Reserved characters
```
| (pipe) Field delimiter
, (comma) List item delimiter
% (percentage) Dictionary key
$ (dollar) Prefix for string
{} (curly brackets) For enclosing properties names
[] (Square brackets) For enclosing list 
o (Letter o) Literal for true
x (Letter x) Literal for false
 (nothing) Means null

```
If the json key or value contains any of the characters above, they shall be escaped with backslash.  Example :
```json
[{
    "name": "john[fake]",
    "age" : 12
}]
```
In JSOF in will be:
```
name|age
john\[fake\]|#12
```