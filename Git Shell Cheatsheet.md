# GitHub Cheatsheet
Cheatsheet to get you comfortable with the Git Shell

## Prerequisites
Material you need before you start working with the Git Shell

[GitHub Desktop (includes Git Shell)](https://github-windows.s3.amazonaws.com/GitHubSetup.exe)

---

### First time setup
Initial one-time setup for creating new *local repositories* and new *remotes*

##### 1. Creating a new *local repository*

1. Open Git Shell.
2. Change your current working directory to the one you want to be your new repository.

    ```
    $ cd <directory>
    ```

3. Initialize the current working directory as a local Git repository.

    ```
    $ git init
	# Initializes current workiing directory as a local Git repository.
    ```

---

##### 2. Creating a new *remote*

1. Make sure you have a remote repository on GitHub, or [create one here](https://help.github.com/articles/creating-a-new-repository).
2. Open Git Shell.
3. [Add the URL for the remote repository](https://help.github.com/articles/adding-a-remote) where your local repository should be pushed.

    ```
    $ git remote add origin <remote repository URL>
	# Sets the new remote.
    $ git remote -v
	# Verifies the new remote URL.
    ```

---
---

### Modifying existing *local repositories*
Make changes to repositories that already exist

##### 1.Switching to the right branch

+ Switch to an existing branch, or use `$ git branch <branch name>` to create a new one (and then use the `$ git checkout` command to switch to it).

    ```
    $ git checkout <branch name>
	# Switches to existing branch.
    ```

##### 2. Committing changes to a *local repository*

1. **Make sure you're working in the right branch before continuing with the following steps!**

2. Prepare to add new or changed files by staging them for the next commit. To stage the entire *local repository*, use `$ git add .`. To unstage a file, use `$ git reset HEAD <target>`.

    ```
    $ git add <target>
	# Stages the targeted files for the next commit.
    ```

3. Commit the files that you've staged in your *local repository*. To remove this commit, use `$ git reset --soft HEAD~1`. 

    ```
    $ git commit -m "Message"
	# Commits the tracked changes to the local repository and prepares them to be pushed to a remote repository.
    ```

---

### Pushing changes to *remote repository*
Update the *remote repository* to match your *local repository*

+ Push the changes from your *local repository* to the *remote repository*.

    ```
    $ git push <remote> <local branch>
	# Pushes the changes from the specified branch of your local repository to the the specified remote repository.
    ```

---

### Merging branches
**DO THIS ONLY WHEN BOTH BRANCHES ARE STABLE!**  
Incorporate changes from branch to branch

1. **Make sure the current working branch is the one *without* the newest changes. These changes will be incorporated from a specified branch!**

2. Merge branch into current working branch. (e.g. merging changes from `dev` branch into `master` branch)

    ```
    $ git merge <branch name>
	# Merges the specified branch into the current working branch.
    ```

---

### Pulling changes from *remote repository*
Update your *local repository* to match the *remote repository*

+ Pull the changes from the *remote repository* to your *local repository*.

    ```
    $ git pull <remote> <local branch>
	# Pulls the changes from the specified remote repository to the specified branch in your local repository.
    ```
	