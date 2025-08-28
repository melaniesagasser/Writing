# Cheat Sheet: Working With Branches in Git

## Creating a New Local Repository
1. Create a new local repository:
   `mkdir NewRepo`
2. Go into the new repository:
   `cd NewRepo`
3. Initiate the NewRepo directory as a git repository by using the git init command:
   `git init`
   This initiates a local git repository with a .git folder containing all the git files. 
4. Verify that the new repo has been initialized:
   `ls -la .git`

## Creating and Adding a File to the Local Repository
1. Create a new empty file:
   `touch newfile`
2. Add this file to the repository:
   `git add newfile`

## Committing Your Changes
Commit your changes and add a message:
`git commit -m "Added newfile"

## Creating a Branch
1. Create a new branch in your repository:
   `git branch MyBranch`
2. Switch to the new branch:
   `git checkout MyBranch`
3. Verify you're in the right branch:
   `git branch`
   Note: The branch that is highlighted with an asterisk is the active branch.
**Note:** As a shortcut, you can create and navigate to a new branch in one go:
`git checkout -b MyBranch`

## Making Changes in Your Branch Through Git
1. Add the text for your new file using the command `echo`:
   `echo "This is the first line in my newfile." >> newfile
2. Verify the changes:
   `cat newfile`

## Verifying the Status of Your Files
Use the `git status` command to verify the current status of files in your repository.

## Adding All Modifications and Additions to the Staging Area
Use `git add *` as a shortcut to make all files and changes ready to be committed.
Then use `git commit -m "My Message"` to commit your changes.

## Reverting Committed Changes
`git revert HEAD --no-edit` The shortcut HEAD rolls back the last commit. You could also specify the ID of your commit here.

## Merging Changes Into Another Branch
1. Switch to the main branch using the `git checkout`command:
   `git checkout master`
2. Merge the changes from NewBranch into Master:
   `git merge NewBranch`

    `git log`

Tip: To exit the `git log` command, press the "Q" key.

## Deleting a Branch
`git branch -d NewBranch`