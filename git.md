# GIT
- Distributed Version Controller 
    - command line interface (cli)
    - code database
    - incremental development
    - compare and revert changes
    - parallel versions
    - documents updates
    - directed acyclic graph (DAG)



## Setting Up

`➜ ➜ ➜ mkdir repo && cd repo`

`➜ ➜ ➜ git init`

`➜ ➜ ➜ git config user.name "YOUR_USERNAME"`

`➜ ➜ ➜ git config user.email "YOUR@EMAIL.COM"`

- add `--global` to make it work for all repos

`➜ ➜ ➜ git config --global user.email YOUR@EMAIL.COM`



## Commits
- snapshot of changes in the repository at a specific moment *T*
- small and incremental changes
- contains only the changes made to the files
- differentiates by hashvalues
- can be reverted/modified/revisited
- works in 3 steps:

- `➜ ➜ ➜ git status`:
    - returns the **status** of your repository
    - shows which files have changed but tracked

- `➜ ➜ ➜ git add <path/to/file>`:
    - stage the specific files for the next commit

- `➜ ➜ ➜ git commit`:
    - commit the files (add a node to the graph)
    - PLEASE WRITE A NICE MESSAGE EXPLAINING
    - TIP: `➜ ➜ ➜ git commit -m <your message here :)>`

- .gitignore file: a hidden file containing file patterns you want git to ignore



## Monitoring
- `➜ ➜ ➜ git diff <path/to/file>`:
    - show the differences between versions
    - if `<path/to/file>` is not given, shows changes to all tracked files

- `➜ ➜ ➜ git log`:
    - shows the commit history in your current branch


## Branch
- paths in the graph (parallel lines of development)
- pointers to a commit
- production branch: **main**
- homolog branch: **devel/dev** 
- create a branch to implement something so that you dont destroy the codebase :)
- switching branches: changes your working directory to match the branch's snapshot

- commands:
    - `➜ ➜ ➜ git branch`: list local branches
    - `➜ ➜ ➜ git branch <branch_name>`: create new branch
    - `➜ ➜ ➜ git checkout <branch_name>`: switch to another branch
    - `➜ ➜ ➜ git checkout -b <branch_name>`: create + switch to another branch

- merging branches:
    - can be merged, adding changes from *YOUR_BRANCH* -> *DESTINY*
    - pull request: discussion about a potential merge
    - flow: *your_branch* -> *devel* -> *main*
    - **NEVER MERGE YOUR BRANCH WITH OTHERS LOCALLY, DO A PULL REQUEST  INSTEAD**
    - **delete your branch after merge**

    - commands:
        - `➜ ➜ ➜ git merge <branch_name>`


## Remote
- remote repos are copies of your local repo on a external server
- allows collaboration
- keeps local and remore in sync

- concepts:
    - `➜ ➜ ➜ git pull`: get and merge changes from the remote repo to local
    - `➜ ➜ ➜ git push`: send your local commits to the remote repo
    - `➜ ➜ ➜ git fetch`: get changes, but doesnt merge

- commands:
    - `➜ ➜ ➜ git clone <url>`: make a copy of a remote repo (normal method)
    - `➜ ➜ ➜ git remote add <name> <url>`: add a remote to a existing local repo (not correct)
    - `➜ ➜ ➜ git push <remote> <branch>`: upload commits to a specific **branch** of **remote**
        - `➜ ➜ ➜ git push origin main`
    - `➜ ➜ ➜ git pull <remote> <branch>`: get and merge from a **remote branch** (best way to do)
        - `➜ ➜ ➜ git pull origin main`



## TIPS
- if you commit on the wrong branch, its okay :)
- if you **PUSH** to the wrong branch, its **NOT** okay
- NEVER COMMIT DIRECTLY ON THE MAIN OR DEVEL, IT WILL BREAK YOUR PROJECT
- always write a good commit message
- (but you can fix it easily)
- never merge locally, always merge on pull requests (directly on the browser)
- have fun with git, build your own little projects to get better
- git gets easy with time, dont worry :)
- if it does not, i have a bad news for you...

    


