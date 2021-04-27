# Task3

### COMMIT (SO)
When you make a change to a file, you want to record the change. Commits are snapshots or save points within GIT Version Control which records these changes; basically a way if recording the a state of a program on a branch. When a commit is made, a code is made which is known as a SHA-1 hash. 

By using the command ****git commit**** this creates a snapshot of your repository (aka commit). Over time the commits made tell a story of the history of your repository and how you arrived at its current state. 

Commits are always stored in the the branch you are checkedout to, so it is best practice to run **git status** to confirm it is being stored in the correct location. You will also need to stage any new changes prior to the commit, which can be done with the **git add [file]** command.

In the case a commit needs to be undone, there are two ways to do so - **git revert** and **git reset**. **git revert** is the preferred option as it undoes the change, acknowledges the change and keeps a record of the change. **git reset** on the other hand removes head and branch pointer (removes commit as well) and does not make a record. This option is usually avoided as it can result in loss of work/project. It is advised you discuss with your team before actioning this command.


# Using GIT Efficiently

## Git workflows
Whenever multiple developers are involved in a project it is necessary to use the right workflow for Git
The Main Branch should always have a copy of the exiting code in Production.

### Best practices:

1. One developer has to create an empty develop branch locally and push it to the server.
...git branch develop
...git push -u origin develop
...Other developers will clone the central repository 

2. Feature branches should never interact directly with Main branch.  So each feature branch should reside in its own branch
Make a new feature branch off develop 
...git branch feature1

3. Switch to feature branch 
...git checkout feature1

4.  Make any changes like adding  or editing file

5. Stage the changes using
...git add filename.

6. Commit the changes locally using
...git commit 

7. Repeat the above steps 3,4,5,6 if need more changes.

8. Switch to develop branch using
--git checkout develop

9.  Merge changes into develop 
...git merge origin feature1 

10.  If there is any conflict pull the latest code from develop branch through
...git pull
Resolves all the conflicts and merge into develop branch

11. Once code reviews and testing are done push into the main branch using
...git push 

12.  Delete feature branch if necessary using 
...git branch -d feature1

### Example
git checkout master
git checkout -b develop
git checkout -b feature_branch
### work happens on feature branch
git checkout develop
git merge feature_branch
git checkout master
git merge develop
git branch -d feature_branch

# Task3

### COMMIT (SO)
When you make a change to a file, you want to record the change. Commits are snapshots or save points within GIT Version Control which records these changes; basically a way if recording the a state of a program on a branch. When a commit is made, a code is made which is known as a SHA-1 hash. 

By using the command ****git commit**** this creates a snapshot of your repository (aka commit). Over time the commits made tell a story of the history of your repository and how you arrived at its current state. 

Commits are always stored in the the branch you are checkedout to, so it is best practice to run **git status** to confirm it is being stored in the correct location. You will also need to stage any new changes prior to the commit, which can be done with the **git add [file]** command.

In the case a commit needs to be undone, there are two ways to do so - **git revert** and **git reset**. **git revert** is the preferred option as it undoes the change, acknowledges the change and keeps a record of the change. **git reset** on the other hand removes head and branch pointer (removes commit as well) and does not make a record. This option is usually avoided as it can result in loss of work/project. It is advised you discuss with your team before actioning this command.

