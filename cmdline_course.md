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
