## IBM cheat-sheets

### Linux terminal tips
---
> Use **tab completion** to autocomplete pathnames and command names.

> Scroll through your **command history** with the `Up Arrow` and `Down Arrow` keys to find and re-run a command you already used.
#### Display the reference manual for the `ls` command:
1. `man ls`
### Browsing and navigating directories
---
#### Special paths

| Symbol | Represents path to                  |
| ------ | ----------------------------------- |
| `~`    | home directory                      |
| `/`    | root directory                      |
| `.`    | present working directory           |
| `..`   | parent of present working directory |
##### List files and directories in the current directory:
1. `ls`
##### List files and directories in a directory:
1. `ls path_to_directory`
##### Return path to present working directory:
1. `pwd`
##### Change the current directory to a subdirectory:
1. `cd child_directory_name`
> **Tip**: Because `cd` looks in the current directory for `child_directory_name`, you don’t need to type the entire path.
##### Change the current directory:
> **Up one level:**  
1. `cd ../`
> **To home:** 
1. `cd ~` or `cd`
> **To some other directory:**
1. `cd path_to_directory`
##### Change the current directory to another one at the same level:
> Suppose you have two sibling directories within the same directory, `dir_1` and `dir_2`, and your present working directory is `dir_1`. To switch to `dir_2`, enter:
> 
> `cd ../dir_2`

> **Tip**: Using `..`, you don't need to know the path to the parent directory to switch to a sibling.
##### Change the current directory back to the directory you were in previously:
> `cd -`
### Upgrading and installing packages
---
##### Fetch and display up-to-date information about all upgradable packages:
1. `sudo apt update`
##### Upgrade to the latest supported version of nano:
1. `sudo apt upgrade nano`
##### Install Vim:
1. `sudo apt install vim`
### Creating and editing files
---
##### Create a new text file and open it with nano:
1. `nano file_name.txt`
> **Tip**: If the file already exists, nano simply opens it for editing.
##### Return your user name:
1. `whoami`
##### Return your user and group id:
1. `id`
##### Return operating system name, username, and other info:
1. `uname -a`
##### Display reference manual for a command:
1. `man top`
##### List available `man` pages, including a brief description for each command:
1. `man -k .`
##### Get help on a command:
1. `curl --help`
##### Return the current date and time:
1. `date`
### Navigating and working with directories
---
##### List files and directories by date, newest to last:
1. `ls -lrt`
##### Find files in directory tree that end in `.sh`:
1. `find -name \'\*.sh\'`
##### Return path to present working directory:
1. `pwd`
##### Make a new directory:
1. `mkdir new_folder`
##### Change the current directory:
> **Up one level:**
1. `cd ../`
> **To home:**
1. ``cd ~` or `cd``
> **To some other directory:** 
1. `cd path_to_directory`
##### Remove directory verbosely:
1. `rmdir temp_directory -v`
### Monitoring system performance and status
---
##### List selection of/all running processes and their PIDs:
1. `ps`
2. `ps -e`
##### Display resource usage:
1. `top`
##### List mounted file systems and usage:
1. `df`
### Creating, copying, moving, and deleting files:
---
##### Create an empty file or update existing file's timestamp:
1. `touch a_new_file.txt`
##### Copy a file:
1. `cp file.txt new_path/new_name.txt`
##### Change file name or path:
1. `mv this_file.txt that_path/that_file.txt`
##### Remove a file verbosely:
1. `rm this_old_file.txt -v`
### Working with file permissions
---
##### Change/modify file permissions to 'execute' for all users:
1. `chmod  +x  my_script.sh`
##### Change/modify file permissions to 'execute' only for you, the current user:
1. `chmod u+x my_file.txt`
##### Remove 'read' permissions from group and other users:
1. `chmod go-r`
### Displaying file and string contents
---
##### Display file contents:
1. `cat my_shell_script.sh`
##### Display file contents page-by-page:
1. `more ReadMe.txt`
##### Display first 10 lines of file:
1. `head -10 data_table.csv`
##### Display last 10 lines of file:
1. `tail -10 data_table.csv`
##### Display string or variable value:
1. `echo "I am not a robot"`  
2. `echo "I am $USERNAME"`
### Basic text wrangling
---
#### Sorting lines and dropping duplicates:
##### Sort and display lines of file alphanumerically:
1. `sort text_file.txt`
>In reverse order:
2. `sort -r text_file.txt`
##### Drop consecutive duplicated lines and display result:
1. `uniq list_with_duplicated_lines.txt`
#### Displaying basic stats:
##### Display the count of lines, words, or characters in a file:
> **Lines:**
1. `wc  -l table_of_data.csv`
> **Words:**
2. `wc  -w my_essay.txt`
> **Characters:**
3. `wc  -m some_document.txt`
#### Extracting lines of text containing a pattern:
Some frequently used options for `grep`:

