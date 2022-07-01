# GIT
Description of GIT
Introduction: What is GIT? Git is a free and open-source distributed version control system, which is designed to handle everything from small to very large projects with speed and efficiency.

So Why Git? What are the advantages? Imagine a scenario without using Git.

There is a large project and 100 developers are working on the project.

Developers used to submit their codes to the central server without having a copy of their own. Any changes made to the source code were not known to the other developers. There was no communication between any of the developers. Now, let's analyse the scenario after using Git.

Every developer has an entire copy of the code on their local system. Any change made to the source code can be tracked by others. There is regular communication between the developers. Therefore, for large projects that involve thousands of developers, Git helps those developers to work collaboratively and efficiently in a structured manner. Learn More. image

Learn GIT: Basics to Advanced Concepts

Uses of Git Git is used to tracking changes in the source code. Distributed version control tool used for source code management. Allows multiple developers to work together. Supports non-linear development because of its thousands of parallel branches.
Features of Git Free and open-source Tracks history Supports non-linear development Creates backup Scalable Supports collaboration Branching is easier Distributed development.
Git WorkFlow The following image shows the git workflow diagram:
In Git, the workflow is mainly divided into three areas -

Working directory - This is the area where you modify your existing files. Staging area (Index) - In this, the files in your working directory are staged and snapshots are added. Git directory or repository - It is basically where you perform all the changes that need to be made i.e. perform commits to branch, checkout branch, make changes etc. image 4. Install Git: Installation in Windows/Linux/Mac OS X Install Git on Windows -

Download the latest version of Git from here. After starting the installer, follow the command on the screen and press Next to complete the installation. Open Command Prompt and run the following command to configure Git on your PC using your username and email. git config --global user.email "user_emails@interviewbit.com" This configures Git on your PC with your username and email.

Install Git on Linux -

You can install Git on Linux using the command apt-get : sudo apt-get install git Configure your username and email using the following command: git config --global user.email "user_email@interviewbit.com" Install Git on Mac OS -

Download the latest version of Git from here. Open the installer and follow the instructions. Now since Git is installed, open command line and configure your username and user email. git config --global user.email "user_email@interviewbit.com" 5. Git Clone git clone is a command which is used to clone or copy a target repository.

The following image shows an illustration of the git clone command. Using the command, a copy image How to clone a repository?

Open Github and navigate to the target repository which needs to be cloned. Under the repo name, click on the tab Clone or Download. An option named Clone with HTTPS appears. Copy the Clone URL. Open a command line and use the command: git clone <repo_URL> In this way, a clone of the target repository can be made.

Clone a specific branch from the repository.

A very useful feature of the git clone is that it allows cloning a specific branch of the target repository without having to clone the entire repository. To clone a specific branch, you need to use the command -b to specify the branch. The following command is used:

git clone -b <Branch_name> <Repo_URL> 6. Git Branch A branch in Git is used to keep your changes until they are ready. You can do your work on a branch while the main branch(main) remains stable. After you are done with your work, you can merge it to the main branch. For creating a new branch, the following command is used :

git branch <branch_name> For example -

git branch demo This command creates a new branch named demo from the Main branch: image The diagram shows there is the main branch. There are two more branches small feature and large feature working separately. Once the work is complete for the two separate branches, you can merge it into the main branch. 7. Git Switch Branch Using the git checkout command, we can switch from one branch to another.

Command :

git checkout <branch_name> 8. Create Remote Branches Git doesn’t allow creating a new and isolated branch on a remote repository. But, you to make a branch remote, we can push an existing local branch.

The steps to create a remote branch is as follows:

Create a local branch and switch to that branch: git checkout -b <branch_name> Push in the local branch: git push -u origin <branch_name> Note: origin is the default name of remote Now, if someone wants to fetch some information, one can simply run:

git fetch git checkout <branch_name> 9. Delete Branches Once the work is done on a branch and merged with the Main branch, one can delete the branch.

The following command is used to delete branches:

git delete -d <branch_name> Note: This command deletes a copy of the branch, but the original branch can still exist in remote repositories. To delete remote branches, use the following command:

git push origin --delete <branch_name> 10. Git Checkout The Git checkout is used to command Git on which branch changes have to be made. Checkout is simply used to change branches in repositories. It can also be used to restore files.

