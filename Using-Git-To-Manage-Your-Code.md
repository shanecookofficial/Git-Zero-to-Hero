# Using Git to Manage Your Code

Imagine you and your team are collaborating on a software project to create a Tic-Tac-Toe game. Each member of the team is responsible for a specific aspect of the project. As changes and updates are required, everyone must manually copy and integrate the code onto their individual computers. This process can quickly become arduous and time-consuming when changes need to be passed back and forth through email or Google Drive. Moreover, there is the risk of unintentionally introducing bugs into the codebase. In such a scenario, it becomes difficult to pinpoint who made the changes and when they were implemented. Debugging becomes a daunting task, potentially leading to weeks of lost progress.

A problem like this could have easily been prevented with the use of a version control system like Git.

## Prerequisites

- An idea of what a version control system is
- An idea of what Git is
- Git downloaded on your computer
- An idea of what GitHub is
- A GitHub account

## What is a repository?

A repository essentially is a folder that contains files for a software project.

In the example above, a shared repository could have easily solved a lot of the problems for the group working on the Tic-Tac-Toe project. GitHub is a cloud service that allows for repositories to be stored in the cloud.

Many software teams use cloud services such as GitHub to work on software projects together. The main repository is stored in the cloud which allowws for teams to be able to work on the same codebase together. Each person will _clone_ the main repository to their own computer and work on whatever feature they are assigned.

We are going to practice this right now!

## Practice

1. Go to [this repository](https://github.com/shanecookofficial/Git-Zero-to-Hero).
2. Fork the repository by clicking the Fork button.

<img src="assets/fork-button.png">

3. Change the name of the repository and make sure your username is selected as the owner. Click create fork when you are done. You have now created your a repository! A fork essentially is a copy of a repository.

<img src="assets/create-fork.png">

4. Your screen should now have the name of your new repository instead of Git-Zero-to-Hero. If it does, click the green code button. A drop down should open below the button.

<img src="assets/code-button.png">

5. Make sure HTTPS has an underline indicating it has been selected. If you are working on a smaller screen, it might be darkened grey. Once you have verified it is selected, click the copy button.

<img src="assets/copy-button.png">

6. Open up a terminal and type the following command:

   git clone -copied url-

   Make sure to replace -copied url- with the url you copied from GitHub.

   Whenever you want to execute a git command, always preface the command with 'git'. Just now, we executed the 'git clone' command which allows us to clone a repository from the internet. There are several ways you can go about this like through SSH but for the sake of this tutorial, we will be using HTTPS.

   Once you execute the command, you will be prompted to enter your github username and password. Do so.

   Congradulations on executing a git command!