| Option | Description                                      |
| ------ | ------------------------------------------------ |
| `-n`   | Print line numbers along with matching lines     |
| `-c`   | Get the count of matching lines                  |
| `-i`   | Ignore the case of the text while matching       |
| `-v`   | Print all lines which do not contain the pattern |
| `-w`   | Match only if the pattern matches whole words    |
##### Extract lines containing the word "hello", case insensitive and whole words only:
1. `grep  -iw hello  a_bunch_of_hellos.txt`
##### Extract lines containing the pattern "hello" from all files in the current directory ending in `.txt`:
1. `grep  -l hello  *.txt`
#### Merge two or more files line-by-line, aligned as columns:
Suppose you have three files containing the first and last names of your customers, plus their phone numbers.
##### Use `paste` to align file contents into a Tab-delimited table, one row for each customer:
1. `paste first_name.txt last_name.text phone_number.txt`
##### Use a comma as a delimiter instead of the default Tab delimiter:
1. `paste -d "," first_name.txt last_name.text phone_number.txt`
#### Use the `cut` command to extract a column from a table-like file:
Suppose you have a text file whos rows consist of first and last names of customers, delimited by a comma.
##### Extract first names, line-by-line:
1. `cut -d "," -f 1 names.csv`
##### Extract the second to fifth characters (bytes) from each line of a file:
1. `cut -b 2-5 my_text_file.txt`
##### Extract the characters (bytes) from each line of a file, starting from the 10th byte to the end of the line:
1. `cut -b 10- my_text_file.txt`
### Compression and archiving
---
##### Archive a set of files:
1. `tar -cvf my_archive.tar.gz file1 file2 file3`
##### Compress a set of files:
1. `zip my_zipped_files.zip file1 file2`   
2. `zip my_zipped_folders.zip directory1 directory2`
##### Extract files from a compressed zip archive:
1. `unzip my_zipped_file.zip` 
2. `unzip my_zipped_file.zip -d extract_to_this_direcory`
### Working with networking commands
---
##### Print hostname:
1. `hostname` 
##### Send packets to URL and print response:
1. `ping  www.google.com`
##### Display or configure system network interfaces:
1. `ifconfig`   
2. `ip` 
##### Display contents of file at a URL:
1. `curl  <url>`
##### Download file from a URL:
1. `wget  <url>`

