# Introduction to Git and Github
Git is version control tool. In one way or the other you may need to use git and github either to store your project on the cloud or to collabrate with your team.
A version control is a means of recording changes to a file or set of files over time so that you can recall specific versions later. 

## 1. Install Git and Signup on Github
* Git:
    Install [git](https://git-scm.com/downloads)
* Github
    Signup on [github](https://github.com/)

## 2. Congigure your name and your email
```shell
    git config --global user.name 'yourname'
    git config --global user.email 'youremail'
    git config --global color.ui 'auto
```
## 3. Create a local git repository
On this step your will create a folder(directory) for your project. A local repository is a project or a folder which is on your computer.
Go to start and type git bash. Git terminal will popup. On the terminal write:
```shell
    mkdir project_name
    cd project_name
```
## 4. Initialize Git

After creating a new local repository or in an existing local repository, intitiale the repository by the following command:

```shell
  git init 
```
Once, the repository is intialized git tracks the changes in the files and folders.
## 5. Add file to the staging area
File can be added to the stage area in multiple ways. To add single file
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
## 6. Commit the changes
Commiting means taking a snapshot of the copy of your file and archiving it for use if it is needed.
```shell
  git commit -m 'your message'
```

Your commit message has to be associated with the changes or modification you make. 




