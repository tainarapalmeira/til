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

- Amending commits: By amending a commit, it's possible to add new changes to the last commit. It is not necessary to make a brand new commit.

Some useful commands to remember: `git log --oneline`
