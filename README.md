# GitHub Tutorial

_by <Ayden Rodriguez>_

---
## Git vs. GitHub
#### Git
* It's a Version Control system.
* It keeps a "snapshot" of a piece of code.
* It could be used to look back at older versions of certain pieces of code
* It doesn't require **GitHub** to function.

#### GitHub
* It stores code in the cloud
* It visually keeps track of any changes
* It's easy to use when collaborating with others
* It requires the use of **Git** to work properly.

#### Differences between Git and GitHub
* Git is a software that allows a person to change or edit a repository
* GitHub is a storage software for the repositories
* Guthub also requires the use of Git while Git doesn't need GitHub to function

---
## Initial Setup
#### Creating a account on Github
1. Go to _github.com_ and click **Sign Up**.
2. Create a account using you hstat email which would be `firstname_firstinitialoflastname_last4#ofosis@hstat.org`(Ex:`aydenr7109@hstat.org`) and your password should be your osis number and a few letters for convenience.
3. Your username should be the first half of your email which would be `firstname_firstinitialoflastname_last4#ofosis`.

##### Setting up cs50
* To set up your ide, go to this link https://github.com/hstatsep/ide50
    * Follow all of the steps and you should get the end result that is described in it.

##### Importance of SSH
* In the directions, one of the steps tells us to generate and connect a SSH Key
    * We need so that we can set up a basic connection between GitHub(remote) and cs50(local).
    * Another reason we establish this connection is so that we can copy and paste SSH links when trying to push any changes made in commits for future projects that involve git.
    * Lastly, we use SSH as opposed to HTTPS as HTTPS requires you to type your username and password every time that you make a commit in cs50 which is very annoying and time-consuming.

---
## Repository Setup
1. In the parent folder, create a new folder using the `mkdir` command.
2. Once you use `cd` to move into the right folder, type `git init` to activate git and turn the folder into a repository.
3. Create a README.md file using the `touch` command.
4. Use the `c9` command to move into the file and type whatever you want or need to type.
5. Once you are finished editing in the file, use `git add .` to add the changes to "the staging area".
6. Use `git status` to check and make sure that the changes made in the file were added to the "staging area". You can tell whether or not it was based on if the modified text is in red which means it hasn't been added or green which means it has been added.
7. Use the command `git commit -m ""` to save the addition and make sure that you write a message in the quotation marks in lowercase letters to make that commit easier to remember and look back at.
8. With that done, go to _github.com_, click the **+** on the top right, and select **New repository** to create a new repository. Make sure that it shares the same name as the repository in cs50 in order to connect the two.
9. In the repository on _github.com_, tap on the green "Clone or Download" option and copy the **SSH** link.
10. Next, go back to cs50 and type the command `git remote add origin URL` in which the URL would be the SSH link from the repository at _github.com_. Through that, you can now connect changes made from cs50 to the repository on _github.com_.
11. Then, type the command `git push -u origin master` to push the latest commit from the repository on cs50 to the one on _github.com_.
12. Finally, go back to _github.com_ and refresh the page. There, you will see the README.md file added to the repository and once you open it, you will see the text you wrote in cs50 present as a preview.
13. If you followed all of the steps correctly, Congratulations!!!!!! You know how to make repositories in cs50 and how to connect it to repositories on _github.com_.

---
## Workflow & Commands
#### Git Init
* `git init` is a command that initializes git in a folder.
* Remember these practices while having git activated
    * Make sure you're in the right folder when you initialize git.
    * Never do it in the ~/ folder or else you would cause multiple issues.
    * If you want to initialize git in a different folder, make sure you un-initialize it whatever folder it is currently activated in.

#### Git Status
* `git status` is a command that checks and sees which files are staged to be commited.
    * You can tell which files are set to be commited if the text for the file is green as opposed to red.
    * This is an optional command as it is not necessary to adding and commiting a file.
    * It's best to use when checking whether or not an edit made in a file was added or not

#### Git Add
* `git add` is a command that add files to the "staging area".
    * There are three types of `git add` that can be used.
    * `git add file.ext` adds files to the "stage" so they can be commited.
    * `git add .` adds everything in the current directory which includes changed, renamed, or deleted files.
    * `git add --all` adds all new and modified files to the repository.
    * Usually, it's the next step after editing a file.

#### Git Commit
* `git commit -m ""` is a command that is used to save the changes made in the files that were included by git add.
    * The `-m ""` is included in order to make a short message to describe what changes the commit is making.
    * The message should be in lowercase letters and should describe what changes were made in a file.

#### Git Diff
* `git diff` is a command that displays the difference between your current code and the previous commit.
    * It's a useful tool when trying to tell if their was a change in git.
    * The difference between `git diff` and `git status` is that git status troubleshoots whether or not an issue is present while git diff shows changes between commits.

#### Git Log
* `git log` is a command that lets you see your past commits.
    * Press Q to quit git log

#### Git Push
* `git push` is a command that pushes any changes saved by git commit from cs50 to GitHub.
* `git push -u origin master` is used as the first git push to take place between cs50(local) and GitHub(remote)
* Steps to utilize `git push` include
1. Create a repository on GitHub and make a README.md file with it.
2. Clone it to cs50 in the parent directory.
3. Cd into the repository and open the README.md file with c9.
4. Make any edits or changes, add, and commit.
5. Use git push to send those changes made in the commit the GitHub.
6. Go back to _github.com_ and refresh the page to see the changes made.
OR
1. Create a repository in cs50 and make a README.md file with it.
2. Make any edits or changes, add, and commit.
3. Create a repository on GitHub that shares the same name.
4. Copy and paste onto cs50
git remote add origin git@github.com:aydenr7109/about-ayden.git
git push -u origin master
5. Go back to _github.com_ and refresh the page to see the changes made.

#### Git Pull
* `git pull` is a command that brings changes from GitHub to cs50.

#### Git Remote -v
* `git remote -v` Tells you where your commits will be pushed to or pulled from.
    * the v stands for verbose
    * `git remote add origin URL` sets up a connection between a GitHub repository and a cs50 repository.

---
## Rolling Back Changes
#### rm -rf .git
* `rm -rf .git` is a command that un-initializes git.
* Remember to use it when you want to remove git from a certain folder and make sure you are in that folder in order to remove git.

#### git checkout -- file
* `git checkout -- file` is a command that deletes any edits made in between the current commit and the next commit.
* It is best used as a shortcut when wanting to delete any edits without having to go back into the file.

#### git reset HEAD file
* `git reset HEAD file` is a command that will undo the most recent git add.
* It is best used when wanting to undo a git add without having to edit and add again.

#### git revert
* `git revert` is a command that changes the current commit back to an older commit.
* It is best used when you want to undo changes made in a commit without editing, adding, and committing again.

#### git reset
* `git reset --hard [SHA]` is a command that can be used to undo a git push.
* It is best used when wanting to change something that was pushed to GitHub without having to edit, add, commit, and push again.