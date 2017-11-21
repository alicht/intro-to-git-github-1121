[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

# Git and Github


## Objectives

-   Synchronize local and remote repositories.
-   Fork a remote repository.
-   Clone a remote repository.
-   Collaborate with other developers on the same project.
-   Create a new branch, pull requests, and merging
-   Don't be like the characters from "Mean Girls" :no_good:


## Overview



In our previous lesson, we learned about git and created a local repository. But what about a remote repository?

## Remotes

![Alt Text](https://media.giphy.com/media/3orifhOeMIcO6YE0fu/giphy.gif)

A remote repository is just another repository that you are connected to and
(depending on your permission) you can push code up to it and pull code down from
it.

## Introducing GitHub!

So we have a local repository, but now let's use GitHub to create our remote repository. Why use
GitHub? So we can backup our code online. It also has an stellar graphical interface and useful collaboration features.

If you work by yourself, you don't really need remotes. However, we want to work with others! Thus let's talk about remotes.


## Let's create a remote repository on GitHub

-  let's go to GitHub, click the BIG plus sign in the menubar and select New repository. 
-  let's enter a name for our repository in the repository name field. We'll enter the same name we did for our local version `mean-girls` 


## Lets connect our local repo and our remote repo

![mg1](https://user-images.githubusercontent.com/6153182/33035113-09f033dc-cdf8-11e7-8f7a-24fda5b84a2c.png)

-  since we already have a repo we'll follow step 2
-  go to terminal 
-  lets add the URL we copied to 
-  `git remote add`
-  `git remote push`

### Connected!


## We do: Lets add another Mean Girl... and this time we can push it to GitHub!

![Alt Text](https://media.giphy.com/media/xT9KVtQBk8cGFcZH4A/giphy.gif)

The last time we saw the Mean Girls, Regina was kicked out. Let's now add Karen to take her place: 

-  NEW: create a new branch in the terminal

-  create a `karen.txt` file and add:

`"There's a 30% chance that it's already raining"`  


Push this to GitHub.


#  Add Tina Fey (last Mean Girls reference, I promise :grimacing: )
Tina Fey is here to teach us about forking, cloning, and pull requests! 

##### (we have a You Do coming up guys- so pay attention! :)


![Alt Text](https://media.giphy.com/media/3o7aTLkyh3yAG6DEuQ/giphy.gif)



## Fork

![fork](https://user-images.githubusercontent.com/6153182/33048606-bed6d2c0-ce29-11e7-8f54-bf7cf4560dec.png)

## Clone

![clone](https://user-images.githubusercontent.com/6153182/33048675-24e2bc50-ce2a-11e7-804f-634a7790107c.png)

## Pull request

![bridgid](https://user-images.githubusercontent.com/6153182/33048688-3098920e-ce2a-11e7-9873-29cc04f36d49.png)

#### To recap:
-  `fork`
-  `clone`
-  `new branch, tina-fey.txt & "Go home", add/ commit/ push`
-  `create pull request`

# You do: Adding to Other's Stories

Working with a partner, follow the example we just did and take turns: (Example names: Ruben & Leah)
-  Ruben should clone Leah's repo & create a new branch in the terminal
-  on this new branch, add your-name.txt and add your "catchphrase" to the text inside
-  Ruben should create a pull request
-  Leah  should accept this pull request and merge it into her GitHub repo
-  Leah should pull the new changes Ruben made (via using the terminal)

and vice versa.

## Pulling: Updating Your Local

Each of you should now have updated code on GitHub, but your local Git repo
will be behind.  We need to get the latest code off of GitHub.  We can do this
by pulling the changes that we merged.  The command to do this is:

`git pull origin master`

This gets the latest copy of our code from the master branch of our original
repository.


# Be the Opposite of "Mean Girls"

![Alt Text](https://media.giphy.com/media/xT5LMXR7iA0mSSxOBG/giphy.gif)

We're all in this together #narwahls :whale:





## Additional Resources

-   [Git Commands](https://confluence.atlassian.com/bitbucketserver/basic-git-commands-776639767.html)
-   [An Introduction to Git and GitHub by CS50](https://www.youtube.com/watch?v=MJUJ4wbFm_A)
-   [Github's fork page](https://help.github.com/articles/fork-a-repo/)
-   [Branching](https://guides.github.com/activities/hello-world/)

