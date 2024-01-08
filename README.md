# Git

## SEIR 0911EC

![Git](https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png)

## Overview
In this lesson, we'll learn about distributed version control using Git.

## Objectives
- Understand what Git is and why we need it
- Use Git to save our code

## What is Git?

![XKCD - Git, How do we use it?](https://imgs.xkcd.com/comics/git.png)

Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency. Git is easy to learn and has a tiny footprint with lightning fast performance.

Git keeps track of all your code and saves your code **locally**. *GitHub* is a service where you save your code **online**. We'll cover that later. 

Each time you save to Git, you save a version of your code. It's kind of like a video game where you can save as many times as you want. Git stores a safe version of your code that you can come back to in case something goes wrong.


# GitHub

![GitHub](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwww.thesoftwarereport.com%2Fwp-content%2Fuploads%2F2019%2F06%2Fgithub2.jpeg&f=1&nofb=1)

## Lesson Overview
In this lesson, we'll learn about the vital role GitHub plays in the web development world.

## Objectives
  - Understand what GitHub is and why we need it
  - Use GitHub to save your code

## Lesson Instructions

### What is GitHub?

GitHub is a code hosting platform for version control and collaboration. 

It lets you and others work together on projects from anywhere.

GitHub is where you upload your code.

GitHub is where others can see and download your code.

### What is a GitHub repository?

Pronounced *re·pos·i·to·ry*, but called *repo* for short.

It’s the place where your code is stored.

![Branching](https://thumbs.gfycat.com/DarkWellmadeCony-size_restricted.gif)

### Branching

Branching is a way to work on different versions of a repository at the same time.

Anything in the "main" branch is always *deployable*.

### Pull Requests

A *pull request* is a way in GitHub to say you’re proposing a change to a repo.

The change you’re proposing is visible to all developers working on that repo.

**[Further Reading](https://help.github.com/articles/about-pull-requests)**

![Cloning](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fmedia.giphy.com%2Fmedia%2FpMbrcAbQWjlyE%2Fgiphy.gif&f=1&nofb=1)

### Cloning

When you create a repository on GitHub, it exists as a *remote* repository. 

You can clone a repository to create a *local* copy on your computer and sync between the two locations.

**[Further Reading](https://help.github.com/articles/cloning-a-repository)**

![Forking](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fmedia.giphy.com%2Fmedia%2FLD1BmDQiDh2o0%2Fgiphy.gif&f=1&nofb=1)

### Forking

Creating a “fork” is producing a personal copy of someone else’s project.

**[Further Reading](https://help.github.com/articles/fork-a-repo)**

### GitHub Flow

GitHub Flow is a workflow you use to collaborate with other developers on a GitHub project.

**[Further Reading](https://guides.github.com/introduction/flow)**


## Why is Git important?

Git handles versioning our code. In simple terms, if we make a mistake, we can always revert back to the old codebase. 

Git makes it easy to share your code with other developers.

Git is a version control system (VCS), more specifically, a distributed version control system (DVCS)

## The Git Lifecycle

To understand how Git works, we need to talk about the lifecycle of a Git-tracked file.

### Staging and Commiting

There are 3 states that your file can reside in `modified`, 
`staged`, and `committed`. These states map to the different sections of a Git project.

A) `modified` means that you have changed the file in your working directory, but that's it (ie you have not committed it to
your repository yet).

B) `staged` means that you have marked a modified file in its current version
to go into your next commit snapshot. Use `git add <file name>` to `stage` files.

C) `committed` means that the data is safely stored in your local repository. Use `git commit -m 'Your message here'`.


When we add a file we are moving it from the working directory to the staging area. Commiting it means we've moved it from our staging area to our local repository.

Below is an example of the commit history of the GA instructor team's work building and editing our constantly evolving curriculum. Notice how the commit messages are all short and to the point of what the individual's task was with each. 

<img src="./assets/commit-history.png">

This screenshot shows 8 commit messages made by 4 different people on one day. The full curriculum update has over 400 commits by more than 20 people over the past months!



### Lets create a new Repository on Github. We can call it "Practice-Repo".

Make sure to Initialize it with a ReadMe, which will allow us to Clone it down in a few steps. For this lesson, it may not matter, but make sure to keep track of whether or not you are making your Repositories Private or Public, depending on what you want to do with them.

Once you create your repo, lets clone it down

First, find out where we are, change directories to make sure we're in the right place, then see what else is in our folder

pwd - Print Working Directory

cd ______ - change into a child directory

ls - list folders and files inside of a directory


```
git clone <url>
```

will copy our new git repo into our local machine.

Now we need to make some kind of edit to our readme file. Lets open up this file in our Code Editor and change up some text in it. We can say "Hello World" or something simple like that, as long as we make some kind of change. 

###  there are 3 main stages of a Git-tracked file after the repository has been initialized:

1. **Add to Staging** — Once the files in your working directory are being tracked by Git, you can now add any changes to the staging area with the `git add` command.


```
git add .

```

The "." in "git add ." will add **all** of the files in the directory that we are currently working with. We are also able to add one file at a time, or multiples, by simply writing the file names out when we add.

```
git add index.html
```

``` 
git add index.html style.css
```

you can even add from nested, child directories

```
git add index.html js/script.js css/styles.css 
```
You can probably see how *not* adding every single file at once would be beneficial if you are working with a large team on a number of different tasks.

How you wish to add your files up for the Commit stage is up to you, and something that you will build up more familiarity and comfort with as you continue working with Git and with your code


2. **Commit to Local Repo** - Once you're all set adding files to staging, you can commit them to your local repository with the `git commit` command. This command will commit ALL files that have been staged.

>Note: Whenever you do `git commit` you MUST add a brief message describing the commit with `-m "message text"`. So a full git commit command should look something like this:

```bash
git commit -m "Created login form frontend"
```


Once you’ve completed the steps to link the local git repository with the GitHub repository, you can push your code using the following commands:
"Initial commit" is a good place to start!
```
git add .
git commit -m 'initial commit'
```

As you work on larger and larger projects, you will see your Commit history grow. This is a great way to track who on your team has made changes to what parts of which files, and when they were made. It can be especially useful when there is a conflict or bug in the code, so  we can see where exactly the error has been made, and fix it easily

### Now we need to sync our local repository to our Remote/Github.



3. Use `git push` to push your commits from your local branch to your remote repository.

The `git push` command takes two arguments:
- A remote name, for example, **origin**
- A branch name, for example, **main**


``` 
git push origin main

``` 

will be the command used 90% of the time in this class. The only real changes will be when we are on different branches in some future hw's, and in our P3


## More Git Commands

#### Git Pull

```bash
git pull origin main
```

The git pull command is used to fetch and download content from your connected remote repository and immediately update your local repository to match that content.


#### Git Status
```bash
git status
```

The `git status` command displays the state of the present working directory and the staging area. It lets you see which changes have been staged, which haven’t, and which files aren’t being tracked by Git. Status output does not show you any information regarding the committed project history. For this, you need to use `git log`.


#### Git Log
```bash
git log
```

After you have created several commits, or if you have cloned a repository with an existing commit history, you’ll probably want to look back to see what has happened. The most basic and powerful tool to do this is the `git log` command.



When you run git log in this project, you should get output that looks something like this:
```bash
$ git log
commit ca82a6dff817ec66f44342007202690a93763949
Author: Scott Chacon <schacon@gee-mail.com>
Date:   Mon Mar 17 21:52:11 2008 -0700

    changed the version number

commit 085bb3bcb608e1e8451d4b2432f8ecbe6306e7e7
Author: Scott Chacon <schacon@gee-mail.com>
Date:   Sat Mar 15 16:40:33 2008 -0700

    removed unnecessary test

commit a11bef06a3f659402fe7563abf99ad00de2209e6
Author: Scott Chacon <schacon@gee-mail.com>
Date:   Sat Mar 15 10:31:28 2008 -0700

    first commit
```

#### Git Help
```bash
$ git help -a -g
```
This command displays help information about Git. If the option --all or -a is given, all available commands are printed. If the option --guide or -g is given, a list of the useful Git guides is also printed.

# Writing Good Git Commit Messages

![Git Commit](https://imgs.xkcd.com/comics/git_commit.png)

5 minute reading: [Writing Good Commit Messages](https://chris.beams.io/posts/git-commit/)


# Heads & Error Messages you will inevitably see

Each time a new branch is created and a new block of code has been pushed up, Git creates what is known as a new "Head". When a new Head is created, all other instances of the git project across local machines must be updated so that they are all at the same head. If a change is made and the update is not run on the local machine, you will see an error like this:
 
<img src="./assets/git-error.png">

While this may seem a bit scary at first, there are a few simple fixes we'll see

# Resources

- [Atlassian Learn Git](https://www.atlassian.com/git/tutorials/what-is-version-control)
- [Try Git](https://try.github.io/levels/1/challenges/1)
- [Git - the Simple Guide](http://rogerdudler.github.io/git-guide/)
- [The git book](https://git-scm.com/book/en/v2) Read chapters 1-3
