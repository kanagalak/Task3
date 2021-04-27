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


Adding Files 
 
Here we are going to look at how we add files on Git and what we need to do once we have added a file. 
When we want to add a file on Git there are two ways we can go about this. The first is by entering the command touch fileName.fileExtension (touch Newfile.txt) or you can enter the command echo > fileName.fileExtension (echo > Newfile.txt).  
Doing this adds the file but it becomes an untracked file which means you will not be able to track the changes made to the file. In order to turn it into a tracked file you must run a git status to confirm it is an untracked file (untracked files are in red) and then you must add the file using the following command git add fileName.fileExtension (git add Newfile.txt) Once this has been done git will confirm that these changes are set to be committed and the files should be coloured green as shown below.  
Renaming, copying and deleting files 
I will now show the commands for renaming, copying and deleting a file. 
 
Renaming  
Mv fileName.fileExtension NewFileName.FileExtension 
Ren fileName.fileExtension NewFileName.FileExtension 
Copying  
Cp fileName.fileExtension fileCopy.fileExtension 
Copy-Item fileName.fileExtension 
Copy-item fileName.fileExtension fileCopy.FileExtension 
Deleting 
Rm fileName.fileExtension 
Del fileName.fileExtension 