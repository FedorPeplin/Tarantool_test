# How to Use Git_Tarantool_test_Peplin
## Introduction
Hello, dear colleagues! 
This is a quck-start guide to Git. It is a very powerful tool to control versions of projects and save them online instead of just having them on several PC's.
You need absolutely no skill in programming and 10 minutes to read this instruction to become a Git-user. 
> **Note**: this instruction includes information about Windows only and GitHub as service. 

To learn how to adjust Git on another OS or service go to [Official Git website].

## Install

Go to the [Git for Windows] page. Just download and install the package.

## Adjustment
1. Go to [GitHub].
2. Sign up with your name and email.
3. Create project on this website as it is in [Creating repo instruction].
> **Note**: make your project public for the first time. After success, you may change the type of your project and try yourself.

To adjust the git and make it understand that it was you who made changes:
1. Open just installed program **git bash** (as administrator).
2. Type the commands from below, but change requisites according to the algorithm above (signing up).
```sh
git config --global user.name "My Name"
git config --global user.email myEmail@example.com
```
## Creating a folder
You need to adjust the folder before sending in to the Git service.
1. Open **git bash** as administrator, go to the certain folder you want to work with by changing the directory in the example below:
```sh
$ cd C:/Users/user/my_project
```
2. Type an initialization commamd:
```sh
$ git init
```
At this point there are two options: to create a project if it wasn't existed or to change an existed one.
## Creating a new project
If the project wasn't existed before:
1. Continue to work in a folder that you just initialized in chapter **Creating a folder**: add or change images, text files, etc. 
> **Note**: don't close the git bash at this point, keep it open.
2. Come back to the **git bash** and type:
```sh
$ git add *
```
This command will make all of your files in folder "gited". Without it the system won't recognize what to proceed and send to git.
3. Commit changes. At this point you need to make an explanation, what you've done to the folder — commit. This is a required option, without it you can't send your files to git. Write the change description instead of "Initial commit"
```sh
$ git commit -m "Initial commit."
```
4. Сonnect your folder to the existed project in GitHub from chapter **Adjustment**. 
Copy the link in the GitHub project instead of the link below:
```sh
$ git remote add origin https://github.com/yourusername/testproject.git
```
5. Push the project. This is kind of magic, that a random repository in the internet is connected to the exact folder on your computer. 
However, you need the last move to succeed — type in **git bash**:
```sh
$ git push -u origin master
```
6. Wait for that finish and be happy! 
You've just sent your files to the repository you've created in the beginning of this tutorial. You may refresh a page in your browser with open GitHub project to see that all of your files are there.

## Changing an existed project

Working with existed project is much easier — you don't need to create all the files. 

1. Go to the folder, which is different from the one that you've just used in chapter **Creating a new project**.
2. Repeat step #2 from **Creating a folder chapter** (`git init`) and test it with the project that you've just created.
3. In a new folder, type `git clone` and a link to your project:
```sh
$ git clone https://github.com/yourusername/testproject.git
```
After that, you may work with your files as you want - change texts, images, etc.
After you finished, the algorithm of sending the project back is:
1. Repeat step 2 (`git add`) **Creating a new project**
2. Repeat step 3 (`git commit`) **Creating a new project**
3. Repeat setp 5 (`git push`) from chapter **Creating a new project**. 

This will create a new change of your project and refresh an existed one.

That's all. You've just learn the Git basics!


   [Official Git website]: <https://git-scm.com/>
   [Git for Windows]: <http://git-scm.com/download/win>
   [GitHub]: <https://github.com/>
   [Creating repo instruction]: <https://docs.github.com/en/github/getting-started-with-github/create-a-repo>
