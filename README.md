# Introduction to Git and Github

Git is a version control tool. In one way or the other you may need to use a git and a github.
You need to use git and github either to store your projects on the cloud or to collabrate with your team.
A version control is a means of recording changes to a file or set of files over time so that you can recall specific versions later.

## 1. Install Git and Signup on Github

- Git:
  Install [git](https://git-scm.com/downloads)
- Github
  Signup on [github](https://github.com/)

## 2. Configure your name and your email

```shell
git config --global user.name 'yourname'
git config --global user.email 'youremail'
```

## 3. Create a local git repository

On this step your will create a folder (directory) for your project. A local repository is a project or a folder which is on your computer.
Go to start and type git bash. Git terminal will popup. On the terminal write:

```shell
mkdir project_name
cd project_name
```

## 4. Initialize Git

After creating a new local repository or in an existing local repository, intitialize the repository by the following command:

```shell
   git init
```

Once, the repository is intialized git tracks the changes in the files and folders.

## 5. Add file to the staging area

File can be added to the stagging area in multiple ways.
To add single file

```shell
   git add filename
```

To add multiple files

```shell
   git add filename1 filename2
```

To add all files and folders at once

```shell
   git add .
```

## 6. Unstage a file

```shell
    git reset HEAD filename
```

## 7. Commit the changes

Commiting means taking a snapshot or a copy of your file at that point of time.

```shell
   git commit -m 'your message'
```

Your commit message has to be associated with the changes or modification you make.

## 8. Creating a branch

You can create copy of the master using branch. You built an awesome application. You like to keep this awesome application as it is and you like to add some features.
This is the time, you need branching the master. Branch is the copy of the master at branching instant. After branching the branch and the master they don't see each other. You can create as many branches as you want.

To create branch:

- Only to create branch

```shell
    git checkout  branchname

```

To create branch:

- To create and checkout to the branch at the same time:

```shell
    git checkout -b branchname

```

To switch between branches:

```shell
    git checkout master
    git checkout branchname
```

To list down all the branches:

```shell
    git branch
```

## 9. Create Repository on Github

Go to [github](https://github.com/) and create a repository by click the plus icon on the top right corner.

## 10. Connecting git with remote repository

In this step you will connect your local git repository with your remote github repository

```shell
    git remote add origin remote_repository_ul

```

The word origin could be any word. It is a means to assign the repository url.
If this is step is passed without error, you are ready to push it to your remote github repository

## 11. Push

Commits if you have any changes and be ready to push your files to your remote github repository
git push -u origin master

## 12. Merge

When you work on an individual project or a team project you may have different branches. Mostly you will have master, develop and other branchs.Then you will merge other branchs to your develop and your develop to master. It is possible to merge any branches. For instance lets merge feature branch to develop

```shell
    git checkout develop
    git merge feature

```

## 12. Pull

If your team merge new features to the develop. Then you will be behind, now you need to make your project to current stage by pulling from develop

```shell
    git checkout yourbranch
    git pull origin develop
    git checkout develop
    git merge yourbranch
    git push -u origin master


```

## Git cheatsheet:

Here you have the basic git commands which might be useful:

```shell
git --version //to check the version
git help  // To get help from git
git help commit // To get commit help

git init  // Initilaizing git repository on local machine

git config --list // to check what is configured
git config // to get information about configuration
git config --global user.name "username" //Configuring git user name
git config --global user.email "email" //Configuring git user email

git add filename
git add first.txt # adding only one file
git add second.txt third.txt // to add multiple file
git add . //To add all the files and folders to the staging area

git commit -m 'commit message' // after staging using add
git commit -a -m 'commit message' // staging using a and commiting
git commit -am 'commit message' // staging and committing

git commit -am "Message" #Grab every thing in the working copy and -a allows to skip the staging copy
git log  // To see the history on the repository
git log --author ="name" #To check change by specific user
git status  //To check changes or status of the file


git diff #Compare workin copy in the repository
git diff --staged # Compare files in the staging area

git rm filename
git mv filename1 filename2
git mv filename foldernam/filename2
git commit -am "This skip the stage process"
git checkout -- filename #To get working copy back
git reset  HEAD filename // removes from the staging area/unstage
git checkout 01e7ba -- filename # Tracking the differentversion of the project
git remote add anyname repositoryUrl
git push -u remote master // to push the file into github
git checkout 01e7ba -- filename
git remote add anyname repositoryUrl
```
