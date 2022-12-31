# GIT CHEAT SHEET

## _A list of commonly used Git commands_

---

### SETUP & Configuring user information

| Command                                      | Description                                                            |
| -------------------------------------------- | ---------------------------------------------------------------------- |
| `git config --global user.name "[Username]"` | set a name that is identifiable for credit when review version history |
| `git config --global user.email "[Email]"`   | set an email address that will be associated with each history marker  |
| `git config --global color.ui auto`          | set automatic command line coloring for Git for easy reviewing         |

### Configuring user information, initializing and cloning repositories

| Command           | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| `git init`        | Initialize a local Git repository                            |
| `git clone [url]` | retrieve an entire repository from a hosted location via URL |

### Working with snapshots and the Git staging area

| Command                             | Description                                                           |
| ----------------------------------- | --------------------------------------------------------------------- |
| `git status`                        | show modified files in working directory, staged for your next commit |
| `git add [file-name.txt]`           | Add a file to the staging area                                        |
| `git add -A`                        | Add all new and changed files to the staging area                     |
| `git reset [file]"`                 | unstage a file while retaining the changes in working directory       |
| `git diff`                          | diff of what is changed but not staged                                |
| `git diff --staged`                 | diff of what is staged but not yet commited                           |
| `git commit -m "[commit message]"`  | Commit changes                                                        |
| `git rm -r [file-name.txt]`         | Remove a file (or folder)                                             |
| `git mv [existing-path] [new-path]` | change an existing file path and stage the move                       |

### Branching & Merging

| Command                                              | Description                                             |
| ---------------------------------------------------- | ------------------------------------------------------- |
| `git branch`                                         | List branches (the asterisk denotes the current branch) |
| `git branch -a`                                      | List all branches (local and remote)                    |
| `git branch [branch name]`                           | Create a new branch                                     |
| `git branch -d [branch name]`                        | Delete a branch                                         |
| `git push origin --delete [branch name]`             | Delete a remote branch                                  |
| `git checkout -b [branch name]`                      | Create a new branch and switch to it                    |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it                  |
| `git branch -m [old branch name] [new branch name]`  | Rename a local branch                                   |
| `git checkout [branch name]`                         | Switch to a branch                                      |
| `git checkout -`                                     | Switch to the branch last checked out                   |
| `git checkout -- [file-name.txt]`                    | Discard changes to a file                               |
| `git merge [branch name]`                            | Merge a branch into the active branch                   |
| `git merge [source branch] [target branch]`          | Merge a branch into a target branch                     |

### INSPECT & COMPARE Examining logs, diffs and object information

| Command                                    | Description                                                  |
| ------------------------------------------ | ------------------------------------------------------------ |
| `git log`                                  | show the commit history for the currently active branch      |
| `git log --stat -M`                        | show all commit logs with indication of any paths that moved |
| `git log --summary`                        | View changes (detailed)                                      |
| `git log --oneline`                        | View changes (briefly)                                       |
| `git log branchB..branchA`                 | show the commits on branchA that are not on branchB          |
| `git log --follow [file]`                  | show the commits that changed file, even across renames      |
| `git show [SHA]`                           | show any object in Git in human-readable format              |
| `git diff [source branch] [target branch]` | Preview changes before merging                               |

### Sharing & Updating Projects

| Command                                                                           | Description                                                 |
| --------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| `git push origin [branch name]`                                                   | Push a branch to your remote repository                     |
| `git push -u origin [branch name]`                                                | Push changes to remote repository (and remember the branch) |
| `git push`                                                                        | Push changes to remote repository (remembered branch)       |
| `git push origin --delete [branch name]`                                          | Delete a remote branch                                      |
| `git fetch`                                                                       | fetch down all the branches from that Git remote            |
| `git pull`                                                                        | Update local repository to the newest commit                |
| `git pull origin [branch name]`                                                   | Pull changes from remote repository                         |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git`     | Add a remote repository                                     |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH                     |

### logs /_.notes pattern_/, Save a file with desired paterns as .gitignore with either direct string matches or wildcard globs.

| Command                                        | Description                                          |
| ---------------------------------------------- | ---------------------------------------------------- |
| `git config --global core.excludesfile [file]` | system wide ignore patern for all local repositories |

### REWRITE HISTORY Rewriting branches, updating commits and clearing history

| Command                     | Description                                                    |
| --------------------------- | -------------------------------------------------------------- |
| `git rebase [branch]`       | apply any commits of current branch ahead of specified one     |
| `git reset --hard [commit]` | clear staging area, rewrite working tree from specified commit |

### TEMPORARY COMMITS, Temporarily store modified, tracked files in order to change branches

| Command           | Description                                 |
| ----------------- | ------------------------------------------- |
| `git stash`       | Stash changes in a dirty working directory  |
| `git stash clear` | Remove all stashed entries                  |
| `git stash list`  | list stack-order of stashed file changes    |
| `git stash pop`   | write working from top of stash stack       |
| `git stash drop`  | discard the changes from top of stash stack |
