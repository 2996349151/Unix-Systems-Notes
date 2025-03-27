## Regular Expressions

```Bash
# Use grep
grep "pattern" filename
# output matched lines
# pattern can be a string or a regular expression
# grep flags:
# -E: patterns are regular expressions
# -F: strings
# -v: select non-matching lines
# -c: ouput the count of selected lines
```

* Regular Expressions
  * Literals: exact character
  * Metacharacters
  * Character Classes: 
    * "[abc]": matches a or b or c
    * "[A-Za-z]": matches any letter
    * "[^A-Z]": matches no capital letter
    * "\d": equals to [0-9] (not for Bash)
    * "\w"; equals to [A-Za-z0-9_]
    * "\s": any whitespace character
    * "\b": word boundary
    * ".": anything
  * POSIX extended notation:
    * [:alnum:] is  [:digit:] or [:alpha:]
    * [:alpha:] is any letter
    * [:blank:] is a space or tab
    * [:cntrl:] is any control character
    * [:digit:] is any of 0 1 2 3 4 5 6 7 8 9
    * [:graph:] is not [:alnum:] nor [:punct:] 
    * [:lower:] is low case characters
    * [:upper:] is upper case
    * [:print:] is any printable character
    * [:punct:] is any punctuation character
    * [:space:] is any of :CR FF HT NL VT SPACE
    * [:xdigit:] is any  hexadecimal digit
  * Quantifiers
    * *: 0 or more occurrences
    * +: 1 or more occurrences
    * ?: 0 or 1 times
    * {n}: exactly n times
    * {n,}: n or more
    * {n,m}: n to m times
  * Anchors
    * ^: matches the start of a string
    * $: matches the end of a string
  * Groups and Alternation
    * (): group
    * |: or
  * Example:
    * Email address: "^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$"
    * US phone number: "^\(\d{3}\) \d{3}-\d{4}$"

```Bash
# For a string, use =~ to use regular expression
re="^[A-Za-z]"
read DATA
if [[ $DATA =~ $re ]]; then
    echo "The string begins with a character"
else
    echo "False"
fi
```