```bash
```
### Bash shebang
---
1. `#!/bin/bash`
### Get the path to a command
---
1. `which bash`
### Pipes, filters, and chaining
---
##### Chain filter commands together using the pipe operator:
1. `ls | sort -r`
##### Pipe the output of manual page for `ls` to `head` to display the first 20 lines:
1. `man ls | head -20`
##### Use a pipeline to extract a column of names from a csv and drop duplicate names:
1. `cut -d "," -f1 names.csv | sort | uniq`
### Working with shell and environment variables:
---
##### List all shell variables:
1. `set`
##### Define a shell variable called `my_planet` and assign value `Earth` to it:
1. `my_planet=Earth`
##### Display value of a shell variable:
1. `echo $my_planet`
##### Reading user input into a shell variable at the command line:
1. `read first_name`
> **Tip:** Whatever text string you enter after running this command gets stored as the value of the variable `first_name`.
##### List all environment variables:
1. `env`
##### Environment vars: define/extend variable scope to child processes:
1. `export my_planet`
2. `export my_galaxy='Milky Way'`
### Metacharacters
---
##### Comments `#`:
1. `# The shell will not respond to this message`
##### Command separator `;`:
1. `echo 'here are some files and folders'; ls`
##### File name expansion wildcard `*`:
1. `ls *.json`
##### Single character wildcard `?`:
1. `ls file_2021-06-??.json`
### Quoting
---
##### Single quotes `''` - interpret literally:
1. `echo 'My home directory can be accessed by entering: echo $HOME'`
##### Double quotes `""` - interpret literally, but evaluate metacharacters:
1. `echo "My home directory is $HOME"`
##### Backslash `\` - escape metacharacter interpretation:
1. `echo "This dollar sign should render: \$"`
### I/O Redirection
---
##### Redirect output to file and overwrite any existing content:
1. `echo 'Write this text to file x' > x`
##### Append output to file:
1. `echo 'Add this line to file x' >> x`
##### Redirect standard error to file:
1. `bad_command_1 2> error.log`
##### Append standard error to file:
1. `bad_command_2 2>> error.log`
##### Redirect file contents to standard input:
1. `$ tr “[a-z]” “[A-Z]” < a_text_file.txt`
##### The input redirection above is equivalent to:
1. `$cat a_text_file.txt | tr “[a-z]” “[A-Z]”`
### Command Substitution
---
##### Capture output of a command and echo its value:
1. `THE_PRESENT=$(date)`
2. `echo "There is no time like $THE_PRESENT"`
##### Capture output of a command and echo its value:
1. `echo "There is no time like $(date)"`
### Command line arguments
---
1. `./My_Bash_Script.sh arg1 arg2 arg3`
### Batch vs. concurrent modes
---
##### Run commands sequentially:
1. `start=$(date); ./MyBigScript.sh ; end=$(date)`
##### Run commands in parallel:
1. `./ETL_chunk_one_on_these_nodes.sh  & ./ETL_chunk_two_on_those_nodes.sh`
### Scheduling jobs with cron
---
##### Open crontab editor:
1. `crontab -e`
##### Job scheduling syntax:
1. `m  h  dom  mon  dow   command`
> (minute, hour, day of month, month, day of week)

> **Tip:** You can use the `*` wildcard to mean "any".
##### Append the date/time to a file every Sunday at 6:15 pm:
1. `15 18 * * 0 date >> sundays.txt`
##### Run a shell script on the first minute of the first day of each month:
1. `1  0 1 * * ./My_Shell_Script.sh`
##### Back up your home directory every Monday at 3:00 am:
1. `0 3 * * 1  tar -cvf my_backup_path\my_archive.tar.gz $HOME\`
##### Deploy your cron job:
> Close the crontab editor and save the file.
##### List all cron jobs:
1. `crontab -l`
### Conditionals
---
##### `if`-`then`-`else` syntax:
```bash
1 if [[ $# == 2 ]]
2 then
3   echo "number of arguments is equal to 2"
4 else
5   echo "number of arguments is not equal to 2"
6 fi
```
##### 'and' operator `&&`:
1. `if [ condition1 ] && [ condition2 ]`
##### 'or' operator `||`:
1. `if [ condition1 ] || [ condition2 ]`
### Logical operators

| Operator | Definition                  |
| -------- | --------------------------- |
| `==`     | is equal to                 |
| `!=`     | is not equal to             |
| `<`      | is less than                |
| `>`      | is greater than             |
| `<=`     | is less than or equal to    |
| `>=`     | is greater than or equal to |
### Arithmetic calculations
##### Integer arithmetic notation:
1. `$(())`
##### Basic arithmetic operators:

| Symbol | Operation      |
| ------ | -------------- |
| `+`    | addition       |
| `-`    | subtraction    |
| `*`    | multiplication |
| `/`    | division       |
##### Display the result of adding 3 and 2:
1. `echo $((3+2))`
##### Negate a number:
1. `echo $((-1*-2))`
### Arrays
---
##### Declare an array that contains items `1`, `2`, `"three"`, `"four"`, and `5`:
1. `my_array=(1 2 "three" "four" 5)`
##### Add an item to your array:
```bash
1 my_array+="six"
2 my_array+=7
```
##### Declare an array and load it with lines of text from a file:
1. `my_array=($(echo $(cat column.txt)))`
### `for` loops
---
##### Use a `for` loop to iterate over values from 1 to 5:
```bash
1 for i in {0..5}; do
2     echo "this is iteration number $i"
3 done
```
##### Use a `for` loop to print all items in an array:
```bash
1 for item in ${my_array[@]}; do
2   echo $item
3 done
```
##### Use array indexing within a `for` loop, assuming the array has seven elements:
```bash
1 for i in {0..6}; do
2     echo ${my_array[$i]}
3 done
```