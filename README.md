# Git Cheatsheet

This is a "cheat sheet" of all the Git commands I curently know from Udacity course and not only:
[How to Use Git and GitHub](https://www.udacity.com/course/how-to-use-git-and-github--ud775).
For a more detailed view go to: [Git Reference](https://git.github.io/git-reference/) [Git](https://git-scm.com/book/en/v2).

<h3>Basic Console Commands</h3>

Command | Description | Options
------------ | ------------- | -------------
`cd <directory path>` | "change directory" -<br>changes the folder you are operating in. | `~` - to home directory<br>`../` - up one folder
`mkdir <folder name>` | "make directory" -<br>creates a new folder. |
`pwd` | "print working directory" -<br>displays the file path of the folder you are working in. |
`ls` | "list" -<br>lists files and folders in the folder you are working in | `-a` - list hidden files too
`touch <filename>` | creates a new file |
`explorer` | Open the current folder in Windows Explorer |
`echo 'alias <alias-name>="<path>"' >> ~/.bashrc` | Add the specified line into my .bashrc file <br> this will create an shortcut for the specified program |
`vim <file>` | Open the specified file into vim text editor |

<h3>Getting and Creating Projects</h3>

Command | Description | Options
------------ | ------------- | -------------
`git init` | Create an empty Git repository |
`git clone <repo-url>` | Clone a repository into a new directory | `directory` - create a new folder for the clone<br>

<h3>Basic Snapshotting</h3>

Command | Description | Options
------------ | ------------- | -------------
`git add <filename>` | Add file contents to the index |
`git status` | Show the working tree status |
`git diff` | Show changes between commits, commit and working tree, etc | (no arguments) - compare changes between working directory and staging area<br>`--staged` - compare changes between staged area and the most recent commit<br>`<commit1> <commit2>` - compare two commits
`git commit` | Record changes to the repository | `-m` - add message in terminal<br>`-a` - automatically stage files that have been modified and deleted <br> `--amend` - amend stanging files and change commit message (only in local)
`git reset` | Reset current HEAD to the specified state | `HEAD` - unstage file from index and reset pointer to HEAD <br>`--soft` - moves HEAD to specified commit reference, index and staging are untouched <br>`--hard` - unstage files and undo any changes in the working directory since last commit (unreversible)
`rm <filename>` | deletes a file |
`mv <filename> <target folder name>` | moves a file |

<h3>Branching and Mearging</h3>

Command | Description | Options
------------ | ------------- | -------------
`git branch` | List, create, or delete branches | `<branch-name>` - switch to branch<br>`-a` - shows all local and remote branches<br>`-r` -shows only remote branches<br>`-d <branch-name>` - delete branch<br> `-f <branch> <commit>` - move defined branch to the defined commit <br> `-m <new-name>` - change branch name with new-name
`git checkout` | Switch branches or restore working tree files | `<branch-name>` - switch to branch<br>`-b <new-branch-name>` - create and switch to new branch<br> `ID` - swich to the specified commit ID<br> `master` - swich to master head<br> `-- <file>` - extract the version of the `<file>` from the staging area (index)<br> `-- <directory>` - extract all files from the staging area (index) whose path name begins with `<directory>`<br> `-- .` - extract all files from the staging area (index) (if you are at the top level of your work-tree)
`git merge <branch1> <branch2>` | Join two or more development histories together | `--abort` - abort merge if there are unexpected conflicts
`git log` | Show commit history | `--oneline` - display on one line<br>`--graph` - show a graph of the branch, merge history<br>`-<n>` - show `n` commits<br>`--stat` - shows number of files changed, plus deletions and insertions for each commit

<h3>Sharing and Updating Projects</h3>

Command | Description | Options
------------ | ------------- | -------------
`git remote` | View remote repositories | `add <url>` - add new remote <br> `<new-remote>` - create new-remote <br> `-v` - view remote with more (verbose) information <br> `set-url <remote> <url>` - change the url of the specified remote
`git fetch` | Download objects and refs from another repository |
`git pull <remote> <branch>` | Update remote refs along with associated objects |
`git push <remote> <branch>` | Fetch from and integrate with another repository or a local branch |

<h3>Inspection and Comparison</h3>

Command | Description | Options
------------ | ------------- | -------------
`git show` | It shows the log message and textual diff | `<commit-ID>` - Show various types of objects

<h3>Other Gir Commands</h3>

Command | Description | Options
------------ | ------------- | -------------
`git help` | Prints the synopsis and a list of the most commonly used commands | `-a` prints all commands
`git config --global color.ui auto` | Color diff output <br> red for removed and green for added. |
`git gc` | git garbage collector`
