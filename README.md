# Git Tutorial (Basics)

**Table of Contents**

- [About](#about)
- [Install](#install)
- [Getting Started](#getting-started)
  - [Setting up](#set-up)
  - [Starting a Repo](#starting-repo)



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
$ mkdir store
$ cd store
$ git init
Initialized empty Git repository in /Users/Andrei/store/.git/
```
This command is going to create a local Repo for us. It is not up on any server, it's just local. It is actually stored in that .git hidden directory. You'll never going to need to go into that directory, it is just for you to know where it's all stored.


	
