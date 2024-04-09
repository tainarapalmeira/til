# Git Basics
- Git is a **version control system** that tracks and manages changes to files over time.
   - It's like a checkpoint where you save a game.

- A Git repository (repo) is a workspace that tracks and manages files within a folder.

- The basic Git workflow:
   1. Work on stuff - create new files, edit files, delete, etc.
   2. Add changes - group specific changes together in preparation for committing.
   3. Commit - commit everything that was previously added.

- `git add .` &rarr; will stage everything in the current directory.

- `git add --all` &rarr; will stage everything no matter which directory you are currently in.

## Git Commit
- Atomic Commit: When possible, a commit should encompass a single feature, change, or fix. In other words, try to **keep each commit focused on a single thing**. This makes it much easier to undo or rollback changes later on. It also makes your code or project easier to review.

- Commit messages: Describe your changes in imperative mode, e.g., *make xyz*, *fix abc*.

- Amending commits: By amending a commit, it's possible to add new changes to the last commit. It is not necessary to make a brand new commit. &rarr; `git commit --amend`

- Ignoring Files: It is possible to tell Git which files and directories to ignore in a given repository, using .gitignore file. Examples of files to be ignored by Git: Secrets, API keys, log files, operating system files, etc.

Some other useful commands to remember: `git log --oneline`

## Git Branch
- It is all about contexts: branches enable us to create separate contexts where we can try new things, or even work on multiple ideas in parallel.

- We are always working on one branch.

- Master branch: the default branch name when initializing a repo is master. It doesn't do anything special. It's just like any other branch. But, it is usually designated as the "official branch" of a codebase.

- HEAD: HEAD is simply a pointer that refers to the current "location" in your repo. It is possible to move the HEAD around.

- Some other useful commands to remember:
   - `git branch` &rarr; lists existing branches in the repository.
   - `git switch -c <branch-name>` or `git checkout -b <branch-name>` &rarr; creates and switches to the new branch
   - `git branch -m <new-branch-name>` &rarr; rename a branch
   - `git branch -d <branch-name>` &rarr; delete a branch
   - `git branch -D <branch-name>` &rarr; delete a branch forcefully


## Git Merge
- Merging: branching makes it easy to work within self contained contexts, but we often want to incorporate changes from one branch into another. We do this using git merge command.

- We merge branches, not specific commits.

- **We always merge to the current HEAD branch**.

- Fast-foward merge.

## Comparing changes with Git Diff
- We can use the `git diff` command to view changes between commits, branches, files, and working directories.

- `git diff` lists all the changes in our working directory that are **NOT** staged for the next commit. This means it compares the *staging area* and *working directory*. - What I could add to the *staging area* -

- `git diff HEAD` lists all changes in the working directory tree since the last commit. Therefore, it compares *staged* and *unstaged* work since HEAD.

- `git diff --stage` or `git diff --cache` will list the changes between the staging area and the last commit. - What will be included in my next commit if I run git commit right now. -

- Comparing branches: `git diff branch1..branch2`

## Git Stash
- Stashing: Git provides an easy way of stashing uncommitted changes so that we can return to them later without having to make unnecessary commits.

- Running `git stash` will take all uncommitted changes (*staged and unstaged*) and stash them, reverting the changes in the current working directory.
   - `git stash save` or just `git stash`

- `git stash pop` removes the most recently stashed changes from your stash and reapplies them to your working directory.

- Stash apply: git stash apply applies whatever is stashed away without removing it from the stash. This can be useful if you want to apply stashed changes to multiple branches.

- Some other useful commands to remember:
   git stash list
   git stash drop <stash-id> &rarr; delete a particular stash
   git stash clear &rarr; removes all the stash