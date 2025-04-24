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

###  1. Confused smiley
Write a script that displays a confused smiley `"(Ôo)'`.
```
julien@ubuntu:/tmp/h$ ./1-confused_smiley 
"(Ôo)'
julien@ubuntu:/tmp/h$ 
```
#### Repo:

 - GitHub repository: alx-system_engineering-devops
 - Directory: 0x02-shell_redirections
 - File: 1-confused_smiley

###  2. Let's display a file
Display the content of the `/etc/passwd` file.

Example:
```
$ ./2-hellofile
##
# User Database
#
# Note that this file is consulted directly only when the system is running
# in single-user mode. At other times this information is provided by
# Open Directory.
#
# See the opendirectoryd(8) man page for additional information about
# Open Directory.
##
nobody:*:-2:-2:Unprivileged User:/var/empty:/usr/bin/false
root:*:0:0:System Administrator:/var/root:/bin/sh
daemon:*:1:1:System Services:/var/root:/usr/bin/false
_uucp:*:4:4:Unix to Unix Copy Protocol:/var/spool/uucp:/usr/sbin/uucico
_taskgated:*:13:13:Task Gate Daemon:/var/empty:/usr/bin/false
_networkd:*:24:24:Network Services:/var/networkd:/usr/bin/false
_installassistant:*:25:25:Install Assistant:/var/empty:/usr/bin/false
_lp:*:26:26:Printing Services:/var/spool/cups:/usr/bin/false
_postfix:*:27:27:Postfix Mail Server:/var/spool/postfix:/usr/bin/false
_scsd:*:31:31:Service Configuration Service:/var/empty:/usr/bin/false
_ces:*:32:32:Certificate Enrollment Service:/var/empty:/usr/bin/false
_mcxalr:*:54:54:MCX AppLaunch:/var/empty:/usr/bin/false
_krbfast:*:246:-2:Kerberos FAST Account:/var/empty:/usr/bin/false
$
```
#### Repo:

 - GitHub repository: alx-system_engineering-devops
 - Directory: 0x02-shell_redirections
 - File: 2-hellofile


### 
