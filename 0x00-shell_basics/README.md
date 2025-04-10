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

## 
