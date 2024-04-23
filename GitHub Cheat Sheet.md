# GitHub Command Cheat Sheet

## Basic Commands

- **Clone a Repository**: `git clone <repository_url>`
  - Clones a repository from a remote location to your local machine. This creates a copy of the repository, including all branches and commit history, on your local file system.

- **Initialize Repository**: `git init`
  - Initializes a new Git repository in the current directory. This creates a hidden `.git` directory where Git stores all the information about the repository, such as commits, branches, and configurations.

- **Add Files**: `git add <file_name>` or `git add .`
  - Adds one or more files to the staging area. The staging area is where you prepare changes to be committed to the repository. You can specify individual files or use `.` to add all changes in the current directory.

- **Commit Changes**: `git commit -m "Commit message"`
  - Commits staged changes to the local repository. Each commit represents a snapshot of the repository at a specific point in time. You must provide a commit message describing the changes made in the commit.

- **Push Changes**: `git push origin <branch_name>`
  - Pushes committed changes from the local repository to a remote repository. The `origin` refers to the default remote repository, and `<branch_name>` specifies the branch to push changes to. This command updates the remote repository with your local changes.

- **Fetch Changes**: `git fetch` (`git fetch --all`)
  - Fetches changes from the remote repository without merging them into the local branch. This command updates the local repository's knowledge of the remote repository's branches and commits.

- **Pull Changes**: `git pull`
  - Fetches changes from the remote repository and merges them into the current branch. This command is equivalent to running `git fetch` followed by `git merge`. It updates your local repository with changes from the remote repository.

## Branching

- **Create Branch**: `git branch <branch_name>`
  - Creates a new branch with the specified name. Branches allow you to work on different features or versions of your project independently. After creating a branch, you can switch to it using the `git checkout` command.

- **Switch Branch**: `git checkout <branch_name>`
  - Switches to the specified branch. You can use this command to navigate between different branches in your repository. Any changes you make will be applied to the currently checked out branch.

- **Merge Branch**: `git merge <branch_name>`
  - Merges changes from the specified branch into the current branch. This command combines the commit histories of the two branches and applies the changes to the current branch.

- **Delete Branch**: `git branch -d <branch_name>`
  - Deletes the specified branch. This command removes the branch from your local repository. Note that you cannot delete the currently checked out branch.

- **Rename Branch**: `git branch -m <old_branch_name> <new_branch_name>`
  - Renames the specified branch. This command changes the name of the branch without affecting its commit history or contents.

- **List Branches**: `git branch`
  - Lists all branches in the repository. This command displays both local and remote branches. The currently checked out branch is indicated with an asterisk (`*`).

- **List Remote Branches**: `git branch -r`
  - Lists remote branches in the repository. Remote branches are branches stored on the remote repository server.

- **List All Branches**: `git branch -a`
  - Lists all branches, including both local and remote branches.

- **Show Current Branch**: `git branch --show-current`
  - Displays the name of the currently checked out branch.

## Remote Repositories

- **Add Remote**: `git remote add <name> <repository_url>`
  - Adds a new remote repository with the specified name and URL. Remote repositories are versions of your project hosted on a server, such as GitHub or GitLab.

- **Remove Remote**: `git remote remove <name>`
  - Removes the specified remote repository from your local repository. This command detaches the remote repository from your local repository, but it does not delete any files.

- **Rename Remote**: `git remote rename <old_name> <new_name>`
  - Renames the specified remote repository. This command changes the name of the remote repository in your local repository's configuration.

- **Show Remote Information**: `git remote show <name>`
  - Displays information about the specified remote repository, such as its URL and branches.

## Undoing Changes

- **Discard Changes in Working Directory**: `git checkout -- <file_name>`
  - Discards changes to the specified file in the working directory. This command reverts the file to its state in the last commit.

- **Undo Commit**: `git reset HEAD~1`
  - Undoes the last commit, keeping changes in the working directory. This command removes the last commit from the commit history, but it does not delete any files.

- **Revert Commit**: `git revert <commit_id>`
  - Creates a new commit that undoes changes made in a previous commit. This command adds a new
## Viewing Information

- **View Status**: `git status`
  - Displays the current status of the working directory and staging area. This command shows which files have been modified, added, or deleted since the last commit.

- **View Commit History**: `git log`
  - Displays a chronological list of commits in the repository. This command shows the commit message, author, date, and commit hash for each commit.

- **View Differences**: `git diff`
  - Shows the differences between the working directory and the staging area. This command highlights lines that have been added, modified, or deleted.

- **View Remote URLs**: `git remote -v`
  - Displays the URLs of remote repositories associated with the local repository. This command shows both fetch and push URLs for each remote.

- **Show Staged Changes**: `git diff --staged`
  - Shows the differences between the staging area and the last commit. This command highlights changes that have been staged but not yet committed.

## Stashing Changes

- **Stash Changes**: `git stash`
  - Temporarily saves changes in the working directory and staging area. This command allows you to switch to another branch or apply other changes without committing the current changes.

- **List Stashes**: `git stash list`
  - Lists all stashed changes in the repository. This command shows the stash number, branch, and message for each stash.

- **Apply Stash**: `git stash apply`
  - Applies the most recent stash to the working directory and staging area. This command restores the stashed changes without removing them from the stash list.

- **Apply Specific Stash**: `git stash apply stash@{<stash_number>}`
  - Applies a specific stash to the working directory and staging area. This command allows you to choose which stash to apply based on its index in the stash list.

- **Clear Stash**: `git stash clear`
  - Removes all stashed changes from the stash list. This command permanently deletes all saved stashes and cannot be undone.

## Tagging

- **Create Tag**: `git tag <tag_name>`
  - Creates a lightweight tag at the current commit. Tags are used to mark specific points in the commit history, such as release versions or milestones.

- **Create Annotated Tag**: `git tag -a <tag_name> -m "Tag message"`
  - Creates an annotated tag with a message at the current commit. Annotated tags include additional metadata, such as the tagger's name and email, and are recommended for release versions.

- **Push Tags**: `git push --tags`
  - Pushes all tags from the local repository to the remote repository. This command synchronizes tags between the local and remote repositories.

- **List Tags**: `git tag`
  - Lists all tags in the repository. This command displays both lightweight and annotated tags, sorted alphabetically.

## Miscellaneous

- **Undo Last Commit But Keep Changes**: `git reset --soft HEAD~1`
  - Undoes the last commit while keeping changes in the working directory and staging area. This command resets the current branch to the previous commit without modifying the working directory.

- **Show Git Version**: `git --version`
  - Displays the version of Git installed on your system. This command shows the Git version number and any additional information, such as the build date.

- **Show Git Configuration**: `git config --list`
  - Displays the configuration settings for Git on your system. This command shows both global and local configuration options, such as user name, email, and aliases.

- **Show Git Help**: `git --help`
  - Displays the Git help documentation. This command shows a list of available Git commands and options, along with brief descriptions and usage examples.
