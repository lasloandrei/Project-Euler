# Git Tutorial (Basics)

**Table of Contents**

- [About](#about)
- [Install](#install)
- [Getting Started](#getting-started)
  - [Setting up](#set-up)
  - [Starting a Repo](#starting-repo)
	-[GIT Work Flow](#git-work-flow)


## About

Git allows groups of people to work on the same documents (often code) at the same time, and without stepping on each other's toes. It's a distributed version control system.

## Install

```shell
$ sudo apt-get install git
```

## Getting Started

I am going to go through some basic commands using git. If you want to learn by using a terminal prompt and an example, click [here](https://try.github.io/levels/1/challenges/1).

### Setting up

Like most command line tools git comes with a help syestem so if you ever get stuck, you can run:

```shell
$ git help
usage: git [--version] [--help] [-C <path>] [-c name=value]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p|--paginate|--no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           <command> [<args>]

The most commonly used git commands are:
   add        Add file contents to the index
   bisect     Find by binary search the change that introduced a bug
   branch     List, create, or delete branches
   checkout   Checkout a branch or paths to the working tree
   clone      Clone a repository into a new directory
   commit     Record changes to the repository
   diff       Show changes between commits, commit and working tree, etc
   fetch      Download objects and refs from another repository
   grep       Print lines matching a pattern
   init       Create an empty Git repository or reinitialize an existing one
   log        Show commit logs
   merge      Join two or more development histories together
   mv         Move or rename a file, a directory, or a symlink
   pull       Fetch from and integrate with another repository or a local branch
   push       Update remote refs along with associated objects
   rebase     Forward-port local commits to the updated upstream head
   reset      Reset current HEAD to the specified state
   rm         Remove files from the working tree and from the index
   show       Show various types of objects
   status     Show the working tree status
   tag        Create, list, delete or verify a tag object signed with GPG
```

Or if you already know a little bit you can start setting up git by using:

```shell
$ git config --global user.name "Andrei Laslo"

$ git config --global user.email andreil.ltai@yahoo.com

```

### Starting a Repo

So you've installed git and you're ready to work on your first Repository. You're going to need a directory so create one first.

```shell
$ mkdir test
$ cd test
$ git init
Initialized empty Git repository in /Users/Andrei/test/.git/
```
This command is going to create a local Repo for us. It is not up on any server, it's just local. It is actually stored in that .git hidden directory. You'll never going to need to go into that directory, it is just for you to know where it's all stored.

### GIT Work Flow

Let's start working with git. I'm going to talk about the work flow before we get into the commands. We are going to create a readme file, this file starts as Untracked. When we're ready to start tracking that file we're first going to add it to a staging area then we're going to commit the changes, immagine the file up on a stage and commiting is basically like taking a snapshot of those files that we put on the stage. We then might work on out project more, modify the readme and when we're ready, we're going to add the file to the staging area again and commit. Now the commands:

Create the file README.txt

```shell
~/test$ vim README.txt
The program 'vim' can be found in the following packages:
 * vim
 * vim-gnome
 * vim-tiny
 * vim-athena
 * vim-gtk
 * vim-nox
Try: sudo apt-get install <selected package>
```

Edit the file README.txt

```shell
~/test$ gedit README.txt
```

One of the most important commands with git is <b>$ git status</b> command. This is going to tell you what has changed since your last commit.

```shell
/test$ git status
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	README.txt

nothing added to commit but untracked files present (use "git add" to track)
```

Start tracking the file

```shell
/test$ git add README.txt
/test$ git status
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	modified:   README.txt


```

Now we are ready to make our first commit. We do this by running the command below and describe between quotes what this changes do. In this case we have created a README file.

```shell

/test$ git commit -m "Create a README"
[master (root-commit) 626bd12] Create a README
 1 file changed, 1 insertion(+)
 create mode 100644 README.txt

```

To see your commits you use the command below. This command should get you every change that you came up with, the Author and the Date.

```shell

/test$ git log

```

	
