---
layout: default
title: Introduction to Command Line
permalink: /outline/command-line-introduction/
parent: Outline
nav_order: 2
---

# Introduction to Using the Command Line
## What is the Command Line or Shell?

The shell (sometimes referred to as the “Unix shell”, for the operating system where it was first developed) is a program that allows you to interact with your computer using typed text commands. It is the primary interface used on Linux and Unix-based systems, such as macOS, and can be installed optionally on other operating systems such as Windows.

It is the definitive example of a “command line interface”, where instructions are given to the computer by typing in commands, and the computer responds by performing a task or generating an output. With only a few keystrokes, the shell allows you to combine existing tools into powerful pipelines and to handle large volumes of data automatically.

## Opening the shell

Let’s start by opening the shell. This likely results in seeing a black or white window with a cursor flashing next to a dollar sign. This is our command line, and the $ is the command prompt to show that the system is ready for our input.

## Navigating the File System

When working in the shell, you are always somewhere in the computer’s file system, in some folder (directory). We will therefore start by finding out where we are by using the pwd command, which you can use whenever you are unsure about where you are. It stands for “print working directory” and the result of the command is printed to your standard output, which is the screen.

Let’s type pwd and press enter to execute the command:

Input{: .label .label-green}
~~~
pwd
~~~

Output{: .label .label-yellow}
~~~ 
/Users/riley
~~~

The output will be a path to your home directory. Let’s check if we recognise it by looking at the contents of the directory. To do that, we use the ls command. This stands for “list” and the result is a print out of all the contents in the directory:

Input{: .label .label-green}
~~~
ls
~~~

Output{: .label .label-yellow}
~~~ 
Applications Documents    Library      Music        Public
Desktop      Downloads    Movies       Pictures
~~~

If we want more information, we type ls -l and press enter, the computer returns a list of files that contains information similar to what we would find in our Finder (Mac) or Explorer (Windows): the size of the files in bytes, the date it was created or last modified, and the file name.

The -l  is an example of a flag (also known as option, parameter, or, most frequently, argument) to go with our basic commands. Arguments modify the workings of the command by telling the computer what sort of output or manipulation we want.

Input{: .label .label-green}
~~~
ls -l
~~~

Output{: .label .label-yellow}
~~~ 
total 0
drwx------+  6 riley  staff   204 Jul 16 11:50 Desktop
drwx------+  3 riley  staff   102 Jul 16 11:30 Documents
drwx------+  3 riley  staff   102 Jul 16 11:30 Downloads
drwx------@ 46 riley  staff  1564 Jul 16 11:38 Library
drwx------+  3 riley  staff   102 Jul 16 11:30 Movies
drwx------+  3 riley  staff   102 Jul 16 11:30 Music
drwx------+  3 riley  staff   102 Jul 16 11:30 Pictures
drwxr-xr-x+  5 riley  staff   170 Jul 16 11:30 Public
~~~

We’ve now spent a great deal of time in our home directory. Let’s go somewhere else. We can do that through the cd or Change Directory command:

Input{: .label .label-green}
~~~
cd Desktop
~~~

Input{: .label .label-green}
~~~
pwd
~~~

Output{: .label .label-yellow}
~~~ 
/Users/riley/Desktop
~~~

## Creating Directories

Now, we will create a new directory and move into it:


Input{: .label .label-green}
~~~
mkdir firstdir
cd firstdir
~~~

Here we used the mkdir command (meaning ‘make directories’) to create a directory named ‘firstdir’. Then we moved into that directory using the cd command.

But wait! There’s a trick to make things a bit quicker. Let’s go up one directory using two periods.

Input
{: .label .label-green}
~~~
cd ..
~~~

To move to a specific directory, you don't have to type the full name. Instead of typing cd firstdir, let’s try to type cd f and then press the Tab key. We notice that the shell completes the line to cd firstdir/.
