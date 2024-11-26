
# Basic Git Usage Guide

This guide covers the basic Git commands that are commonly used when working with Git repositories. It assumes that Git is already installed on your system.

---

## 1. **Configuring Git**

Before you start using Git, you need to set your name and email address. This information is included in each commit you make.

### Set Your Name and Email:

```bash
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```

The `--global` flag makes these settings apply to all repositories. If you want to set them for a specific repository, omit the `--global` flag and run the commands inside the repository.

---

## 2. **Creating a New Repository**

To create a new Git repository, follow these steps:

### Initialize a New Repository:

```bash
git init
```

This creates a new `.git` directory in the current directory, which allows Git to track changes.

### Clone an Existing Repository:

```bash
git clone <repository-url>
```

This will create a local copy of the repository in your current directory.

---

## 3. **Staging Changes**

Before committing any changes, you need to stage them. This tells Git which files you want to include in your next commit.

### Stage a Specific File:

```bash
git add <file_name>
```

### Stage All Changed Files:

```bash
git add .
```

This will stage all files that have been modified or created.

---

## 4. **Committing Changes**

Once your changes are staged, you can commit them to the local repository. Each commit should have a message describing the changes.

### Commit with a Message:

```bash
git commit -m "Your commit message"
```

### View Commit History:

```bash
git log
```

This will display the commit history for the current branch.

---

## 5. **Pushing Changes**

If you're working with a remote repository (e.g., GitHub), you'll need to push your commits to the remote repository.

### Push Changes to Remote Repository:

```bash
git push origin <branch_name>
```

The `origin` is the default name of the remote repository, and `<branch_name>` is usually `main` or `master`.

---

## 6. **Pulling Changes**

To update your local repository with changes made to the remote repository, use the pull command.

### Pull Changes from Remote Repository:

```bash
git pull origin <branch_name>
```

This will fetch and merge changes from the remote repository into your local branch.

---

## 7. **Branching**

Branches allow you to work on different features or fixes without affecting the main project.

### Create a New Branch:

```bash
git branch <branch_name>
```

### Switch to a Different Branch:

```bash
git checkout <branch_name>
```

### Create and Switch to a New Branch:

```bash
git checkout -b <branch_name>
```

### List All Branches:

```bash
git branch
```

---

## 8. **Merging Branches**

Once you’ve finished working on a branch, you can merge it back into the main branch (or any other branch).

### Merge a Branch into the Current Branch:

```bash
git merge <branch_name>
```

This will bring the changes from `<branch_name>` into your current branch.

---

## 9. **Viewing Differences**

You can see what changes have been made before committing by using the following commands.

### View Changes in Staged Files:

```bash
git diff --cached
```

### View Changes in Unstaged Files:

```bash
git diff
```

---

## 10. **Undoing Changes**

If you make a mistake or want to undo changes, there are several ways to do it.

### Unstage a File (after `git add`):

```bash
git reset <file_name>
```

### Discard Changes in a File (after `git add` or without staging):

```bash
git checkout -- <file_name>
```

### Undo Last Commit (keep changes staged):

```bash
git reset --soft HEAD~1
```

---

## 11. **Git Ignore**

To avoid committing unnecessary files (e.g., build files or editor backups), you can create a `.gitignore` file to specify which files or directories Git should ignore.

### Example `.gitignore`:

```
# Ignore Mac system files
.DS_Store

# Ignore node_modules folder
node_modules/

# Ignore build output
build/
```

---

## Conclusion

These are the basic Git commands to help you get started with version control. Git is a powerful tool, and as you grow more comfortable with it, you’ll discover many more advanced features to help you manage your code.

---

**Resources:**
- [Git Documentation](https://git-scm.com/doc)
- [Pro Git Book](https://git-scm.com/book/en/v2)
