## File Operations
```Bash
# Get number of lines
wc -l filename
cat filename | wc -l

# Redirection
# Redirect line 1 to file3, line 2 to file4
ls file1 file2 1> file3
ls file1 file2 2> file4
# print file1 to file2
cat file1 > file2 

# Piping
# Print content of a file
cat filename
# Pipe symple |, meaining command 1's output is used for command 2's input
# Print less content of filename
cat filename | less

# Cut Some content
# Only print first column
cat filename | cut -d : -f 1

* Single quote presents special meaning, double quote presents literal meaning, except $, \, etc


```bash
# IF
Space for [[ and ]] are needed
if [[ some_condiition ]]; then
# command
else
# command
fi

# Loop
while [[ some_condiition ]]; do
# command
done
#Available condition:
# while [[ $count -ls 5 ]];
# while read line;
# while true;

for i in variable; do
# command
done
# Available variable:
# for i in {1..5};
# for i in $var1 $var2 $var3;
# for ((i=1;i<5;i++));
# for i in *.txt;
```