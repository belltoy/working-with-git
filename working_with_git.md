autoscale: true

# Working With Git

### By belltoy, Jul 2015

---

![right 50%](https://git-scm.com/images/logos/downloads/Git-Logo-1788C.png)

# What is Git?


> git - the stupid content tracker
-- GIT(1) Manual

Git is a **fast**, **scalable**, **distributed** revision control system with an unusually rich command set that provides both high-level operations and full access to internals.


---

# Why Revision Control?

- Collaboration
- Storing Versions
- Restoring Previous Versions
- Understanding What Happened
- Backup (side-effect)

---

# How to?

- cp
- Centralized (e.g. CVS, Subversion)
- Distributed (e.g. Git, Mercurial, Bazaar)

---
# Why Git?

- Branching and Merging
- Small and Fast
- Distributed
- Data Assurance
- Staging Area
- Free and Open Source
- **World Wide Popular**

---

# Git Basics

---

# Snapshots, Not Differences

---

![inline](https://git-scm.com/book/en/v2/book/01-introduction/images/deltas.png)

_Storing data as changes to a base version of each file._

---

![inline](https://git-scm.com/book/en/v2/book/01-introduction/images/snapshots.png)

_Storing data as snapshots of the project over time._

---

# Nearly Every Operation Is Local

- Entire repository right there on your local disk
- Browse the history, see the changes introduced between any versions
- Work offline

---

# Git Has Integrity

## Everything in Git is check-summed (SHA-1 hash)

---

# Git Generally Only **Adds** Data

---

# Areas

![inline](http://appendto.com/wp-content/uploads/2015/06/Screen-Shot-2015-06-24-at-8.37.13-PM-1024x663.png)

---

# Distributed

### `clone` instead of `checkout`

![inline](http://techidiocy.com/wp-content/uploads/2013/08/svn-repo.png)

---

# About Remote Repositories

- Clones
- Remote repositories can be anywhere
- A repository can have more than one remote

---

# Remote repositories can be anywhere!

- Public git hosting services (e.g. Github, Bitbucket)
- Self hosting centralized server
- Other computer
- Other directories

---

# Getting a Git Repository

Initializing a Repository in an Existing Directory

```sh
$ git init
$ git add README.md
$ git commit -m 'First commit'
```

---

# More Basic Operations

```sh
$ git status                      # Show the working tree status
$ git rm some_file.txt            # Remove files from the working directory and staging area
$ git mv <source> <destination>   # Move or rename a file, a directory, or a symlink
$ git log                         # Show the commit history log
$ git diff                        # Show changes between commits, commit and working tree, etc
$ git help                        # Show the most commonly used git commands
$ git help subcommand             # Show the subcommand help
```

---

# Demo

---

# Branching

---

![inline](https://git-scm.com/book/en/v2/book/03-git-branching/images/branch-and-history.png)

_A branch in Git is simply **a lightweight movable pointer** to one of these commits._

---

# Basic Branching and Merging

---

# Branching Workflows

---

# Long-Running Branches

![inline](http://git-scm.com/book/en/v2/book/03-git-branching/images/lr-branches-2.png)

---

# Topic Branches

![inline](http://git-scm.com/book/en/v2/book/03-git-branching/images/topic-branches-2.png)

---

# Working with the Remotes

---

# Getting a Git Repository

Cloning an Existing Repository

```sh
$ git clone <repository> [directory]

- ssh://[user@]host.xz[:port]/path/to/repo.git/
- git://host.xz[:port]/path/to/repo.git/
- http[s]://host.xz[:port]/path/to/repo.git/
- ftp[s]://host.xz[:port]/path/to/repo.git/
- rsync://host.xz/path/to/repo.git/
- [user@]host.xz:path/to/repo.git/
- file:///path/to/repo.git/
- /path/to/repo.git/
```

---

# Show Remote Repositories

```sh
$ git remote
$ git remote -v
$ git remote add <name> <url>
$ git fetch [remote-name]
```

---

# Remote Branches

- fetch
- pull
- push
- delete remote branch

---

# Tagging

- Listing Your Tags
- Creating Tags
- Annotated Tags
- Lightweight Tags
- Tagging Later
- Sharing Tags
- Checking out Tags

---

# Git Configuration

## `man git-config`

---

# Configuration Files

```
$(prefix)/etc/gitconfig
~/.gitconfig
$GIT_DIR/config
```

---

# Basic Client Configuration

- `user.name`
- `user.email`
- `core.editor`
- `color.ui`
- `diff.tool`
- `merge.tool`

---

# Advanced Topics

---

# Undoing Things

---

# The Three States

![inline](https://git-scm.com/book/en/v2/book/01-introduction/images/areas.png)

---

# Some Tips

- Modify last commit message

```sh
$ git commit --amend              # Now you can write commit message again
```

- Forget to add a file?

```sh
$ git commit -m 'do some changes'  # Assume we forgot to add another file `README.md`
$ git add README.md                # We add the forgotten file
$ git commit --amend               # Then we add the file in the last commit!
```

---

# Dealing with Merge Conflicts

---

# Rebasing

---

# Distributed Workflows[^1]

---

# Centralized Workflow

![inline](https://git-scm.com/images/about/workflow-a@2x.png)

---

# Integration-Manager Workflow

![inline](https://git-scm.com/images/about/workflow-b@2x.png)

---

# Dictator and Lieutenants Workflow

![inline](http://rocketeerbkw.github.io/slides/austin-linux-meetup/git/workflow-c@2x.png)

---

# Git-flow

## A successful Git branching model[^2]

![right fit gitflow](http://nvie.com/img/git-model@2x.png)

---

# Best Practises - "DO"s

- Do read about git
- Do commit early and often
- Do test before you commit
- Do choose a workflow
- Do make useful commit messages
- Do keep up to date
- Do use useful tools

---

# Best Practises - "DON'T"s

- Don't panic
- Don't change published history
- Don't rewrite public history
- Don't change where a tag points
- Don't commit anything that can be regenerated from other things that were committed
- Don't commit configuration files
- Don't commit large binary files (when possible)
- Don't create very large repositories (when possible)
- Don't use reset (--hard || -merge) without committing/stashing
- Don't prune the reflog

---

# Further Reading

- [Git Official Web Site](http://git-scm.com)
- [ProGit](https://progit.org)
- Manual Pages[^3]

---

# Q & A

---

# Thanks


[^1]: [Distributed Workflows](http://git-scm.com/book/en/v2/Distributed-Git-Distributed-Workflows)

[^2]: [A successful Git branching model](http://nvie.com/posts/a-successful-git-branching-model/)

[^3]: `man git`
