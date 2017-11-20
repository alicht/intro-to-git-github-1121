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

## to add
-  fork
-  clone
-  pull request
-  git fetch upstream?
-  merge
-  branching?

Continuing with what we started [Git Basics](https://git.generalassemb.ly/ga-wdi-boston/git) we are going to use Github
to manage our project.

## Remote Repository-  Linking with GitHub


![Alt Text](https://media.giphy.com/media/3orifhOeMIcO6YE0fu/giphy.gif)

So we have a local repository, watch as I create a GitHub repository. Why
GitHub? So we can backup our code online. It also provides us with a useful
graphical interface and useful collaboration features.

GitHub is just another git repository in the cloud. If you work by yourself, you don't need remotes. However, we want to work with others! Thus let's talk about remotes.


## Let's create a remote repository on GitHub

-  let's go to GitHub, click the heavy_plus_sign in the menubar and select New repository. 
-  let's Enter a name for your repository in the Repository name field. let's enter the same name we did for our local version `mean-girls` 
-  After creating the repo, you should see a "Quick setup" page. Click the "Copy to clipboard" symbol next to the repo URL (pictured) to copy the URL. (We'll use this in the next section.)

Now create your own GitHub repository and `push` your master branch.

## Lets connect our local repo and our remote repo
-  since we already have a repo let's follow step 2
-  go to terminal 
-  lets add the URL we copied to 
-  `git remote add`
-  `git remote push`

### Connected!

# We Do

## Lab: Lets add another Mean Girl... and this time we can push it to GitHub!

![Alt Text](https://media.giphy.com/media/xT9KVuBS9UBLUciObu/giphy.gif)

The last time we saw the Mean Girls, Regina was kicked out. Let's now add Cady Heron to take place: 

create a cady-heron.txt file and add "Hey I'm Cady, I'm in charge now" #boss 


Push this to GitHub.


## Demo: Adding to Your Story

Watch as I `fork` and `clone` one of your repos and make an addition by
creating a `pull request`.

# You do

## Lab: Adding to Other's Stories

Working with a partner follow my example and take turns adding to one another's
stories. Accept each other's pull requests.  After you've each gone once stop.

## Pulling: Updating Your Local

Each of you should now have updated code on GitHub, but your local Git repo
will be behind.  We need to get the latest code off of GitHub.  We can do this
by pulling the changes that we merged.  The command to do this is:

`git pull origin master`

This gets the latest copy of our code off of the master branch of our original
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


## Additional Resources

-   [Git Commands](command-reference.md)
-   [Github's fork page](https://help.github.com/articles/fork-a-repo/)
-   [An Introduction to Git and GitHub by CS50](https://www.youtube.com/watch?v=MJUJ4wbFm_A)

## [License](LICENSE)

1.  All content is licensed under a CC­BY­NC­SA 4.0 license.
1.  All software code is licensed under GNU GPLv3. For commercial use or
    alternative licensing, please contact legal@ga.co.


