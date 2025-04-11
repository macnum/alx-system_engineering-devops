# 0x00. Shell, basics

> `DevOps` `Shell` `Bash`

![RTFM](https://s3.amazonaws.com/intranet-projects-files/holbertonschool-sysadmin_devops/205/image.jpg)

## 0. Where am I?

Write a script that prints the absolute path name of the current working directory.

Example:

```$ ./0-current_working_directory
/root/alx-system_engineering-devops/0x00-shell_basics
$
```

## 1. What’s in there?

Display the contents list of your current directory.

Example:
    ```
    $ ./1-listit
    Applications    Documents   Dropbox Movies Pictures
    Desktop Downloads   Library Music Public
    $ 
    ```
##  2. There is no place like home
Write a script that changes the working directory to the user’s home directory.
    - You are not allowed to use any shell variables
    ```
    julien@ubuntu:/tmp$ pwd
    /tmp
    julien@ubuntu:/tmp$ echo $HOME
    /home/julien
    julien@ubuntu:/tmp$ source ./2-bring_me_home
    julien@ubuntu:~$ pwd
    /home/julien
    julien@ubuntu:~$ 
    ```

##  3. The long format

    Display current directory contents in a long format

    Example:

```
    $ ./3-listfiles
    total 32
    -rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory
    -rwxr-xr-x@ 1 sylvain staff 19 Jan 25 00:23 1-listit
    -rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:29 2-bring_me_home
    -rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:39 3-listfiles
    $
```

##  4. Hidden files
Display current directory contents, including hidden files (starting with `.`). Use the long format.

Example:
```
$ ./4-listmorefiles
total 32
drwxr-xr-x@ 6 sylvain staff 204 Jan 25 00:29 .
drwxr-xr-x@ 43 sylvain staff 1462 Jan 25 00:19 ..
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 sylvain staff 19 Jan 25 00:23 1-listit
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:39 3-listfiles
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:41 4-listmorefiles
$
```

##  5. I love numbers

Display current directory contents.

 - Long format
 - with user and group IDs displayed numerically
 - And hidden files (starting with .)
 Example:
```
$ ./5-listfilesdigitonly
total 32
drwxr-xr-x@ 6 501 20 204 Jan 25 00:29 .
drwxr-xr-x@ 43 501 20 1462 Jan 25 00:19 ..
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:23 1-listfiles
-rwxr-xr-x@ 1 501 20 19 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 501 20 20 Jan 25 00:39 3-listfiles
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:41 4-listmorefiles
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:43 5-listfilesdigitonly
$
```

##  6. Welcome
    Create a script that creates a directory named `my_first_directory` in the `/tmp/` directory.

Example:
```
$ ./6-firstdirectory
$ file /tmp/my_first_directory/
/tmp/my_first_directory/: directory
$
```

## 7. Betty in my first directory
Move the file `betty` from `/tmp/` to `/tmp/my_first_directory`.

Example:
```
$ ./7-movethatfile
$ ls /tmp/my_first_directory/
betty
$
```

## 8. Bye bye Betty
Delete the file `betty`.

The file `betty` is in `/tmp/my_first_directory`
Example:
```
$ ./8-firstdelete
$ ls /tmp/my_first_directory/
$
```

## 9. Bye bye My first directory

Delete the directory `my_first_directory` that is in the `/tmp` directory.

Example:
```
$ ./9-firstdirdeletion
$ file /tmp/my_first_directory
/tmp/my_first_directory: cannot open `/tmp/my_first_directory' (No such file or directory)
$
```

##  10. Back to the future
Write a script that changes the working directory to the previous one.
```
julien@ubuntu:/tmp$ pwd
/tmp
julien@ubuntu:/tmp$ cd /var
julien@ubuntu:/var$ pwd
/var
julien@ubuntu:/var$ source ./10-back
/tmp
julien@ubuntu:/tmp$ pwd
/tmp
```

##  11. Lists

Write a script that lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the `/boot` directory (in this order), in long format.

```

Repo:

    - GitHub repository: alx-system_engineering-devops
    - Directory: 0x00-shell_basics
    - File: 11-lists

```

##  12. File type

Write a script that prints the type of the file named `iamafile`. The file `iamafile` will be in the `/tmp` directory when we will run your script.

Example
```
ubuntu@ip-172-31-63-244:~$ ./12-file_type
/tmp/iamafile: ELF 64-bit LSB  executable, x86-64, version 1 (SYSV), dynamically linked (uses shared libs), for GNU/Linux 2.6.24, BuildID[sha1]=bd39c07194a778ccc066fc963ca152bdfaa3f971, stripped
```

Note that depending on the file, the output of your script will be different.

## 13. We are symbols, and inhabit symbols

Create a symbolic link to `/bin/ls`, named `__ls__`. The symbolic link should be created in the current working directory.
```
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 144
drwxrwxr-x  2 ubuntu ubuntu   4096 Sep 20 03:24 .
drwxrwxrwt 12 root   root   139264 Sep 20 03:24 ..
ubuntu@ip-172-31-63-244:/tmp/sym$./13-symbolic_link
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 144
drwxrwxr-x  2 ubuntu ubuntu   4096 Sep 20 03:24 .
drwxrwxrwt 12 root   root   139264 Sep 20 03:24 ..
lrwxrwxrwx  1 ubuntu ubuntu      7 Sep 20 03:24 __ls__ -> /bin/ls
```
## 
