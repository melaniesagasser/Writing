# Working With Branches in Git and GitHub

There are two ways you can create and work with branches: Locally through Git, or remotely through a web-hosted Git repository like GitHub.

- [Working with Branches in GitHub](#working-with-branches-in-github)
- [Working with Branches in Git](#working-with-branches-in-git)


## Working with Branches in GitHub

The following describes how you work with branches in the GitHub web UI.

### Creating A Child Branch 

To create a branch in GitHub:

1. Log in to your GitHub account.
2. Go to the repository for which you want to create a branch. Make sure you're on the `Code` tab of the repository.
3. Check that the branch menu that's located under the repository's title shows the main branch. By default, the main branch is called `main` unless you've renamed it. If you're not on the main branch, select the main branch from the branch menu.
4. Click the branch menu to open the `Switch branches/tags` dropdown menu. In the entry field with the search icon, enter a name for your child branch.
5. On the `Branches` tab of the dropdown menu, click `Create branch <name of branch> from main`.

   **Result:** You're automatically connected to the child branch you've just created.
   Now, two branches are displayed in your repository.

### Adding a File to a Child Branch 

**Prerequisite:** Check that the correct branch is displayed in the branch dropdown menu.

To add a file to a child branch in GitHub:
1. In the repository, select `Add file -> Create new file`.
2. Enter a name and extension for the file (for example, `Test.md`).
3. In the `Edit` view of the file, enter your text.
4. At the bottom of the page, in the `Commit new file` window, add a description of the changes you made to the file, and click the `Commit new file` button.

   **Result:** Your file is committed to the child branch.

**Next Step:** To add the file of the child branch to the main branch, open a pull request.

### Opening a Pull Request

   **Prerequisite:** You're in the child branch and you're committed changes to it. On the `Code` or `Pull requests` tab, you get a highlighted message box about the last pushes (that is, committed changes).

To open a pull request in GitHub:
1. In the message box about the last pushes, click the `Compare & pull request` button.
2. Check the changes that are displayed at the bottom of the page. 
3. Optional: Add a comment to the pull request.
4. Click the `Create pull request` button.

   **Result:** The pull request is created and ready to be merged by a repository administrator. For all the repositories that you create, you automatically have administrative rights.

### Merging Pull Requests

To merge pull requests in GitHub:
1. On the `Pull Requests` tab of the corresponding branch, click the `Merge pull request` button.
2. Optional: Add a comment to the pull request in the `Add a comment` section. 
3. To merge the changes, click the `Confirm merge` button. 

   **Result:** You get a success message displaying `Pull request successfully merged and closed`. Your changes have been successfully incorporated into the main branch.

**Next Steps:** You can now delete the child branch.

### Deleting Branches

**Prerequisite:** You've successfully merged a child branch into the main branch.

To delete a branch in GitHub:
1. Go to the `Pull requests` tab of your main repository.
2. Select the `Delete branch` button that's displayed next to the message `Pull request successfully merged and closed`.

**Result:** The child branch is successfully deleted.


## Working with Branches in Git
To work with branches in your local Git repository, enter the git commands in a command-line tool.

<!--
### Creating a New Local Repository

1. Create a new local repository:
   `mkdir <name of new repository>`
2. Go into the new repository:
   `cd <name of new repository>`
3. Initiate the new directory as a git repository by using the git init command:
   `git init`
   This initiates a local git repository with a .git folder containing all the git files. 
4. Verify that the new repo has been initialized:
   `ls -la .git`

### Creating and Adding a File to the Local Repository

1. Create a new empty file:
   `touch <name of new file>`
2. Add this file to the repository:
   `git add <name of new file>`

### Committing Your Changes

Commit your changes and add a message:
`git commit -m "Added <name of new file>"

-->

### Creating a Branch 

To create a branch in Git:
1. In the command line tool, go to the folder you want to create a branch for using the `cd` command. For example: `cd <name of folder>`.
2. Create a new branch in your repository and give it a name:
   `git branch <name of child branch>`
3. Activate and switch to the new branch:
   `git checkout <name of child branch>`
4. Verify you're in the right branch:
   `git branch`

   The branch that is highlighted with an asterisk is the active branch.

**Note:** As a shortcut, you can create and navigate to a new branch in one go:
`git checkout -b <name of child branch>`

### Adding Files to Your Branch 

To add a file to your branch in Git and add text to it in one go:
1. Add the text for your new file using the command `echo`:
   `echo "This is the first line in my new file." >> <name of new file>`
2. Verify the changes:
   `cat <name of new file>`

### Verifying the Status of Your Files

Use the `git status` command to verify the current status of files in your repository.

### Adding All Modifications and Additions to the Staging Area

To make all files and changes ready to be committed, enter the `git add *` command as a shortcut.
Then use `git commit -m "My Message"` to commit your changes.

### Reverting Committed Changes

To revert changes after you've committed them, use the following command:
`git revert HEAD --no-edit` 

The shortcut HEAD rolls back the last commit. You could also specify the ID of your commit instead.

### Merging Changes Into the Main Branch

To merge the changes to your child branch into the main branch:
1. Switch to the main branch using the `git checkout` command:
   `git checkout master`
2. Merge the changes from the child branch into the main branch:
   `git merge <name of child branch>`
3. Enter `git log` to get more information about the last changes.

**Tip:** To exit the `git log` command, press the "Q" key.

### Deleting a Branch

Once you've merged your changes to the main branch, it's best practice to delete the child branch.

To delete a branch, use the `git branch -d <name of child branch>` command.
