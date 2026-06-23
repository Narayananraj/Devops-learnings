# Git Command Reference

> A complete file to reference for day to day Git work.

---

## Contents

1. [Git Basics](#-git-basics)
2. [Branching](#-branching)
3. [Staging & Commits](#-staging--commits)
4. [Working with Remotes](#-working-with-remotes)
5. [Logs & History](#-logs--history)
6. [Reverting & Resetting](#-reverting--resetting)
7. [Stash Management](#-stash-management)
8. [Tagging](#️-tagging)
9. [Config & SSH Setup](#️-config--ssh-setup)
10. [Git Ignore & Clean](#️-git-ignore--clean)
11. [Remote Management](#-remote-management)
12. [Submodules](#-submodules)
13. [Cherry-pick & Rebase](#-cherry-pick--rebase)
14. [Archive & Export](#-archive--export)
15. [Search & Grep](#-search--grep)
16. [Aliases](#️-aliases-time-savers)
17. [Conflict Resolution](#️-conflict-resolution)
18. [Maintenance & Inspection](#-maintenance--inspection)

---

## Git Basics

| Command | Purpose |
| :--- | :--- |
| `git init` | Initialize a new Git repository |
| `git status` | Show status of working directory and staging area |
| `git add <file>` | Add a specific file to the staging area |
| `git add .` | Add all changes in the current directory to staging |
| `git add -A` | Stage all changes (new, modified, deleted) repo-wide |
| `git add -p` | Interactively stage parts (hunks) of changes |
| `git commit -m "message"` | Commit staged changes with a message |
| `git commit --amend` | Modify the most recent commit |
| `git config --global user.name "Name"` | Set global username for commits |
| `git config --global user.email "email@example.com"` | Set global email for commits |
| `git --version` | Check the installed Git version |
| `git help <command>` | Show help for a specific command |
| `git rm <file>` | Remove a file from the working dir and stage the deletion |
| `git mv <old> <new>` | Rename/move a file and stage the change |

---

##  Branching

| Command | Purpose |
| :--- | :--- |
| `git branch` | List local branches |
| `git branch -a` | List all branches (local + remote) |
| `git branch <name>` | Create a new branch |
| `git checkout <name>` | Switch to a branch |
| `git checkout -b <name>` | Create and switch to a new branch |
| `git switch <name>` | Switch to a branch *(modern syntax)* |
| `git switch -c <name>` | Create and switch to a branch *(modern syntax)* |
| `git branch -d <name>` | Delete a branch (safe — blocks if unmerged) |
| ⚠️ `git branch -D <name>` | Force delete a branch even if unmerged |
| `git branch -m <new-name>` | Rename the current branch |
| `git merge <branch>` | Merge the specified branch into the current one |
| `git merge --no-ff <branch>` | Merge with a merge commit (no fast-forward) |
| `git merge --abort` | Abort an in-progress merge |

---

##  Staging & Commits

| Command | Purpose |
| :--- | :--- |
| `git add <file>` | Stage changes for commit |
| `git commit -m "message"` | Commit staged changes |
| `git commit -am "message"` | Stage and commit tracked files in one step |
| `git reset HEAD <file>` | Unstage a file |
| `git restore --staged <file>` | Unstage a file *(modern syntax)* |
| ⚠️ `git restore <file>` | Discard working-directory changes *(modern syntax)* |

---

##  Working with Remotes

| Command | Purpose |
| :--- | :--- |
| `git remote -v` | Show connected remotes |
| `git remote add origin <url>` | Add a new remote repo |
| `git push -u origin <branch>` | Push branch and set upstream tracking |
| `git push` | Push commits to the tracked remote branch |
| ⚠️ `git push --force-with-lease` | Force push safely (won't clobber others' work) |
| `git pull` | Fetch and merge changes from the remote |
| `git pull --rebase` | Fetch and rebase local commits on top |
| `git clone <url>` | Clone a remote repo locally |
| `git clone --depth 1 <url>` | Shallow clone (latest commit only) |

---

##  Logs & History

| Command | Purpose |
| :--- | :--- |
| `git log` | Show commit history |
| `git log --oneline` | Condensed one-line log |
| `git log --graph --oneline --all` | Visual branch graph |
| `git log -p` | Show commit history with diffs |
| `git log --author="Name"` | Filter commits by author |
| `git diff` | Show unstaged file differences |
| `git diff --staged` | Show staged differences |
| `git show <commit>` | Show details of a specific commit |
| `git blame <file>` | Show who last modified each line |
| `git reflog` | Show history of HEAD movements (your safety net) |

---

## Reverting & Resetting

| Command | Purpose |
| :--- | :--- |
| ⚠️ `git checkout -- <file>` | Discard changes in the working directory |
| `git revert <commit>` | Create a new commit that undoes the changes (safe) |
| `git reset --soft <commit>` | Move HEAD, keep changes staged |
| `git reset --mixed <commit>` | Move HEAD, keep changes unstaged *(default)* |
| ⚠️ `git reset --hard <commit>` | Move HEAD and discard all changes |

---

## Stash Management

| Command | Purpose |
| :--- | :--- |
| `git stash` | Stash current changes |
| `git stash -u` | Stash including untracked files |
| `git stash list` | List stashes |
| `git stash apply` | Apply latest stash (keep it in the list) |
| `git stash pop` | Apply latest stash and remove it from the list |
| ⚠️ `git stash drop` | Remove the latest stash |
| ⚠️ `git stash clear` | Remove all stashes |
| `git stash show -p` | Show contents of the latest stash |

---

## Tagging

| Command | Purpose |
| :--- | :--- |
| `git tag` | List tags |
| `git tag <name>` | Create a lightweight tag |
| `git tag -a <name> -m "msg"` | Create an annotated tag |
| `git push origin <tag>` | Push a tag to the remote |
| `git push origin --tags` | Push all tags to the remote |
| `git tag -d <name>` | Delete a local tag |
| ⚠️ `git push origin --delete <tag>` | Delete a remote tag |

---

## Config & SSH Setup

| Command | Purpose |
| :--- | :--- |
| `git config --list` | Show all current configs |
| `git config --global core.editor "code --wait"` | Set the default editor |
| `ssh-keygen -t ed25519 -C "email@example.com"` | Generate an SSH key *(recommended)* |
| `ssh-keygen -t rsa -b 4096 -C "email@example.com"` | Generate an RSA SSH key |
| `eval $(ssh-agent -s)` | Start the SSH agent |
| `ssh-add ~/.ssh/id_ed25519` | Add an SSH key to the agent |
| `ssh -T git@github.com` | Test the SSH connection to GitHub |

---

## Git Ignore & Clean

| Command | Purpose |
| :--- | :--- |
| `echo "filename" >> .gitignore` | Add a file to `.gitignore` |
| `git rm -r --cached <file>` | Stop tracking a file (keep it locally) |
| `git clean -n` | Preview untracked files to be removed (dry run) |
| ⚠️ `git clean -fd` | Remove untracked files and directories |
| ⚠️ `git clean -fx` | Remove untracked **and** ignored files/directories |

---

## Remote Management

| Command | Purpose |
| :--- | :--- |
| `git remote rename <old> <new>` | Rename a remote |
| `git remote remove <name>` | Remove a remote |
| `git remote set-url origin <url>` | Change a remote's URL |
| `git fetch <remote>` | Fetch changes from a remote |
| `git fetch --all` | Fetch changes from all remotes |
| `git fetch --prune` | Fetch and remove stale remote-tracking branches |
| `git remote show <name>` | Show detailed info about a remote |

---

## Submodules

| Command | Purpose |
| :--- | :--- |
| `git submodule add <repo-url>` | Add a submodule |
| `git submodule update --init --recursive` | Initialize and update submodules |
| `git submodule update --remote` | Update submodules to the latest remote commit |
| `git submodule status` | Show submodule status |
| `git submodule foreach <cmd>` | Run a command in each submodule |
| ⚠️ `git submodule deinit -f .` | Deinitialize all submodules |

---

## Cherry-pick & Rebase

| Command | Purpose |
| :--- | :--- |
| `git cherry-pick <commit>` | Apply a specific commit to the current branch |
| `git cherry-pick --abort` | Abort a cherry-pick in progress |
| `git rebase <branch>` | Reapply commits on top of another base tip |
| `git rebase -i HEAD~3` | Interactive rebase of the last 3 commits |
| `git rebase --continue` | Continue the rebase after resolving conflicts |
| `git rebase --skip` | Skip the current commit during rebase |
| `git rebase --abort` | Abort a rebase in progress |

---

## Archive & Export

| Command | Purpose |
| :--- | :--- |
| `git archive --format zip --output file.zip HEAD` | Export the current repo as a zip |
| `git archive --format tar --output file.tar HEAD` | Export the current repo as a tarball |
| `git bundle create repo.bundle --all` | Bundle the entire repo into one file |

---

## Search & Grep

| Command | Purpose |
| :--- | :--- |
| `git grep "text"` | Search for a string in the repo |
| `git grep -n "text"` | Search with line numbers |
| `git log -S"string"` | Find commits adding/removing a string |
| `git log --grep="text"` | Search commit messages |
| `git diff --stat` | Show a diff summary with file change counts |

---

## Aliases (Time-savers)

| Command | Purpose |
| :--- | :--- |
| `git config --global alias.st status` | Create `git st` for `git status` |
| `git config --global alias.ci commit` | Create `git ci` for `git commit` |
| `git config --global alias.co checkout` | Create `git co` for `git checkout` |
| `git config --global alias.br branch` | Create `git br` for `git branch` |
| `git config --global alias.lg "log --oneline --graph --all"` | Pretty graph log |

---

## Conflict Resolution

| Command | Purpose |
| :--- | :--- |
| `git status` | Show files with conflicts |
| `git diff` | See the conflicting changes |
| `git mergetool` | Launch the merge conflict tool |
| `git add <file>` | Mark a conflict as resolved |
| `git commit` | Complete the merge after resolving |
| `git merge --abort` | Abort the merge and reset to the pre-merge state |

---

## Maintenance & Inspection

| Command | Purpose |
| :--- | :--- |
| `git gc` | Clean up and optimize the repository |
| `git fsck` | Check repository integrity |
| `git count-objects -vH` | Show repo object/size stats |
| `git bisect start` | Begin a binary search for a buggy commit |
| `git bisect good <commit>` | Mark a commit as good during bisect |
| `git bisect bad <commit>` | Mark a commit as bad during bisect |
| `git bisect reset` | End the bisect session |
| `git worktree add <path> <branch>` | Check out a branch into a separate directory |
| `git worktree list` | List linked working trees |