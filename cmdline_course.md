---
layout: default
---

## Command line course

This course was an important introduction to UNIX and different command line tools.

### Module 1: Command line basics and UNIX

#### Operating systems

This module was about the basics of command line and UNIX. UNIX is an operating system, but it is also often used as an umbrella term for UNIX-like operating systems such as Linux. Linux is also an operating system, newer that UNIX, and it is open-source option. 

#### Basic commands

When using Bash, you always have to think about directories and files. Root is the highest directory that includes subdirectories like home directory and subdirectories that include things that the operation system needs and which are available to all users if there are more than one.

Directories and files in user's home directory can be listed, read, copied, etc using Bash. In the following table, the commands I mostly used during this course are listed:

|Command        |Use                      |
|---------------|-------------------------|
|ls             |List contents            |
|---------------|-------------------------|
|cd             |Change directory         |
|---------------|-------------------------|
|mkdir          |Create directory         |
|---------------|-------------------------|
|nano           |Opens file in text editor|
|---------------|-------------------------|

#### My thoughts

I think I am starting to grasp the ideas and history of different operating systems, but I definitely focused more on understanding and remembering the basic commands. 

### Module 2: Text Processing in UNIX

#### Character encodings

This module started with an introduction to character encodings. The three main ones we focused on were ASCII, Latin-1 and UTF-8.

ASCII is an encoding system where all of the 128 characters it is able to express are encoded with using only 7 bits. These characters include upper and lower case letters from A to Z, numbers from 0 to 9, punctuation marks, space, tabs, some characters only readable to the computer, etc. This, however, is not sufficient for every language in the world. 

Other encoding systems have been invented to combat this problem, largest of them Unicode that is made to cover every possible character with its 1,114,112 code points. Still, it took long time to develop Unicode and sometimes it might seem a bit excessive. Latin-1 is one of the encodings that utilises the one bit that ASCII leaves unused from a whole byte to represent more characters. UTF-8 is one optimization for Unicode, where as many bytes as needed are used and then highest bits in a byte are used to represent how many bytes the character consists of.

#### Regular Expressions

Regular expressions or RegEx can be used to find specific strings from text files. `grep` is a command that allows us to find lines containing the specified string. You can add different modifiers to do more specific tasks.

`sed` is another command that uses regular expressions. Based on a given RegEx pattern, it finds the occurences of the pattern and changes those occurences as specified with modifiers.

#### My thoughts

I have used regular expressions before but learning to use them in Bash also seems useful. I prefer using Python's RegEx package just because I am more used to Python, but in the long run, I would assume using `grep`and `sed`can be useful and easier than using Python if I just need to process text. 

## Module 3

#### Scripts

If we want to sort of automate series of processes executed in Bash, we can use scripts. Scripts are text files that contain these series of commands we want to create for tasks we often do.

In scripts, we can also use if statements and for loops and while loops.

#### Permissions

When executing scripts, execute permission is needed. You typically can have three types of permissions: read, write and execute, and they can be different for every user. These permissions can be modified with `chmod`command for files and directories.

The reading materials mention the root user, which has access to the highest level of permissions. It can access subdirectories of root other than the home directory, where normal users have accesses to their own home directories. Using the root user can be risky because there is often no reason to change the things only the root user has access to, so it is better to stay logged on as a normal user and then use `sudo`command to execute commands that need permissions only the root user has.

#### My thoughts

I have actually used this knowledge about permissions without really understanding it, and it is interesting to learn why Linux as an operating system works this way. 

The scripts remind me of text processing I have done with Python, and using pip and virtual environments was familiar to me, eventhough I prefer to use VSCode when I need to code.
 
## Module 4

#### Remote servers

Remote servers are computers that are accessed through some network and do not need to be physically located in the same place as the user. At least in our case with CSC's Puhti, Puhti can be accessed with SSH using `ssh` command. This works with some kind of personal and public key that allow safe authentication.

To copy files from the remote server, we can use ´scp´command.

#### Git

Git is a version control tool that is widely used to track progress in processes. It creates snapshots of the files and then logs the changes that have been made between the snapshots. With Git, it is possible to create new branches where you can work and not change the main code. Mergin these branches is possible and it is often done when some functionality is tested to be functioning correctly.

GitHub is often used with Git to publish these logs. Having a repository for your project in GitHub makes it possible to share your code and collaborate with others. Users can copy the GitHub repository to their own local directory and then work there and submit their modifications, that can be in different branches, back to the repositorys owner to be added to the master branch.

To update GitHub, following commands are used:

|Command         |Good to remember                                 |
|----------------|-------------------------------------------------|
|`git add`       |Adding everything in repo --all                  |
|----------------|-------------------------------------------------|
|`git commit -m` |Informative message!                             |
|----------------|-------------------------------------------------|
|`git push`      |Check that right branch is used with `git status`| 

#### My thoughts

I think Git and GitHub can be amazing tools to keep track of different projects. Without Git, I have had trouble in remembering, what changes I have made to my projects when I have had to go back to earlier steps, but Git takes care of thet for me if I just remember to do commits often enough and add informative messages. 
