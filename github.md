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


