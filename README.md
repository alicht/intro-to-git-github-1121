[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

# Git Basics

## Objectives

-   Initialize a git repository in order to track changes.
-   Create a new branch to isolate your changes.
-   Place new or changed files into the staging area to prepare them for a
commit.
-   Remove files from the staging area before a commit.
-   Commit new and changed files to a git repository.

## Prerequisites

-   WDI Fundamentals

## Why Git
Git is a form of Version Control. 
Version Control is the process of storing multiple versions of a single project, allowing each version to be recalled at a later date. (Ex: backing up your iPhone before you get it repaired)

## But... who cares why would we need this?
Using version control is useful because it allows you to easily rollback to a previous version of your application, saving you a ton of extra work and time.
There are a lot of advantages to version control. 
-  It's a great way to keep a backup of your work
-  it facilitates collaboration
-  it gives you the freedom to experiment and try new things without messing up the code base.

As developers our code is our livelihood so it's important
that we safely store our work... frequently.  Not only that we want to track our
changes as we make them.  If we make a feature that ends up breaking the rest of
our app we want to be able to go back to a point when our app was last working.

## Local vs Remote
A local version control system stores all of the information on your computer, locally. This system is great while you work on a project by yourself. However, it becomes trickier when you attempt to collaborate.


![Alt Text](https://media.giphy.com/media/fb04se26vMZZm/giphy.gif)


## Code Along: Making a Local Repository

Let's initalize a local repository.

-1 make a directory `mkdir game-of-thrones` and lets then enter it `cd game-of-thrones`

We have an (empty) directory, now what we want to do is initialize it `git init`
This will initialize a new git repository in our code. (.git explanation?)

-  now lets put git to use and create some items!
let's use the touch command to create a README.me -> README.md.

- we can use the ls command now and we'll see our README.
- we can check the status of this `git status` and we'll see our README is not committed
- let's `git add <name-of-file>`
- we can check the status of this `git status`
- then we'll add a committ message `git commit -m"our first commit"`

-Git tells us that it created a new version of our code. The commit changed 1 file. With that commit made and no other changes to our files, if we ask Git what the status of our project is now, we'll see that it is at a "Clean State", that there is nothing to commit and no new changes. 


1.  In your training directory, NOT the directory you just cloned, create a subdirectory called `<your-name>s-game-of-gits`. So if your name is Kyrie, it should be called `kyries-game-of-gits`.

1.  Inside of the `<your-name>s-game-of-gits` directory create a file called `sad-tale.md`.

1.  Opening the file with Sublime/ Atom and copy in the following lines:

  ```bash
  House Stark of Winterfell is led by the just Eddard "Ned" Stark, Lord of
  Winterfell, Warden of the North, Hand of the King, Protector of the Realm,
  Regent.  He is surely honorable and will lead a long and prosperous life.
  ```

1.  Save the file.

1.  Inside of the `<your-name>s-game-of-gits` directory type `git status`. Did anything
happen?

1.  Again, inside the `<your-name>s-game-of-gits` directory type `git init`.

1.  Type `git status` again. Did anything happen this time?

## Code Along: Staging and Commiting

Using `git add <"name_of_file">` we are going to add our story to the staging
area.

There are 3 states that your file can reside in `committed`, `modified` and
`staged`.  These states map to the different sections of a Git project.

-   Modified means that you have changed the file but have not committed it to
your database yet.
-   Staged means that you have marked a modified file in its current version
to go into your next commit snapshot.
-   Committed means that the data is safely stored in your local database.

[Git Basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics)

![Git Sections](https://git-scm.com/book/en/v2/book/01-introduction/images/areas.png)

When we add a file we are moving it from the working directory to the staging
area.

Now that our file is staged let's commit our file by typing `git commit`, Atom
should open. **Do Not Use `git commit -m <message>`**

When you use -m to create an inline commit you are doing yourself and others a
disservice.  Your commit will be inherently poor due to the short nature of
inline commits, and the lack of a body description to it. This is surely a sign
of a poor developer and one that does not respect his or her teammate's time.

## Lab: Crafting A Commit

Read over the following blog posts and carefully think about what a good commit
message would be. Take some time to come up with your own. Be ready to share
your commit with the rest of the class.

-   [A Note About Git Commit Messages](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
-   [What's in a Good Commit?](http://dev.solita.fi/2013/07/04/whats-in-a-good-commit.html)

Now that we've made our first commit, let's see what happens when we type `git
log`... We see our previous commit! This typically shows all of our previous
commits, but since we just have one, that's all we see. Feel free to play around
with options for `git log`, like `--oneline`, `--name-status`, and `--graph`
for example. For all options [click here.](https://git-scm.com/docs/git-log)

## Staging: And He Lived Happily After

Together, let's continue our story.

In our `sad-tale.md`, we'll tell the rest of Ned Stark's story.  Paste this in
below our current description and save:

```sh
Ned Stark went to King's landing where he made lots of friends and lived
happily ever after...  He definitely didn't get axe murdered.
```

Now using what we learned earlier stage this change. To figure out the status
of your files you can type `git status` in the terminal at any time.

**Remember: Staging isn't committing**

## Unstaging: Maybe We Jumped the Gun

It turns out Ned actually did get axe murdered. So we probably want to unstage
our file.

Unstage the file with `git reset <"filename">`

Delete the last thing we wrote in `sad-tale.md`.

We know that Ned's story doesn't have a happy ending but let's dream big.  We're
going to create a dream-story branch and write what we would have wanted to
happen.

## Removing: Now we need to remove files previously added

1.  Inside of `<your-name>s-game-of-gits` create a file called `the-stark-bunch.md`.

1.  Type `This is a story... of a man named Neddy... and three
very badass really awesome girls`.

1.  Save the file.

1.  `git add the-stark-bunch.md`.

1.  `git rm -f the-stark-bunch.md`.

What's the difference? What is actually happening with the `rm` command?

## Branching: Multiple Stories, One Main Plot

Similar to having one main story and various sub-plots--a branch lets us
effectively duplicate and section off the code we have writte thus far, make
alterations to it, and if we would like at some point we can join it back to the
main branch (typically called `master`).

Create a branch called `dream-story` by typing `git branch dream-story`.
_You can see all your current branches at any time by tying `git branch`._

Now that we've created our branch--in order to use it we have to switch to it.
We can do this with the command `git checkout <"branch_name">`.

## Lab: Branching Your Dreams

1.Switch to your `dream-story` branch and write a brief description of what
you would have wanted to happen to Ned.

2.Save the file, Stage and commit your changes.

3.Switch back to your `master` branch. (Notice anything?) Add what really
happened to Ned.

4.Stage and commit your changes.

(Be ready to talk about any issues you many have encountered or strange things
you may have noticed).

## Git Workflow Checklist

-   [ ] `git status` to confirm clean working directory
-   [ ] confirm branch is correct
-   [ ] make changes to `file`
-   [ ] `git add 'file'`
-   [ ] `git status` (to confirm modified files have been staged)
-   [ ] `git commit`
-   [ ] `git push origin <branchname>`

## Git Best Practices

-   NEVER use `git add .`
-   ALWAYS add files explicitly. If you have multiple files, use full paths to
    refer to each. Example: `git add foo/bar.md baz/qux.js`
-   NEVER use `git commit -m "an example commit message"`
-   ALWAYS use `git status` before any other command
-   NO commit is too small
-   NO commit message is too long
-   NEVER nest repositories

## Additional Resources

-   [Git Commands Cheatsheet](command-reference.md)
-   [Learn Version Control with Git](http://www.git-tower.com/learn/git/ebook)
-   [Visualizing Git Commands](https://onlywei.github.io/explain-git-with-d3/)
-   [Learn Git Branching](http://pcottle.github.io/learnGitBranching/)

## [License](LICENSE)

1.  All content is licensed under a CC­BY­NC­SA 4.0 license.
1.  All software code is licensed under GNU GPLv3. For commercial use or
    alternative licensing, please contact legal@ga.co.

=============

[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

# Git and Github

## Objectives

-   Manage changes in a project over time.
-   Collaborate over time and space with other developers on the same project.
-   Fork a remote repository to get your own remote copy.
-   Clone a remote repository to get your own local copy.
-   Synchronize local and remote repositories.

## Prerequisites

-   [Git Basics](https://git.generalassemb.ly/ga-wdi-boston/git)

## Overview

Continuing with what we started [Git Basics](https://git.generalassemb.ly/ga-wdi-boston/git) we are going to use Github
to manage our project.

## Demo: Linking with GitHub

So we have a local repository, watch as I create a GitHub repository. Why
GitHub? So we can backup our code online. It also provides us with a useful
graphical interface and useful collaboration features.

Now create your own GitHub repository and `push` your master branch.

## Lab: More Pushing

The last time we saw Ned Stark we had just written his fate.  Below his story
write the beggining of another character's story.  For instance:

> Joffrey Baratheon was the one to do Ned in, but his story was only about to
> being, and let me assure you he will ___DEFINITELY NOT DIE!___

Push the changes you made.

Also push your `dream-story` branch.  We pushed our `master` branch with the
command `git push origin master`.  Can you figure out how to push our
`dream-story` branch?

## Demo: Adding to Your Story

Watch as I `fork` and `clone` one of your repos and make an addition by
creating a `pull request`.

## Lab: Adding to Other's Stories

Working with a partner follow my example and take turns adding to one another's
stories. Accept each other's pull requests.  After you've each gone once stop.

## Pulling: Updating Your Local

Each of you should now have updated code on GitHub, but your local Git repo
will be behind.  We need to get the latest code off of GitHub.  We can do this
by pulling the changes that we merged.  The command to do this is:

`git pull origin master`

This get the latest copy of our code off of the master branch of our original
repository.

## Remotes

A remote repository is just another repository that you are connected to and
depending on your permission you can push code up to it and pull code down from
it.

The command for adding a new remote is `git remote add <remote-name> <remote-URL>`. You may choose any name for the remote-name but it should be sensible. The remote URL can be copied by clicking the green `Clone or Download` button that is on every GitHub repo, then selecting `SSH` and copying it.

Watch as I add a remote from one of your repositories then update my local with
the changes. You will be asked to do this next.

## Adding Your Own Remote

Working with the same partner from before one of you will be the primary
repository, the other will be a contributor.

1.  The contributor will add the primary repository as a remote.

2.  The primary will push their latest story to the master branch.

3.  The contributor will pull the master branch from the primary.

4.  The contributor will add to the story and push their changes to their own
repository and create a pull request to the primary.

5.  The primary will accept the pull request and pull the changes to their
local.

6.  The primary will add to the story and push the changes to their master
branch.

7.  The primary and the contributor will go back and forth adding to the story.

## Editing on GitHub

Hey! See that little pencil button on the top of a page on GitHub!? That looks
to change text and will help us, right?!
![Edit Pencil](https://i.imgur.com/Drt2g9u.png)
Wrong! DON'T EVER USE THAT! Regardless of how small changes are you typically
never want to edit ON GitHub. You always want to make changes locally and push
 them.
The reason we never want to do that is if you edit in the cloud, our local repo
and GitHub repo become out of sync and it breaks convention.

## Additional Resources

-   [Git Commands](command-reference.md)
-   [Github's fork page](https://help.github.com/articles/fork-a-repo/)
-   [An Introduction to Git and GitHub by CS50](https://www.youtube.com/watch?v=MJUJ4wbFm_A)

## [License](LICENSE)

1.  All content is licensed under a CC­BY­NC­SA 4.0 license.
1.  All software code is licensed under GNU GPLv3. For commercial use or
    alternative licensing, please contact legal@ga.co.


