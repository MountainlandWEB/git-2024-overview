## What is Git?
``Git`` is a ``distributed version control`` software. Version control is a way to save changes over time without overwriting previous versions. Being ``distributed`` means that every developer working with a Git repository has a copy of that entire repository – every commit, every branch, every file.

## Register for a Git Account
GitHub is the single largest host for Git repositories, and is the central point of collaboration for millions of developers and projects. A large percentage of all Git repositories are hosted on GitHub, and many open-source projects use it for Git hosting, issue tracking, code review, and other things. So while it’s not a direct part of the Git open source project, there’s a good chance that you’ll want or need to interact with GitHub at some point while using Git professionally.

### Account Setup and Configuration
The first thing you need to do is set up a free user account. Simply visit ``[https://github.com](https://github.com/signup?source=login)``, type your email address and a password, then enter a username click the ``Continue`` green button. Then account will need to be verified with a puzzle then a code from your email address.

Whether or not you've worked with version control before, there are a few things you should know before getting started with Git:

## Why use Git?
Version control is very important – without it, you risk losing your work. With Git, you can make a "commit", or a save point, as often as you'd like. You can also go back to previous commits. This takes the pressure off of you while you're working. Commit often and commit early, and you'll never have that gut-sinking feeling of overwriting or losing changes.

There are many version control systems out there – but Git has some major advantages.
+ Git uses SHA compression, which makes it very fast. Git stores changes in SHA hashes, which work by compressing text files. That makes Git a very good version control system (VCS) for software programming, but not so good for binary files like images or videos.
+ Storage inefficiency with binary files, such as images and videos, are typically already compressed in specific formats (JPEG, PNG, MP4, etc.). Git's delta compression works by storing the differences (or deltas) between versions of files. However, changes to binary files often result in significant alterations across the entire file, rather than just localized changes. As a result, Git may need to store multiple complete copies of the file, especially if changes are frequent or substantial. This can lead to increased storage requirements compared to text files, where changes are typically localized to specific lines.
+ Binary files may undergo significant changes with each version, making it harder for Git to efficiently manage and store these changes. This can result in slower performance and larger repository sizes over time. Git stores the entire history of files in its repository, which includes all versions of each file. For large binary files like videos, this can quickly lead to a bloated repository size. Git was originally designed to handle text-based source code files where changes are frequent but typically small in size. Managing large binary files with Git can therefore be cumbersome and inefficient.
+ Operations such as cloning a Git repository or checking out different versions involve transferring and potentially processing all files in the repository. With large binary files, these operations can be slower and require more network bandwidth and processing power compared to repositories containing primarily text files. Git relies on textual differences to track changes efficiently. For text files, Git can easily display line-by-line changes and compute differences. However, binary files lack this line-by-line structure, making it difficult for Git to provide meaningful diffs or efficiently compute changes between versions.

Branches are lightweight and cheap, so it's OK to have many of them. Git stores changes in SHA hashes, which work by compressing text files. That makes Git a very good version control system (VCS) for software programming, but not so good for binary files like images or videos.
Git repositories can be connected, so you can work on one locally on your own machine, and connect it to a shared repository. This way, you can push and pull changes to a repository and easily collaborate with others.

## How to use Git
Some of the most important and most used commands that you'll find there are:
+ ``git clone [url]:`` Clone (download) a repository that already exists on GitHub, including all of the files, branches, and commits.
+ ``git status:`` Always a good idea, this command shows you what branch you're on, what files are in the working or staging directory, and any other important information.
+ ``git branch:`` This shows the existing branches in your local repository. You can also use git branch [branch-name] to create a branch from your current location, or git branch --all to see all branches, both the local ones on your machine, and the remote tracking branches stored from the last git pull or git fetch from the remote.
+ ``git checkout [branch-name]:`` Switches to the specified branch and updates the working directory.
+ ``git add [file]:`` Snapshots the file in preparation for versioning, adding it to the staging area.
+ ``git commit -m "descriptive message":`` Records file snapshots permanently in the version history.
+ ``git pull:`` Updates your current local working branch with all new commits from the corresponding remote branch on GitHub. git pull is a combination of git fetch and git merge.
+ ``git push:`` Uploads all local branch commits to the remote.
+ ``git log:`` Browse and inspect the evolution of project files.
+ ``git remote -v:`` Show the associated remote repositories and their stored name, like origin.
