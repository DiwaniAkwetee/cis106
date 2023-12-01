----
Name: Diwani Akwetee
Course: CIS 106
Semester: Fall 2023
----

# Week Report 7

## cat command
**Description:** 
* The cat command is used for displaying the content of a file. 

**Formula:** 
* cat + option + file(s) to display 

**Examples:**
* Display the content of a file located in the pwd
  * `cat todo.lst`
* Display the content of a file located in the pwd
  * `cat ~/Documents/todo.lst`
  

## tac command
**Description:**
* The command is used for displaying the content of a file in reverse order.

**Formula:**
* tac + option + file(s) to display 

**Examples:**
* Display the content of a file located in the pwd
  * `tac todo.md`
* Display the content of file using absolute path 
  * `tac ~/Documents/todo.md`

## head command
**Description:**
* The head command is used to show the top N number of lines of a given file. By default, it prints the first ten lines. If more than one file name is provided then data from each file is preceded by its file name.   

**Formula:**
* head + option + file(s)

**Examples:**
* Display the first 10 lines of a file
  * `head ~/Documents/Books/dracula.txt`
* Display the first 5 lines of a file
  * `head -5 ~/Documents/Books/dracula.txt`

## tail command 
**Description:**
* The tail command displays the last N number of lines of a given file. By default, it prints the last 10 lines. If more than one file name is provided then data from each file is preceded by its file name.  

**Formula:**
* tail + option + file

**Examples:**
* Display the last 10 lines of a file
  * `tail ~/Documents/Book/dracula.txt`
* Display the last 5 lines of a file
  * `tail -5 ~/Documents/Book/dracula.txt`

## cut command
**Description:**
* The cut command is used to extract a specific section of each line of a file and display it to the screen. 

**Formula:**
* cut + option + file(s)

**Examples:**
* Display a list of all the users in your system
  * `cut -d ':' -f1 /etc/passwd`
* Display a list of all the users in your system with their login shell
  * `cut -d ':' -f1,7 /etc/passwd`

## paste command 
**Description:**
* The paste command is used for joining files horizontally in columns. 

**Formula:**
* paste + option + files

**Examples:**
* Merge two files
  * `paste users.lst ip_address.lst`
* Merge two files using a different delimiter
  * `paste -d ":" users1.lst ip_addresses.lst`

## sort command 
**Description:**
* The sort command is used for sorting files. The sort command supports sorting: alphabetically, in reverse order, by number, and by month. 

**Formula:**`

**Examples:**
* Sort a file
  * `sort users.lst`
* Sort a file and save the output to a new file
  * `sort -o sorted.lst users.lst`

## wc command 
**Description:**
* The wc command is used for printing the number of lines, characters and bytes in a file.

**Formula:**
* wc + option + file(s)

**Examples:**
* Display the number of characters in a file
  * `wc -m users.txt`
* Display the number of lines in a file
  * `wc -l users.txt`

## tr command 
**Description:**
* The tr command is used for translating or deleting characters from standard output. 

**Formula:**
* standard output | tr + option + set + set

**Examples:**
* Translate one character to another (For example a period with a comma).
  * `cat file.txt | tr '.' ','`
* Translate white space into tabs.
  * `cat program.py | tr "[:space:]" '/t'`

## diff command 
**Description:**
* The diff command compares files and displays the differences between them. 

**Formula:**
* diff + option + file1 + file2

**Examples:**
* Display the difference between two files
  * `diff cars.csv cars-backup.csv`
* Display the difference between two files in a column format :
  * `diff -y cars.csv cars-backup.csv`

## grep command 
**Description:**
* Grep is used to search text in given file. Grep works line by line basis (it matches the search criteria in a line by line basis).

**Formula:**
* grep + option + search criteria + file(s)

**Examples:**
* Search any line that contains the word "dracula" in the given file: 
  * `grep 'dracula' ~/Documents/dracula.txt`
* Search any line that contains the word 'dracula' regardless of the case
  * `grep -i 'dracula' ~/Documents/Books/dracula.txt` 


## awk command 
**Description:**
* Awk is a scripting language used for processing and displaying text. Awk can work with a text file or from standard output. Awk performs operations line by line.

**Formula:**
* awk + options + {awk command} + file + file to save (optional)

**Examples:**
* Print the first column of every line of a file
  * `awk '{print $1}' ~/Documents/Csv/cars.cvs`
* Print the first field of /etc/passwd file
  * `awk -F: '{print $1}' /etc/passwd`
* Print the last field of the /etc/passwd file 
  * `awk -F: '{print $NF}' /etc/passwd`
* Print the first and last field of the /etc/passwd file
  * `awk -F: '{print $1," = ",$NF}' /etc/passwd`
* Print the first and 4th field  with a different field separator
  * `awk -F: '{OFS="="}{print $1,$4}' /etc/passwd` 

## sed command 
**Description:**
* SED is a stream editor that performs operations on files and standard output. For instance it can search, find and replace, insert, and deletion. 

**Formula:**
* sed options + sed script + file

**Examples:**
* Replacing the number of occurrences of a pattern in a file 
  * `sed 's/pizza/rice/4' shopping-list.lst`
* Replacing all the occurrence of the pattern in a file
  * `sed 's/pizza/rice/g' shopping-list.lst` 
* Replacing from the given number occurrence to the rest occurrences in a file. Start at the second time the word appears and continue to till the end of the file. 
  * `sed 's/pizza/rice/3g' shopping-list.lst`    
* Replacing string on a specific line number 
  * `sed '3 s/pizza/rice/' shopping-list.lst` 
* Replacing string on a range of lines 
  * `sed '1,3 s/pizza/rice/' shopping-list.lst` 

## Standard file descriptors
**Description:**
*  File descriptors are positive integers used for identifying open files in a given session. Each process is allowed 9 file descriptors at a time. Bash reserves the first 3 file descriptors (0-2).

**Formula:**
* Command output + > + file

**Examples:**
* Save the output of a command to file
  * `ls -lA ~ > all-files-in-home.txt`
* Save the error generated by a command to a file
  * `ls -lA downloads/ 2> error-of-ls`

## pipe 
**Description:**
* The pipe allows you to redirect the standard output of a command to the standard input of another.
**Formula:**
* command_1 | command_2 | command_3 | .... | command_N

**Examples:**
* Use grep to look for a string in a particular man page
  * `man ls | grep "human-readable"`
* Display only the 2nd line in a file
  * `head -2 file.lst | tail -1`
  
## alias command 
**Description:**
* An alias is a shorthand for a more complicated command. Alias do not persist unless you save them in your .bashrc or .bash_aliases file
  
**Formula:**
* alias name_of_alias="command here"
  
**Examples:**
* An alias to upgrade a linux (debian system):
  * `alias update="sudo apt update; sudo apt upgrade -y; sudo apt full-upgrade -y"` 
* An alias to clean your system from unneeded packages
  * `alias clean="sudo apt autoremove -y; sudo apt autoclean; sudo apt purge;"` 