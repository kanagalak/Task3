# Task3

### COMMIT (SO)
When you make a change to a file, you want to record the change. Commits are snapshots or save points within GIT Version Control which records these changes; basically a way if recording the a state of a program on a branch. When a commit is made, a code is made which is known as a SHA-1 hash. 

By using the command ****git commit**** this creates a snapshot of your repository (aka commit). Over time the commits made tell a story of the history of your repository and how you arrived at its current state. 

Commits are always stored in the the branch you are checkedout to, so it is best practice to run **git status** to confirm it is being stored in the correct location. You will also need to stage any new changes prior to the commit, which can be done with the **git add [file]** command.

## Undoing A Change
In the case a commit needs to be undone, there are two ways to do so - **git revert** and **git reset**. **git revert** is the preferred option as it undoes the change, acknowledges the change and keeps a record of the change. **git reset** on the other hand removes head and branch pointer (removes commit as well) and does not make a record. This option is usually avoided as it can result in loss of work/project. It is advised you discuss with your team before actioning this command.
