# Git and GitHub Overview

## Agenda
- What is a File System?
- What is Version Control?
- File System vs. Version Control System
- CVCS vs. DVCS
- What is Git?
- Why Use Git?
- Git Stages
- Basic Git Commands
- Practice of Git
- What is GitHub?
- Git vs. GitHub
- Creating a Repository on GitHub
- Collaborating on GitHub
- Branching and Merging
- Best Practices
- Any Questions

---

## What is a File System?

**Definition:**  
A file system is a method and data structure that an operating system uses to manage files on a disk or partition (Normal File & Folder).

**Key Functions:**
- Organizes files and directories.
- Manages file storage and retrieval.
- Controls access and permissions.

## What is Version Control?

**Definition:**  
A tool that helps you manage changes to files over time.

**Purpose:**  
Tracks history, manages project versions, and facilitates collaboration among developers.

**Example:**  
Version control system.

## File System vs. Version Control System

### File System:
- **Storage:** Files are stored and organized in directories.
- **Versioning:** No inherent version control; changes overwrite existing files.
- **Collaboration:** Limited collaboration features; users must manually manage file versions.
- **Backup:** Requires external tools for version history and backups.

### Version Control System (VCS):
- **Storage:** Tracks changes to files and maintains a history of those changes.
- **Versioning:** Allows you to revert to previous versions and compare changes over time.
- **Collaboration:** Facilitates collaboration by managing simultaneous changes from multiple contributors.
- **Backup:** Automatically maintains a history of changes, serving as a backup.

## CVCS vs. DVCS

### Centralized Version Control Systems (CVCS):
- **Example:** Subversion (SVN).
- **Central Server:** All versions are stored on a single central server.
- **Dependency:** Requires access to the central server for most operations.
- **Collaboration:** Developers work on the same repository, which can lead to bottlenecks if the server is down.

### Distributed Version Control Systems (DVCS):
- **Example:** Git, Mercurial.
- **Local Repositories:** Each developer has a complete copy of the repository, including its full history.
- **Offline Work:** Developers can commit changes, create branches, and perform other operations without needing a central server.
- **Collaboration:** Changes can be merged from multiple repositories, offering more flexibility.

## What is Git?
![git](../assets/git_&_github/git.png)


Git is a distributed version control system designed to track changes in source code during software development. It allows multiple developers to work on a project simultaneously, offering robust features for branching and merging.

## Why Use Git?

- **Version Control:** Git tracks changes in your project, allowing you to revert to previous states and see the history of modifications.
- **Collaboration:** Git enables multiple developers to work on the same project without conflicts.
- **Backup:** Git stores your code in a way that it can be recovered even if something goes wrong.

## Git Stages

1. **Working Directory:**
   - **Description:** Where you modify files in your project.
   - **Stage:** Untracked or modified files that haven’t been staged yet.

2. **Staging Area (Index):**
   - **Description:** A snapshot of your changes, ready to be committed.
   - **Stage:** Files added with `git add` are moved here, preparing them for the next commit.

3. **Local Repository:**
   - **Description:** Where committed changes are stored in your local `.git` directory.
   - **Stage:** Files move here when you run `git commit`, creating a record in your project's history.

4. **Remote Repository:**
   - **Description:** A repository hosted on a remote server (like GitHub).
   - **Stage:** Changes are pushed here with `git push`, making them accessible to others.

## Basic Git Commands

- `git init`: Initializes a new Git repository in your project.
- `git clone`: Creates a copy of an existing repository.
- `git add`: Stages changes to be included in the next commit.
- `git commit`: Saves your staged changes to the local repository.
- `git push`: Uploads your local commits to a remote repository.
- `git pull`: Fetches and merges changes from a remote repository into your local repository.
- `git status`: Displays the state of the working directory and staging area.
- `git branch`: Lists all branches in the repository.
- `git checkout <branch_name>`: Switches to the specified branch.
- `git merge <branch_name>`: Merges the specified branch into the current branch.
- `git log`: Displays a log of commits.
- `git revert <commit>`: Creates a new commit that undoes the changes from a previous commit.
- `git remote`: Work on URLs of remote repositories.
- `git rm <file>`: Removes a file from the working directory and stages the removal.
- `git diff`: Shows the differences between files in the working directory and the staging area.

## Practice of Git

Practical exercises and examples for mastering Git.

## What is GitHub?
![github](../assets/git_&_github/github.png)

GitHub is a web-based platform that hosts Git repositories, enabling collaboration and version control in the cloud.

**Features:**
- Repository hosting for your code.
- Tools for managing pull requests, issues, and project discussions.
- Continuous integration and deployment options.
- A community platform for sharing and discovering open-source projects.

## Git vs. GitHub

- **Git:** A version control tool that manages changes in your source code.
- **GitHub:** A platform built on top of Git, offering additional features for collaboration, repository hosting, and community engagement.

## Creating a Repository on GitHub

Step-by-step guide to creating a repository on GitHub.

## Collaborating on GitHub

- **Forking:** Create a copy of a repository to work on independently.
- **Pull Requests:** Propose changes to a repository by submitting a pull request.
- **Push Requests:** Submit changes to a remote repository.
- **Issues:** Track bugs, enhancements, and other project-related tasks.

## Branching and Merging

- **Branches:** In Git, branches allow you to create isolated environments within your repository. This is particularly useful for developing new features or fixes without affecting the main codebase.
- **Merging:** Once your work on a branch is complete, you can merge the branch back into the main codebase. Git will combine the histories and handle any conflicts.

## Best Practices

- **Commit Messages:** Write clear, concise commit messages that describe what changes were made and why.
- **Branching Strategy:** Adopt a branching strategy that fits your team’s workflow, such as GitFlow or a simple feature-branch model.
- **Pull Requests:** Always use pull requests to review code before merging it into the main branch. This ensures code quality and helps catch potential issues early.

---

## Any Questions?

Feel free to ask any questions regarding Git, GitHub, or anything else covered in this overview.
