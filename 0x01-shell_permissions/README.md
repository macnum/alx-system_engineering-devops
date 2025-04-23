# 0x01. Shell, permissions

> `DevOps` `Shell` `Bash`

## Resources
Read or watch:
    - [permissions](https://intranet.alxswe.com/projects/207)

man or help:
    - chmod
    - sudo
    - su
    - chown
    - chgrp
    - id
    - groups
    - whoami
    - adduser
    - useradd
    - addgroup

## Tasks

### 0. My name is Betty
```
Create a script that switches the current user to the user `betty`.
    - You should use exactly 8 characters for your command (+1 character for the new line)
    - You can assume that the user betty will exist when we will run your script
```
#### Repo:

   - GitHub repository: alx-system_engineering-devops
   - Directory: 0x01-shell_permissions
   - File: 0-iam_betty


### 1. Who am I

```
Write a script that prints the effective username of the current user.
```
Repo:

   - GitHub repository: alx-system_engineering-devops
   - Directory: 0x01-shell_permissions
   - File: 1-who_am_i


### 2. Groups
```
Write a script that prints all the groups the current user is part of.

julien@ubuntu:/tmp/h$ ./2-groups
julien adm cdrom sudo dip plugdev lpadmin sambashare
julien@ubuntu:/tmp/h$ 
Note: depending on the user, you will get a different output.
```
Repo:

   - GitHub repository: alx-system_engineering-devops
   - Directory: 0x01-shell_permissions
   - File: 2-groups

### 3. New owner
```
Write a script that changes the owner of the file hello to the user betty.

julien@ubuntu:/tmp/h$ ls -l
total 4
-rwxrw-r-- 1 julien julien 30 Sep 20 14:23 3-new_owner
-rw-rw-r-- 1 julien julien  0 Sep 20 14:18 hello
julien@ubuntu:/tmp/h$ sudo ./3-new_owner 
julien@ubuntu:/tmp/h$ ls -l
total 4
-rwxrw-r-- 1 julien julien 30 Sep 20 14:23 3-new_owner
-rw-rw-r-- 1 betty  julien  0 Sep 20 14:18 hello
julien@ubuntu:/tmp/h$
```
#### Repo:

   - GitHub repository: alx-system_engineering-devops
   - Directory: 0x01-shell_permissions
   - File: 3-new_owner

###  4. Empty!
```
Write a script that creates an empty file called hello.
```
#### Repo:

   - GitHub repository: alx-system_engineering-devops
   - Directory: 0x01-shell_permissions
   - File: 4-empty

###  5. Execute
```
Write a script that adds execute permission to the owner of the file hello.

  - The file hello will be in the working directory
```
```
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:26 5-execute
-rw-rw-r-- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./hello
bash: ./hello: Permission denied
julien@ubuntu:/tmp/h$ ./5-execute 
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:26 5-execute
-rwxrw-r-- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
```
#### Repo:

  - GitHub repository: alx-system_engineering-devops
  - Directory: 0x01-shell_permissions
  - File: 5-execute


###  6. Multiple permissions
```
Write a script that adds execute permission to the owner and the group owner, and read permission to other users, to the file hello.
 - The file hello will be in the working directory
```
```
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 36 Sep 20 14:31 6-multiple_permissions
-r--r----- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./6-multiple_permissions 
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 36 Sep 20 14:31 6-multiple_permissions
-r-xr-xr-- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
```
#### Repo:

  - GitHub repository: alx-system_engineering-devops
  - Directory: 0x01-shell_permissions
  - File: 6-multiple_permissions


### 7. Everybody!
 ```
Write a script that adds execution permission to the owner, the group owner and the other users, to the file hello

  - The file hello will be in the working directory
  - You are not allowed to use commas for this script
```
```
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:35 7-everybody
-rw-r----- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./7-everybody 
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:35 7-everybody
-rwxr-x--x 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
```
#### Repo:

 - GitHub repository: alx-system_engineering-devops
 - Directory: 0x01-shell_permissions
 - File: 7-everybody

### 8. James Bond
```
Write a script that sets the permission to the file hello as follows:

  - Owner: no permission at all
  - Group: no permission at all
  - Other users: all the permissions
The file `hello` will be in the working directory You are not allowed to use commas for this script
```
```
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:40 8-James_Bond
-rwxr-x--x 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./8-James_Bond 
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:40 8-James_Bond
-------rwx 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
```
#### Repo:

 - GitHub repository: alx-system_engineering-devops
 - Directory: 0x01-shell_permissions
 - File: 8-James_Bond

### 9. John Doe
```
Write a script that sets the mode of the file hello to this:
`Write a script that sets the mode of the file hello to this:`
 - The file hello will be in the working directory
 - You are not allowed to use commas for this script
```
#### Repo:

 - GitHub repository: alx-system_engineering-devops
 - Directory: 0x01-shell_permissions
 - File: 9-John_Doe


###  10. Look in the mirror
```
Write a script that sets the mode of the file hello the same as olleh’s mode.

 - The file hello will be in the working directory
 - The file olleh will be in the working directory
```
```
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 42 Sep 20 14:45 10-mirror_permissions
-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello
-rw-rw-r-- 1 julien julien  0 Sep 20 14:43 olleh
julien@ubuntu:/tmp/h$ ./10-mirror_permissions 
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 42 Sep 20 14:45 10-mirror_permissions
-rw-rw-r-- 1 julien julien 23 Sep 20 14:25 hello
-rw-rw-r-- 1 julien julien  0 Sep 20 14:43 olleh
julien@ubuntu:/tmp/h$ 
```
Note: the mode of olleh will not always be 664. Make sure your script works for any mode.
#### Repo:

 - GitHub repository: alx-system_engineering-devops
 - Directory: 0x01-shell_permissions
 - File: 10-mirror_permissions

### 11. Directories
```
Create a script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users.

Regular files should not be changed.
```
```
julien@ubuntu:/tmp/h$ ls -l
total 20
-rwxrwxr-x 1 julien julien   24 Sep 20 14:53 11-directories_permissions
drwx------ 2 julien julien 4096 Sep 20 14:49 dir0
drwx------ 2 julien julien 4096 Sep 20 14:49 dir1
drwx------ 2 julien julien 4096 Sep 20 14:49 dir2
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./11-directories_permissions 
julien@ubuntu:/tmp/h$ ls -l
total 20
-rwxrwxr-x 1 julien julien   24 Sep 20 14:53 11-directories_permissions
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir2
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
```
#### Repo:

 - GitHub repository: alx-system_engineering-devops
 - Directory: 0x01-shell_permissions
 - File: 11-directories_permissions

### 12. More directories
```
Create a script that creates a directory called my_dir with permissions 751 in the working directory.
```
```
julien@ubuntu:/tmp/h$ ls -l
total 20
-rwxrwxr-x 1 julien julien   39 Sep 20 14:59 12-directory_permissions
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir2
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./12-directory_permission s
julien@ubuntu:/tmp/h$ ls -l
total 24
-rwxrwxr-x 1 julien julien   39 Sep 20 14:59 12-directory_permissions
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir2
drwxr-x--x 2 julien julien 4096 Sep 20 14:59 my_dir
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
```
#### Repo:

 - GitHub repository: alx-system_engineering-devops
 - Directory: 0x01-shell_permissions
 - File: 12-directory_permissions

### 13. Change group
Write a script that changes the group owner to school for the file hello

 - The file hello will be in the working directory
```
julien@ubuntu:/tmp/h$ ls -l
total 24
-rwxrwxr-x 1 julien julien   34 Sep 20 15:03 13-change_group
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir2
drwxr-x--x 2 julien julien 4096 Sep 20 14:59 my_dir
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ sudo ./13-change_group 
julien@ubuntu:/tmp/h$ ls -l
total 24
-rwxrwxr-x 1 julien julien      34 Sep 20 15:03 13-change_group
drwx--x--x 2 julien julien    4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien    4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien    4096 Sep 20 14:49 dir2
drwxr-x--x 2 julien julien    4096 Sep 20 14:59 my_dir
-rw-rw-r-- 1 julien school   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
```
#### Repo:

 - GitHub repository: alx-system_engineering-devops
 - Directory: 0x01-shell_permissions
 - File: 13-change_group

### 14. Owner and group
Write a script that changes the owner to `vincent` and the group owner to `staff` for all the files and directories in the working directory.
```
julien@ubuntu:/tmp/h$ ls -l
total 24
-rwxrwxr-x 1 julien julien   36 Sep 20 15:06 100-change_owner_and_group
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir2
drwxr-x--x 2 julien julien 4096 Sep 20 14:59 my_dir
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ sudo ./100-change_owner_and_group 
julien@ubuntu:/tmp/h$ ls -l
total 24
-rwxrwxr-x 1 vincent staff   36 Sep 20 15:06 100-change_owner_and_group
drwx--x--x 2 vincent staff 4096 Sep 20 14:49 dir0
drwx--x--x 2 vincent staff 4096 Sep 20 14:49 dir1
drwx--x--x 2 vincent staff 4096 Sep 20 14:49 dir2
drwxr-x--x 2 vincent staff 4096 Sep 20 14:59 my_dir
-rw-rw-r-- 1 vincent staff   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 
```
### Repo:

 - GitHub repository: alx-system_engineering-devops
 - Directory: 0x01-shell_permissions
 - File: 100-change_owner_and_group

### 
