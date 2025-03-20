## Basics
```Bash 
# Who am i
whoami

# Look for command instructions
# Type f and b to go forward and backward
# Type p to exit
info any-command
man any-command
# Find "text" in instructions
# Type n and p to go to next and previous matching answer
/text

# Show current location
pwd

# Show operating system
uname

# Change location
cd path-name
# Go to parent directory
cd ..
# Go to home directory
cd ~

# Create a directory
mkdir dir-name
# Create multiple directories
mkdir dir-name1 dir-name2

# List all files
ls
ls dir-name
# List detailed information
ls -l

# Remove a file or directory (only current directory, no subdirectories)
rm file-name
# Remove all files ending .txt in dir1
rm ~/dir1/*.txt
# Remove a nonempty direectory
rm dir-name

# Create empty files (redirection commands, same as >)
touch file1 file2 file3
# Create a file and overwrite a file with content
echo "text" > file-name
# Append a file with content
echo "text" >> file-name


# Copy files
cp file1 file2 target-dir

# Rename a file
mv file1 new-name
# Move a file
mv file1 target-dir

# Search in current directory
echo file-name
# * present any character, any length, ? present any character, one length (THIS ALSO WORKS IN OTHER COMMANDS, SUCH AS cp)
# Find filenames containing o
echo *o*
# Find filename ending .py
echo *.py
# Find filename with length 3
echo ???
# Print without going to new line
echo -n text
```

## Nano editor
```Bash
# Create or edit a file
nano file-name
```