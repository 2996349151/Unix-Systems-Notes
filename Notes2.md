# Scripting Basics

## File permissions
File information  
* Permission:
* File type(1 digit) + onwer permission(3 digits) + group permission(3 digits) + others permission(3 digits)
  * r--: can read
  * rw-: can read, write
  * r-x: can read, execute
  * rwx: can read, write, execute
* Hard link count
* Owner
* Group
* File size (in bytes)
* Modification data & time
* File name

```Bash
# 0: no permission
# 4: can read
# 2: can write
# 1: can execute
# 6(4+2): can read, write
# 5(4+1): can read, execute
# 3(2+1): can write, execute
# 7(4+2+1): can read, write, execute

# All permissions to owner and group, no permission to others
chmod 770 file-name
# All permissions to owner, readble, writable to group, exectable to others
chmod 761 file-name

# u: file owner
# g: other members of the owners
# o: all other users
# a: all users

chmod u+x file-name
chmod g-rw file-name
chmoe a=rxw file-name
```

## Shell Scripts
```Bash
# Create script
nano filename.sh

# Set persimssion
chmod u+x first.sh

# Execute
./filename.sh
```

* In the script file:
```Bash
# Then this file runs Bash command
#!/bin/bash
```

```Bash
# Variable
# $variable is to reference, only variable is to assign
ATEST = 'mydata'
echo $ATEST
export ATEST

# Command substitution
lsoutput = 'ls -l'
echo $lsoutput

# Input
read filename
echo $filename

# $0 stores the name of the script.
# $# stores the number of arguments.
# $* stores the complete argument list.

# Argument
./file-name.sh arg1 arg2 arg3
# $n stores nth arguements

# IF
if [[some_condiition]]; then
# command
else
# command
fi

# Loop
while [[some_condiition]]; do
# command
done

for i in variable; do
# command
done

# Return
exit return_value

# String add
added_s = $s1$s2

# Arithmetic operations
echo $((v1 + v2))
echo $((v1 + 1))

# Number Comparision
# -eq, -ne
# -gt, -ge
# -lt, -le

# String Comparision
# ==
# !=
# >
# <
```