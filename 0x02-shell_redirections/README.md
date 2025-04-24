# 0x02. Shell, I/O Redirections and filters

> `DevOps` `Shell` `Bash`

## Resources
### Read or watch:
 - [Shell, I/O Redirection](https://linuxcommand.org/lc3_lts0070.php)
 - [Special Characters](https://mywiki.wooledge.org/BashGuide/SpecialCharacters)

### man or help:
 - echo
 - cat
 - head
 - tail
 - find
 - wc
 - sort
 - uniq
 - grep
 - tr
 - rev
 - cut
 - passwd (5) (i.e man 5 passwd)

## Shell, I/O Redirection
 - What do the commands `head`, `tail`, `find`, `wc`, `sort`, `uniq`, `grep`, `tr` do
 - How to redirect standard output to a file
 - How to get standard input from a file instead of the keyboard
 - How to send the output from one program to the input of another program
 - How to combine commands and filters with redirections

## Special Characters
 - What are special characters
 - Understand what do the white spaces, single quotes, double quotes, backslash, comment, pipe, command separator, tilde and how and when to use them

## Other Man Pages
 - How to display a line of text
 - How to concatenate files and print on the standard output
 - How to reverse a string
 - How to remove sections from each line of files
 - What is the `/etc/passwd` file and what is its format
 - What is the `/etc/shadow` file and what is its format

## Requirements

### General
 - Allowed editors: `vi`, `vim`, `emacs`
 - All your scripts will be tested on Ubuntu 20.04 LTS
 - All your scripts should be exactly two lines long (`$ wc -l` file should print 2)
 - All your files should end with a new line ([why?](https://unix.stackexchange.com/questions/18743/whats-the-point-in-adding-a-new-line-to-the-end-of-a-file/18789))
 - The first line of all your files should be exactly `!/bin/bash`
 - A `README.md` file, at the root of the folder of the project, describing what each script is doing
 - You are not allowed to use backticks, `&&`, `||` or `;`
 - All your files must be executable
 - You are not allowed to use `sed` or `awk`

### More Info
Read your `/etc/passwd` and `/etc/shadow` files.

Note: You do not have to learn about `fmt`, `pr`, `du`, `gzip`, `tar`, `lpr`, `sed` and `awk` yet.


## Tasks

### 0. Hello World
Write a script that prints “Hello, World”, followed by a new line to the standard output.
```
julien@ubuntu:/tmp/h$ ./0-hello_world 
Hello, World
julien@ubuntu:/tmp/h$ ./0-hello_world | cat -e
Hello, World$
julien@ubuntu:/tmp/h$ 
```
#### Repo:

 - GitHub repository: alx-system_engineering-devops
 - Directory: 0x02-shell_redirections
 - File: 0-hello_world

### 
