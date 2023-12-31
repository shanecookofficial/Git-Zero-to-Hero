# Using Git to Manage Your Code - Intermediate

In your journey as a developer, you've likely gained some experience with Git, and you understand the basics of version control. You can commit, push, and pull code. Now, it's time to delve deeper into Git's capabilities, focusing on collaboration and efficient workflows.

## Prerequisites
Before we dive in, ensure you have the following prerequisites:

- Basic understanding of Git and version control.
- Git installed on your computer.
- A GitHub account.

## Branching Strategies
One of Git's strengths is its branching system. It enables you to work on different features or bug fixes simultaneously without interfering with the main codebase. Here's how to make the most of it:

### Creating and Managing Branches
Branches play a pivotal role in software development, serving as a fundamental element of collaborative coding. In team-based endeavors aimed at constructing substantial software projects, it's imperative that each team member operates within their own isolated workspace to prevent interference with others' contributions. Branches facilitate this by enabling developers to capture a snapshot of a repository and work independently on that snapshot. As they continue to make modifications, the branch evolves, effectively preserving the progress made. Once a developer is content with their contributions or has completed a particular feature, they can seamlessly merge these changes back into the main branch, integrating their work with the collective project. Branches, in essence, offer a structured and organized approach to parallel development efforts, ensuring code stability and collaboration harmony.

Let's create a new branch. Make sure your current working directory is your forked repository.

Execute the following command in your terminal:

`git checkout -b my-branch`

That command creates a new branch and switches to it. If you have uncommitted changes in your old branch, make sure to commit those before moving to a new branch.

Execute the following command in your terminal:

`git branch`

That command lists all branches in your repository. The one with an asterisk (*) is the current branch you are using.

If you want to switch between branches, simply execute the following command in your terminal:

`git checkout branch-name`

That command allows you to switch between different branches, just make sure to replace 'branch-name' with the name of the branch you want to move to.

For the sake of this lesson, make sure you are back in your main branch.

### Merging Changes
Once you are satisfied with your changes in your branch, it is time to merge it back into the main branch.

First, pull any changes that may have been made by executing the `git pull origin main` command in your terminal.

Next, move to the branch you just created by executing the `git checkout my-branch` command.

Open up the hello-world.txt file and make some changes to it and save those changes. Proceed to stage and commit those changes as you have done in the past with other changes.

After that, execute the following command:

`git rebase main`

This command essentially tells git to see if your changes would have any conflicts with the main branch. If there are no conflicts, you will receive a message saying you have successfully rebased. If there are conflicts, git will mark the conflicted areas in the affected files. You have the opportunity to fix those changes by either adding code or removing code.

Once you are done making changes, stage the file for the rebase to continue. When you are ready to continue the rebase, execute the following command:

`git rebase --continue`

Git will continue applying the remaining commits from your branch on top of the main branch. If there are more conflicts, you will repeat the rebasing process by adding/removing code and executing the `git rebase --continue` command.

Some IDEs have the functionality to enhance rebasing with additional visual cues and other features. These can be found in IDEs such as Visual Studio and Visual Studio Code.

### Pull Requests
In a working environment, you will not be able to merge your changes into the main branch without additional approval. That is where Pull Requests fit in.

A pull request essentially is a request for someone to approve your changes and 'pull' them into the main branch. If you have protections enabled on the repository you are working on, you will not be able to merge your changes without having a pull request approved.

Make some more changes in the hello-world.txt file. Stage those changes, commit them, and push them all while inside of the branch you created.

Go to your forked repository in GitHub. Your page should look something like this:

<img src="assets/pull-request.png">

Click the green "Compare & pull request" button. A new screen should load that looks something like this:

<img src="assets/pull-request-page.png">

There is a lot going on here so we are just going to focus on the basics.

The title of the pull request is right above the 'Write' tab. In my example image, it says 'Completed adding information up to Pull Requests'.

The comment or summary of the pull request is located in the section where it says 'Leave a comment'. This section can be very helpful with documenting your changes. You should always leave a detailed comment to help you and those you work with in the future track the progress of changes in the project. Make a comment in your pull request.

Finally, there is the green 'Create pull request' button. That is what we are going to click to create your pull request. Click the button once you have added or edited an appropriate title and added a comment. You will be directed to a new screen that looks something like this:

<img src="assets/merge-pull-request.png">

My pull request summary screen will look a little different than yours because I have branch protections on my repository. This repository is a Git tutorial repository and I am open to accepting contributions but I want those contributions approved before they are added.

Once you are ready to merge your pull request, click the Merge pull request button.