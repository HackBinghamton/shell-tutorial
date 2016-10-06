# The Terminal and Shell
This guide covers the basics of using a computer from the
terminal. You will learn how to navigate folders, and how to make,
delete, copy, and move files and folders.

People often confuse the terminal and the shell, since the difference
is subtle. A *terminal* is an environment to input and display
text, and a *shell* is the program that interprets your input in a
terminal.

## Why Use The Terminal?
While graphical user interfaces (GUIs) are helpful for a lot of things,
sometimes command line interfaces (CLIs) are the better tool for the job.

As an example, imagine you have a messy folder, and you want to combine
all the .txt files into a new file called "newfile.txt". If you use a
GUI, this seems like a tedious task, but it only takes one line in the
*shell*.

    cat *.txt > newfile.txt


## Where Is The Terminal?

### Mac OS
1. Open Finder from the Dock.
2. Open your Applications folder.
3. Open Utilities.
4. Double click on Terminal.

### Ubuntu
Hit the keyboard shortcut Ctrl - Alt - T.

### Windows
Windows also has a built-in terminal, Command Prompt; however, Command
Prompt's shell differs greatly from the shells on Mac and Linux. So you will
need to install a shell

In the next workshop, we will be learning the basics of git. Since Git
for Windows comes with a version of Bash (the shell on Mac and Linux),
we recommend that you install it.
You can get it [here.](https://git-for-windows.github.io/)

## Folder Structure
Folders (often called *directories*) on your computer are arranged in a
tree structure. A folder within another folder is called a *subdirectory*.
The folder containing these subdirectories is called the *parent* of the
subdirectories.
There is a folder called the *root* directory ("/" on Mac/Linux, and "C:"
on Windows) that contains all of the computer's files and folders within
its subdirectories. You often see these directories arranged like this:

![Directory Tree](tree.png)

In this picture, you can see from the navigation bar that these folders are in
is the root ('/').
It is easy to see which folders are parents, which are subdirectories, and
which folders are in the same directory. When you open a terminal, you can
find the same information, but you need to know some commands.

## Navigating Directories

In the last picture, we were in '/' (the root directory). We call your currently
open folder the *working directory*. In a GUI, you can see the working directory
in the navigation bar; in a terminal you find it with the command `pwd`. This command
is an abbreviation for "Print Working Directory". Open a terminal, type `pwd` and
press Enter. You should see the path to your home directory:

![Print Working Directory](pwd.png)

Note that on Windows your home directory path is usually 'C:\Users\USERNAME',
but in Bash it will look like 'c/Users/USERNAME' because on Mac/Linux, folders
are seperated with a forward slash instead of a backslash.

## Viewing Directory Contents

To view what's inside a directory, type `ls mydirectory`.
If you just want to see what's inside your working directory, just type `ls`.

## Copying Files

Creating a copy of a file can be done with the `cp` command.
To make a copy of myfile.txt, enter `cp myfile.txt myfile-copy.txt`.
You can also use `cp` to copy files into a folder.
For example, to copy files into an already created folder, you can type
`cp myfile.txt myfile-copy.txt myfolder`.
Notice that you can type multiple file names, and they'll all be moved into
the last thing (myfolder in this instance).

## Making and Removing Folders

### Making
The previous section assumed you had a folder already created, but what if you
wanted to make it from terminal?
The `mkdir` command stands for MaKe DIRectory, and all you have to do is type
`mkdir myfolder` to create a folder in your working directory.

### Removing
To delete folders, use `rmdir` which stands for ReMove DIRectory.
If you want to remove myfolder, just type `rmdir myfolder`.
This command won't work if there's files or folders inside of myfolder though,
so make sure you have nothing inside myfolder.

## Moving & Renaming Files

### Moving
We might also want to be able to move folders and files to other places instead of
only making copies.
The `mv` command (MoVe) lets you do that, and it works just like `cp`.
To move myfile.txt into myfolder, type `mv myfile.txt myfolder/`.
Notice the `/` after myfolder, it's there because myfolder is a
directory and not a normal file.
Putting a `/` after directory names is a good idea because the shell will refuse
to move something into a nonexistent directory.
The `/` at the end forces your shell to look for a directory with that name.

### Renaming

You can also use `mv` to give files new names.
To rename myfile.txt to otherfile.txt, type `mv myfile.txt otherfile.txt`.
There's no `/` on the end because we aren't moving myfile.txt into a directory,
we're just giving it a new name.
Be careful using `mv`, it will overwrite the otherfile.txt even if it exists.

## Advanced Shell Topics

As you get more and more familiar with the terminal, you'll find that certain
tasks are far less manual than in a normal file explorer.
There's an inconceivable amount of command combinations you can use
in the shell, so understanding the fundamentals of basic commands will help
you understand command combinations, and even craft your own.

One of the quickest ways to learn about commands is to read the manual pages.
You can quickly get to the manual page of a command by typing `man command`
in terminal.
Manual pages are also available on [the internet](https://linux.die.net).
