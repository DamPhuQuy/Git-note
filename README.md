# Git note 

## 1. Git workflow

### 1.1. Git area

The Three Areas of Git
- Working Directory: This is the actual directory on your computer where you are currently making changes to files. Changes here are initially considered "untracked" or "modified" but not yet saved by Git as a version.
- Staging Area (Index): This acts as a temporary "draft board" or intermediate area where you prepare changes to be included in the next commit. You use the git add command to move changes from the working directory to the staging area. This gives you granular control, allowing you to selectively stage specific files or even parts of a single file, ensuring that only related changes are included in a single commit.
- Local Repository (.git directory): This is where Git permanently stores the project's history, including all metadata and the object database of committed snapshots. When you run the git commit command, Git takes all the changes currently in the staging area and records them as a new, permanent version (commit) in the local repository.

### 1.2. Typical Git Workflow
The basic workflow involves a progression through these areas:
- Modify files in your Working Directory.
- Stage the specific changes you want to save using git add [filename] or git add .
- Commit the staged changes to your Local Repository using git commit -m "[message]"

## 2. Git commands

### 2.1. Git config
- To configurate identity
`git config --global user.name "Your name"`
`git config --global user.email "youremail@gmail.com"`

### 2.2. Git init 
- To let git manage an ordinary folder
`git init`

### 2.3. Git status
- To provides information designed to help you understand what changes are taking place in your project.

`git status`

- Red status: git realized the changes, but it is not added to staging area.

- Blue status: the files is added to staging area and ready to commit.

### 2.4. Git commit
- Save a snapshot of your staged changes to the local repository

`git commit`: multi-line commit message
`git commit -m "[messsage]"`: single line commit message

### 2.5. Git log
- To view the commit history of a Git repository

`git log`

- The string right after the "commit" is called SHA-1 hash. It plays as an ID for the version that you have saved.

- In addition, you will see (HEAD -> main), that means: 
    - `main`: branch that you are working with. 
    - `HEAD`: a pointer to show the current position in project history.

## 3. Working with branches

Let imagine your project as a tree: 
- Branch `main`: a main trunk, containing the most stable source code, ready to run. 
- Sub-branches: Like branches growing from the trunk. You can create a new branch to test anything that you want without affecting the main trunk. 
- If the test fails? You simply cut off that branch. If it succeeds? You "merge" that branch back into the main trunk.

`git branch <branch-name>`: Create a new branch
`git checkout <branch-name>`: Move the HEAD pointer to that branch to work on.
`git checkout -b <branch-name>` = git branch + git checkout
<!-- test-->
