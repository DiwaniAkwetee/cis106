---
Name: Diwani Akwetee
Course: CIS 106
Semester: Fall 2023
----

# Week Report 8

## What is VIM?
A command line text editor that is included in all POSIX complaint operating systems. It is an improved version of the vi command. It also has multiple modes.

## What is nano? 
A command line text editor that allows you to edit files easily. 

## How to use VIM

### Start and quit vim
* First type `vim` in the terminal to open VIM.
* Then press the esc key and type `:qa!`
### What are the different vim modes:
* Normal mode: used for manipulating test 
* Insert mode: used for writing text
* Command mode: used for entering vim commands
* Visual mode: used for navigation and manipulation of text selections
* Select mode: similar to visual mode
* Ex mode: similar to the command line mode but optimized for batch processing
  
### Insert text in vim
You insert text in vim by just simply typing. You can use the arrow keys to move around, enter key to continue in the next line, and backspace for deleting. 

### Save a file in vim
* Enter esc key and then type `:w`
* To save a file with its name you would type `:w + name of file`
* To save the file and quit you would type `:wq`
* To save the file and close all you would type `:wqa!`
   
### Search for a word inside vim
* Make sure you are in normal mode
* Type `/` then the word behind the /
  * Example: `/hello`  

### Delete text in vim
`dw`= delete current word
`u`= undo
`dd`= delete line under the cursor
`d + /word`= delete until the given 
