
# Lab 1
## Basic commands
```Bash 
# Who am i
whoami

# Look for command instructions
# Type f and b to go forward and backward
# Type p to exit
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
# Create a file with content
echo "text" > file-name
# Overwrite with content
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
```

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
```

## Nano editor
```Bash
# Create or edit a file
nano file-name
```