# Module 5 Linux essentials

### Task2.

1. Analyze the structure of the /etc/passwd and /etc/group file, what fields are
present in it, what users exist on the system? Specify several pseudo-users, how
to define them?

- structure of **/etc/passwd** :</br>
1) username </br>
2) password (encrypted form is stored in /etc/shadow file) </br>
3) user ID (UID) </br>
4) group ID (GID) </br>
5) GECOS (personal information / user description)</br>
6) user's home directory</br>
7) and which shell does that user use </br>

- structure of **/etc/shadow** :</br>
1) group name </br>
2) encrypted password of that group </br>
3) group ID (GIP) </br>
4) list of users that belong to this group</br></br>
Pseudo-users are to show  processes' ownership. Some pseudo-users :</br>
a) daemon - used by system service processes</br>
b) bin - gives ownership of executables command</br>
c) adm - owns registration files</br>
d) nobody - used by many services</br>
e) sshd - used by the secure shell server</br>
f) myscq - owns all resources concerning databases</br></br>
Usually UIDs less than 10 are defined as system accounts.</br>
10 - 100 UIDs -> pseudo-users concerning to particular components of software


2. What are the uid ranges? What is UID? How to define it?</br></br>
'UID' is numeric designation (ID) for an individual user (total number is not more than 65 535).</br>
These IDs are reserved for special use. UID can be found out in /etc/passwd file or by executing command **"id"** of a current or any other user. Also using environment variable **"echo $UID"** UID can be shown.</br></br>
When you need to define only just number of id of a user (without name) -> use command **"id -u username"**
![1](./screenshots/2.png)</br></br>
Here are the ranges of UIDs:
- 0 -> root
- 1-999 -> daemons, pseudo-users, system and reserved users
- 1000+ -> regular users

3. What is GID? How to define it?</br></br>
GID - unique identifier of the group within the system to which the user belongs. GID can be defined via command **"id -g username"** of a current or any other user.

4. How to determine belonging of user to the specific group?</br></br>
It can be done by using next command lines :</br>
 **"groups username"**</br>
 **"id -Gn username"**

5. What are the commands for adding a user to the system? What are the basic
parameters required to create a user?

- structure: **"useradd option username"**</br></br>
  Basic options :</br>
 -p  - assign password</br>
 -g  - GID or name of the group to which the user belongs</br>
 -G  - write additional groups (separated via coma)</br>
 -s  - shell for the command interpreter for the given user</br>
 -e  - set a time till user will be disconnected automatically</br>
 -o  - allows repeating the same user ID</br>
 -m  - create user's home directory</br>


6. How do I change the name (account name) of an existing user?</br></br>**"usermod -l new_username old_username"**


7. What is skell_dir? What is its structure?</br></br>
This is a default template of files/directories that will be automatically created in a home directory of each newly created user. File location : /etc/skel. This folder can be modified. </br>
![1](./screenshots/7.png)</br></br>


8. How to remove a user from the system (including his mailbox)?</br></br>
 **"sudo userdel -r user_name"** OR **"sudo userdel -l user_name"**</br>
 to remove user's home directory and mail spool


9. What commands and keys should be used to lock and unlock a user account?</br></br>
 To lock :</br>
 a) passwd -l user_name</br>
 b) usermod -L user_name</br></br>
 To unlock : </br>
 a) passwd -u user_name</br>
 b) usermod -U user_name

10. How to remove a user's password and provide him with a password-free login for subsequent password change?</br></br>
To remove password of a user: **"sudo passwd -d username"**</br>
After that no password is asked during su command to that user.

11. Display the extended format of information about the directory, tell about the information columns displayed on the terminal.
12. What access rights exist and for whom (i. e., describe the main roles)?
Briefly describe the acronym for access rights.</br></br>
![1](./screenshots/11.png)</br></br>
First column structure: **"- rwx rwx rwx"**</br></br>
. first item stands for the file type : regular(**-**)/directory(**d**)/block device(**b**)/symbolic link(**s**)/pipe(**p**)/socket(**s**)/character device(**c**)</br>
 . next 3 items are related to User/owner (**u**) rights</br>
 . 2nd group of 3 items are related to Group (**g**) rights</br>
 . 3rd group of 3 items are related to Others (**o**) rights</br></br>
 where:</br>
  . **r** stands for "**read**"</br>
  . **w** stands for "**write**"</br>
  . **x** stands for "**execute**"</br></br>
  . **2nd column**: number of links to that file within the file system </br>
  . **3rd column**: owner of the file </br>
  . **4th column**: group of users that to which that file is related </br>
  . **5th column**: size of file </br>
  . **6th column**: date and time of file creation </br>
  . **7th column**: file name </br>

13. What is the sequence of defining the relationship between the file and the user?</br></br>
When any user sets up the process with file then :</br>
 . if UID of the file is the same as the UID of the process - means that user is the owner of the file;</br>
 . if the GID of the file matches the GID of any group the user belongs to - means he is a member of the group to which the file belongs;</br>
 . if neither the UID no the GID of a file matches with the UID of the process and the list of groups that the user running it belongs to, that user is an outsider.


14. What commands are used to change the owner of a file (directory), as well
as the mode of access to the file? Give examples, demonstrate on the terminal.</br>
- to assign new user : **"chown new_owner file/directory"**
![1](./screenshots/14.1.png)</br></br>
- assign different permissions : **"chmod option file/directory"**
![1](./screenshots/14.2.png)</br></br>


15. What is an example of octal representation of access rights? Describe the
umask command.</br></br>**"umask"** - is a user mask, this is the default range of permissions that will be assigned to file/directory during it creation. It is defined in 2 files (/etc/.bashrc or /etc/.profile).</br></br>
Basic permissions within Linux OSs for:</br>
. directory : 0777 (rwxrwxrwx)</br>
. file : 0666 (rw-rw-rw)</br></br>
Umask (default):</br>
. user : 0002 (with such umask default permissions **for directory**: 775; **for file**: 664)</br>
. root : 0022 (with such umask default permissions **for directory**: 755; **for file**: 644)

16. Give definitions of sticky bits and mechanism of identifier substitution. Give
an example of files and directories with these attributes.</br></br>**Sticky-bit** - as per my understanding if this bit is added to the file/directory - it means that other users which operate in this shared folder (in coop) can create/read/execute but cannot delete these files (which are assigned with sticky bits).</br></br>
Example of folder with sticky bit within ubuntu :</br>
![1](./screenshots/16.png)</br></br>
Example of files with sticky bit within /tmp folder : </br>
![1](./screenshots/16.2.png)</br></br>
Example of locally created files with sticky bit: </br>
![1](./screenshots/16.1.png)</br></br>


17. What file attributes should be present in the command script?</br></br>
For the script - file should have: </br>
 . execute(x) permission for owner, group and others</br>
 . file extension .sh </br>
 . inside the script the 1st line should be **#!/bin/bash** in order to boot shell bash