The following image describes the scenario of creating different branches and switching to a brach when needed, i.e. we can switch from the main brach to a different branch and vice versa. image

Git Checkout Branch To checkout or create a branch, the following command can be used:

git checkout -b <branch_name> This will simply switch to the new branch branch_name.

Git Checkout Tag While working on a large codebase, it because easy to have some reference point. That is where the checkout tag is used.

The following command is used to specify the tagname as well as the branch that will be checked out.

git checkout tag <branch_name> 11. GIT Status git status is mainly used to display the state of the staging area and the repository. It helps us to track all the changes made, point out untracked files.

Command:

git status git status after a file is added

Add files to the repo using the following command: touch file.txt Execute git status. A message would be displayed, describing the changes done to the repository. git status after a file is deleted after commit

Delete the file using the following command: git rm file.txt Execute git status. A message would be displayed, describing the file has been deleted. 12. Git Commit Git commit is used to record all the changes in the repository. The git commit will commit all the changes and make a commit-id for the same for tracking down the changes made as shown in the image below.

As shown in the image, the command git commit creates a commit-id to track down changes and commits all the changes to the git repository. image Command:

git commit git commit -m The -m along with the command lets us write the commit message on the command line.

Command:

git commit -m "Commit message" git commit -am The -am along with the command is to write the commit message on the command line for already staged files.

Command:

git commit -am "Commit message" git commit -amend The amend is used to edit the last commit. In case we need to change the last committed message, this command can be used.

Command:

git commit -amend git rm rm stands for remove. It is used to remove a collection of files. The git rm command is used to remove or delete files from the working tree and index.

Command:

git rm <file_name> Now, if you use the command git status, it would show, that the file has been deleted.

Git Merge Git merge is a command that allows you to merge branches from Git. It preserves the complete history and chronological order and maintains the context of the branch.
The following image demonstrates how we can create different features by branching from the main branch and how we can merge the newly created features after the final review to the main branch. image

The command git merge is used to merge the branches.

Command :

git merge <branch_name> 14. GIT Rebase Git Rebase is a process of combining a sequence of commits to a new base commit.

The primary reason for rebasing is to maintain a linear project history. When you rebase, you ‘unplug’ a branch and ‘replug’ it on the tip of another branch(usually main). The goal of rebasing is to take all the commits from a feature branch and put it on the main branch. The following rebase command is used for rebasing the commits:

git rebase <branch_name> 15. Git Fetch Git Fetch only downloads the latest changes into the local repository. It downloads fresh changes that other developers have pushed to the remote repository since the last fetch and allows you to review and merge manually at a later time using Git Merge. As it doesn’t change the working directory or the staging area, it is safe to use.

The below illustration shows the working of the command git fetch. It fetches all the latest changes that have been made in the remote repository and lets us make changes accordingly.

image The command used is :

git fetch <branch_name> 16. Git Pull Remote Branch You can pull in any changes that have been made from your forked remote repository to the local repository.

As shown in the below image, using the git pull command, all the changes and content can be fetched from the remote repository and can be immediately updated in the local repository to match the content. image

We can simply pull a remote repository by using the git pull command. The syntax is as follows:

git pull This command is equivalent to

git fetch origin head Use the following command to check if there has been any change:

git pull If there is no change, it will show “Already up to date”. Else, it will simply merge those changes in the local repository.

Git Stash Sometimes in large codebases, there might be some cases when we do not want to commit our code, but at the same time don’t want to lose the unfinished code. This is where git stash comes into play. The git stash command is used to record the current state of the working directory and index in a stash.
It stores the unfinished code in a stash and cleans the current branch from any uncommitted changes. Now, we can work on a clean working directory.

If in the future, we again need to visit that code, we can simply use the stash and apply those changes back to the working repository.

As shown below, using the command git stash, we can temporarily stash the changes we have made on the working copy and can work on something else. Later, when needed, we can git stash pop and again start working on it. image How to stash changes in Git?

The syntax for stashing is as follows:

git stash Suppose, you are working on a website and the code is stored in a repository.

Now let's say, you have some files named design.css and design.js. Now you want to stash these files so that you can again use them later, while you work on something else.

Therefore, later you can use the git stash list command to view all the changes.
