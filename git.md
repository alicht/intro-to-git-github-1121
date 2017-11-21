[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

# Git Basics

## Objectives

-   Initialize a git repository in order to track changes.
-   Commit new and changed files to a git repository.
-   Place new or changed files into the staging area to prepare them for a commit.
-   Remove files from the staging area before a commit.

## Prerequisites

-   WDI Fundamentals

## Why Git
Git is a form of Version Control. 
Version Control is the process of storing multiple versions of a single project, allowing each version to be recalled at a later date. (Ex: backing up your iPhone before you get it repaired).

As developers our code is our livelihood so it's important
that we safely and frequently store our work.  Not only that, we want to track our
changes as we make them.  If we make a feature that ends up breaking the rest of
our app we want to be able to go back to a point when our app was last working.

## But... who cares why would we need this?
Using version control is useful because we can easily rollback to a previous version of our application, saving us a ton of extra work and time.
There are a lot of advantages to version control. 
-  it's a great way to keep a backup of your work
-  it facilitates collaboration
-  it gives us the freedom to experiment and try new things without messing up the code base.



## Let's Make a Local Repository!

![Alt Text](https://media.giphy.com/media/3o7aTy3ePwrk5D3bHO/giphy.gif)


Let's initalize a local repository.

-  make a directory `mkdir mean-girls` and lets then enter it `cd mean-girls`

Before we put git to use let's create some items.
let's go to our terminal and use the `touch` command to create `opening-scene.txt`.

- we can use the `ls` command now and we see we have something in our directory.
- we can check the status of this with git status` and we'll see our README is not committed

We have an (empty) directory, now what we want to do is initialize it `git init`
This will initialize a new git repository in our code. (.git explanation?)


- let's `git add <name-of-file>`
- we can check the status of this `git status`
- then we'll add a commit message `git commit -m"our first commit"`

## And...
 ![Alt Text](https://media.giphy.com/media/xT9KVF4zNt70nyNpi8/giphy.gif)
 

Git tells us that it created a new version of our code. The commit changed 1 file. With that commit made and no other changes to our files, if we ask Git what the status of our project is now we'll see that there is nothing to commit and no new changes. 


## Staging and Commiting

There are 3 states that your file can reside in `modified`, 
`staged`, and `committed`. These states map to the different sections of a Git project.

A)  `modified` means that you have changed the file but have not committed it to
your database yet.

B)   `staged` means that you have marked a modified file in its current version
to go into your next commit snapshot.

C)   `committed` means that the data is safely stored in your local database.


When we add a file we are moving it from the working directory to the staging
area.

![git-add-commit](https://user-images.githubusercontent.com/6153182/33028677-839cda1e-cde4-11e7-83c5-59adf22958d9.png)


## Code Along: Let's add Gretchen
![Alt Text](https://media.giphy.com/media/aDub09OOi8e4M/giphy.gif)



1.  Create a directory called `mean-girls`. 

1.  Inside of the `mean-girls` directory create a file called `gretchen.txt`.

1.  Opening the file with Sublime and copy in the following lines:

  ```bash
  That is so fetch!  
  ```

1.  Save the file.

1.  Inside of the `mean-girls` directory type `git status`. Did anything
happen?

1.  Again, inside the `mean-girls` directory type `git init`.

1.  Type `git status` again. Did anything happen this time?



# You do

## Brief Lab: Add Regina George
![Alt Text](https://media.giphy.com/media/6BQeMAeLHCIhi/giphy.gif)

(she's not very nice :/)

1.  Opening the file with Sublime and copy in the following lines:

  ```bash
  Is butter a carb? These sweatpants are all that fits me right now. 
  ```


Now that we've made our first commit, let's see what happens when we type `git
log`... We see our previous commit! This typically shows all of our previous
commits, but since we just have one, that's all we see. Feel free to play around
with options for `git log`, like `--oneline`, `--name-status`, and `--graph`
for example. For all options [click here.](https://git-scm.com/docs/git-log)




## Unstaging: Wait can Regina actually join us? She's wearing sweatpants on a Wed... 

![Alt Text](https://media.giphy.com/media/xT9KVuimKtly3zoJ0Y/giphy.gif)

Uh oh... we have to delete Regina 

Unstage the file with `git reset <"filename">`

OR Delete the last thing we wrote in our `mean-girls` directory.

Let's go back to our Mean Girls directory

we'll go to our terminal and remove it `rm -rf regina.txt` 



What's the difference? What is actually happening with the `rm` command?



## Git Workflow Checklist

-   [ ] `git status` to confirm clean working directory
-   [ ] make changes to `<file-name>`
-   [ ] `git add <file-name>`
-   [ ] `git status` (to confirm modified files have been staged)
-   [ ] `git commit`
-   [ ] `git push origin <branchname>`

## Git Best Practices

-   ALWAYS add files explicitly. If you have multiple files, use full paths to
    refer to each. Example: `git add foo/bar.md baz/qux.js`
-   ALWAYS use a commit message `git commit -m "an example commit message"`
-   ALWAYS use `git status` before any other command
-   NO commit is too small
-   NEVER nest repositories

## Additional Resources

-   [Git Commands Cheatsheet](command-reference.md)
-   [Learn Version Control with Git](http://www.git-tower.com/learn/git/ebook)
-   [Visualizing Git Commands](https://onlywei.github.io/explain-git-with-d3/)
-   [Learn Git Branching](http://pcottle.github.io/learnGitBranching/)

