
### Set up
Configuring user information used across all local repositories

*  **$ git config --global user.name “[firstname lastname]”**\
Set a name that is identifiable for credit when review version history

* **$ git config --global user.email “[valid-email]”**\
Set an email address that will be associated with each history marker

### Create repositories
When starting out with a new repository, you only need to do it
once; either locally, then push to GitHub, or by cloning an
existing repository. <br>

*  **$ git init** \
Turn an existing directory into a git repository 
* **$ git clone [url]** \
Clone (download) a repository that already exists on
GitHub, including all of the files, branches, and commits

Move files or folder into another directory:
* Linux : mv [original file] [new directory]
* Windows : move [original file] [new directory]

### Make changes
Browse and inspect the evolution of project files

* **$ git stauts**\
Show modified files in working directory, staged for your next commit

* **$ git add [file]**\
Add a file as it looks now to your next commit (stage)

* **$  git commit -m "[descriptive message]"**\
Records file snapshots permanently in version history

* **$ git push origin master**\
Transmit local branch commits to the remote repository branch

* **$ git pull**\
fetch and merge any commits from the tracking remote branch

* **$ git diff [first-branch]...[second-branch]**\
Shows content differences between two branches

#### Trouble Shooting

1. Git push error “You must verify your email address.”\
**$git remote set-url origin  https://<i></i>YourName:YourPassword<i></i>@github.com/YourName/YourRepo.git** 

2. How do you push just a single Git branch (and no other branches)?\
https://stackoverflow.com/questions/820178/how-do-you-push-just-a-single-git-branch-and-no-other-branches \
I am working on a local git repository. There are two branches, master and feature_x. \
I want to push feature_x to the remote repo, but I do not want to push the changes on the master branch. \
Will a git push origin feature_x from my feature_x branch (feature_x branch already exists on remote) work? \

    > **1. git checkout feature_x** <br>
    > **2. git push origin feature_x**

