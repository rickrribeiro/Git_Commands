Git Commands
============
___

_A list with some Git commands and example configs_

--

### Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |
| `git restore --staged *` | Remove added files from staging area |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] [commit hash]` | Create a new branch in a specific commit and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git branch -m [old branch name] [new branch name]` | Rename a local branch |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |
| `git revert [commit hash]` | Revert the commit |
| `git revert -n [branch]~[x]..[branch]~[y]` | Revert the changes done by commits from the [x] last commit in master (included) to the [y] last commit in master (included) |
### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |


### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git log --oneline` | View changes (briefly) |
| `git diff [source branch] [target branch]` | Preview changes before merging |

### Configs & meta

| Command | Description |
| ------- | ----------- |
| `git config` | Change or view git configs |
| `git config --global user.name [NAME]` | Configure git username |
| `git config --global user.email [EMAIL]` | Configure git email |
| `git update-index ` | Register file contents in the working tree to the index |
| `git update-index --chmod (+|-)x [FILENAME]` | Add or remove permission to execute file ex: permission error on travis |

### Git Flow Feature

| Command | Description |
| ------- | ----------- |
| `git flow init` | Initialize git flow |
| `git flow feature start [FEATURE_NAME]` | Create a new feature |
| `git flow feature publish [FEATURE_NAME]` | Publish the feature |
| `git flow feature finish [FEATURE_NAME]` | Merges the feature into main and finish it |
| `git flow feature pull origin [FEATURE_NAME]` | Make a pull request |

### Git Flow Release

| Command | Description |
| ------- | ----------- |
| `git flow release start [RELEASE]` | Create a release |
| `git flow release publish` | Publish the release |
| `git flow release finish` | Merges the release into main, tag it and finish it |

### Git Flow Hotfix

| Command | Description |
| ------- | ----------- |
| `git flow hotfix start [NAME]` | Create a hotfix |
| `git flow hotfix finish [NAME]` | Publish the release |

### Git SubModules

| Command | Description |
| ------- | ----------- |
| `git submodule add [URL] path` | Add a submodule |
| `git submodule init` | Init submodules configuration file |
| `git submodule update` | Fetch all submodules project data |
| `git clone --recurse-submodules [REPO]` | Clones The project with submodules |
| `git submodule update --init --recursive` | update and init |
--- to add a submodule as a package, add to package.json "pakage-name": "file:.submodules/pakage-name",
