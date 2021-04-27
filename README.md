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