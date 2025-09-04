# Working With Branches in Git and GitHub

There are two ways you can create and work with branches: Locally through Git, or remotely through a web-hosted Git repository like GitHub.

- [Working with Branches in GitHub](#working-with-branches-in-github)
- [Working with Branches in Git](#working-with-branches-in-git)


## Working with Branches in GitHub

The following describes how you work with branches in the GitHub web UI.

### Creating A Child Branch in GitHub

To create a branch in GitHub:

1. Log in to your GitHub account.
2. Go to your repository's main branch.
3. Click the dropdown menu for the main branch that's located under the repository's title. By default, the menu displays `main`.
4. In the entry field with the search icon, enter a name for your child branch.
5. On the `Branches` tab of the dropdown menu, click `Create branch <name of branch> from main`.
   **Result:** You're automatically connected to the child branch you've just created.
   Now, two branches are displayed in your repository.

**Next Steps:**
Add a file to the branch, and commit your changes. Then open a pull request (`Compare and Pull Request`), and merge your changes into the main branch. Then delete the child branch 


### Adding a File to a Child Branch in GitHub

**Prerequisite:** Check that the correct branch is displayed in the branch dropdown menu.

To add a file to a child branch in GitHub:
1. In the repository, click `Add file -> Create new file`.
2. Enter a name and extension for the file (for example, `Test.md`).
3. In the `Edit` view of the file, enter your text.
4. At the bottom of the page, in the `Commit new file` window, add a description of the changes you made to the file, and click the `Commit new file` button.
   **Result:** Your file is committed to the child branch.

**Next Step:** To add the file of the child branch to the main branch, open a pull request.

### Opening Pull Requests in GitHub

   **Prerequisite:** You're in the child branch and you're committed changes to it. On the `Code` or `Pull requests` tab, you get a highlighted message box about the last pushes (that is, committed changes).

1. In the message box about the last pushes, click the `Compare & pull request` button.
2. Check the changes that are displayed at the bottom of the page. 
3. Optional: Add a comment to the pull request.
4. Click the `Create pull request` button.
   Result: The pull request is created and ready to be merged by a repository administrator. For all the repositories that you create, you automatically have administrative rights.

### Merging Pull Requests in GitHub

1. On the `Pull Requests` tab of the corresponding branch, click the `Merge pull request` button.
2. Optional: Add a comment to the pull request in the `Add a comment` section. 
3. To merge the changes, click the `Confirm merge` button. 
   **Result:** You get a success message displaying `Pull request successfully merged and closed`. Your changes have been successfully incorporated into the main branch.

**Next Steps:** You can now delete the child branch.

### Deleting Branches in GitHub

**Prerequisite:** You've successfully merged a child branch into the main branch.

1. Go to the `Pull requests` tab of your main repository.
2. Select the `Delete branch` button that's displayed next to the message `Pull request successfully merged and closed`.
**Result:** The child branch is successfully deleted.


## Working with Branches in Git
To work with branches in your local Git repository, enter the git commands in a command-line tool.

<!--
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

-->

## Creating a Branch

1. Go to the folder you want to create a branch for using the `cd` command. For example: `cd FolderName`.
2. Create a new branch in your repository and give it a name (for example, MyBranch):
   `git branch MyBranch`
3. Activate and switch to the new branch:
   `git checkout MyBranch`
4. Verify you're in the right branch:
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

To revert changes after you've committed them, use the following command:
`git revert HEAD --no-edit` 

The shortcut HEAD rolls back the last commit. You could also specify the ID of your commit here.

## Merging Changes Into Another Branch

1. Switch to the main branch using the `git checkout`command:
   `git checkout master`
2. Merge the changes from MyBranch into Master:
   `git merge MyBranch`

    `git log`

Tip: To exit the `git log` command, press the "Q" key.

## Deleting a Branch

Once you've merged your changes to the main branch, it's best practice to delete the child branch.

`git branch -d MyBranch`
