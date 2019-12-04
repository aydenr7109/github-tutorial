# GitHub Tutorial

_by Ayden Rodriguez_

---
## Git vs. GitHub
#### Git
* It's a Version Control system.
* It keeps a "snapshot" of a piece of code.
* It could be used to look back at older versions of certain pieces of code.
* It doesn't require **GitHub** to function.

#### GitHub
* It stores code in the cloud.
* It visually keeps track of any changes.
* It's easy to use when collaborating with others.
* It requires the use of **Git** to work properly.

#### Differences between Git and GitHub
* Git is a software that allows a person to change or edit a repository.
* GitHub is a storage software for the repositories.
* Guthub also requires the use of Git while Git doesn't need GitHub to function.

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
> Note: If any command is shown or described as a line of code, that's the way of how it's supposed to be written in cs50. Ex:`git init`

1. In the parent folder, create a new folder using the `mkdir name` command where "name" would be what you would want to call the folder like "first-repo". Make sure that if you make a folder that has more than one word, **DON'T USE SPACES!!!!!!**
2. Once you created it, use `cd name` to move into the new folder and then type `git init` to activate git and turn the folder into a repository.
3. Create a README.md file using the `touch README.md` command.
4. Use the command `c9 README.md` to move into the file.
5. Once in the file, edit or type whatever you want or need to type like "this is my first repo".
6. Once you are finished editing in the file, go back to the command line and type `git add .` to add the changes to "the staging area".
7. Use `git status` to check and make sure that the changes made in the file were added to the "staging area". You can tell whether or not it was based on if it says that the modified text is in red which means it hasn't been added or green which means it has been added.
8. Use the command `git commit -m ""` to save the addition and make sure that you write a message in the quotation marks in lowercase letters to make that commit easier to remember and look back at.
9. With that done, go to _github.com_, click the **+** on the top right, and select **New repository** to create a new repository. Make sure that it shares the same name as the repository in cs50 in order to connect the two.
10. In the repository on _github.com_, tap on the green "Clone or Download" option and copy the **SSH** link.
11. Next, go back to cs50 and type the command `git clone "SSH link"` in the repository you made in cs50 where the "SSH link" would be the link that you copied from _github.com_.
12. Then, type the command `git remote add origin URL` in which the URL would also be the SSH link that you copied from the repository at _github.com_. Through that, you can now connect changes made from cs50 to the repository on _github.com_.
13. Then, type the command `git push -u origin master` to push the latest commit from the repository on cs50 to the one on _github.com_.
14. Finally, go back to _github.com_ and refresh the page. There, you will see the README.md file added to the repository and once you open it, you will see the text you wrote in cs50 present.
15. If you followed all of the steps correctly, Congratulations!!!!!! You know how to make repositories in cs50 and how to connect it to repositories on _github.com_.

---
## Workflow & Commands
> Note: If any command is shown or described as a line of code, that's the way of how it's supposed to be written in cs50. Ex:`git init`

#### Git Init
* `git init` is a command that initializes git in a folder.
* Remember these practices while having git activated
    * Make sure you're in the right folder when you initialize git.
    * Never do it in the ~/ folder or else you would cause multiple issues.
    * If you want to initialize git in a different folder, make sure you un-initialize it whatever folder it is currently activated in.

#### Git Status
* `git status` is a command that checks and sees which files are staged to be committed.
* It's best to use this command after using `git add .`.
    * You can tell which files are set to be committed if the text for the file is green as opposed to red.
    * This is an optional command as it is not necessary to adding and committing a file.
    * It's best to use when checking whether or not an edit made in a file was added or not

#### Git Add
* `git add` is a command that add files to the "staging area".
* It's best to use this command after making any edits in a file.
    * There are three types of `git add` that can be used.
    * `git add file.ext` adds files to the "stage" so they can be committed.
    * `git add .` adds everything in the current directory which includes changed, renamed, or deleted files.
    * `git add --all` adds all new and modified files to the repository.
    * Usually, it's the next step after editing a file.

#### Git Commit
* `git commit -m ""` is a command that is used to save the changes made in the files that were included by git add.
* It's also best to use this command after using `git add .`
    * The `-m ""` is included in order to make a short message to describe what changes the commit is making.
    * The message should be in lowercase letters and should describe what changes were made in a file.

#### Git Diff
* `git diff` is a command that displays the difference between your current code and the previous commit.
* It's best to use this command after using `git commit -m ""` to see any differences between the last commit and the commit before it.
    * It's a useful tool when trying to tell if there was a change in git.
    * The difference between `git diff` and `git status` is that git status troubleshoots whether or not an issue is present while git diff shows changes between commits.

#### Git Log
* `git log` is a command that lets you see your past commits.
* It's best to use this command when trying to revert back to an older commit.
    * Press Q to quit git log

#### Git Push
* `git push` is a command that pushes any changes saved by git commit from cs50 to GitHub.
* `git push -u origin master` is used as the first git push to take place between cs50(local) and GitHub(remote)
* It's best to use this command after using `git commit -m ""`to push the new changes.
* Steps to utilize `git push` include:
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
* It's best to use this command after making changes on _github.com_

#### Git Remote -v
* `git remote -v` Tells you where your commits will be pushed to or pulled from.
* It's best to use this command when trying to figure out where your commits will be pushed or pulled to
    * the v stands for verbose.
    * `git remote add origin URL` sets up a connection between a GitHub repository and a cs50 repository.

#### Git Remote Add Origin URL
* `git remote add origin URL` is a command that connects a repository on _github.com_ to one in cs50.
* It's best to use this command when trying to establish a connection between the repository at _github.com_ and the repository at cs50.
    * git: This is a git command.
    * remote: This helps set up a connection between repositories on _github.com_ and cs50.
    * add: This adds the remote repository(the repository at GitHub) instead of removing it.
    * origin: The "nickname" for the repository on _github.com_
    * URL: The location of the remote repository(It should be the one at _github.com_). It could either be an SSH or a HTTPS link.

#### Git Push -U Origin Master
* `git push -u origin master` is a command that pushes changes from the latest commit on cs50 to the repository at _github.com_
*  It's best to use this command when trying to push your first commit to the repository at _github.com_
    * git: This is a git command.
    * push: This sends our commits from the repository on cs50 to the repository at _github.com_
    * u: This stands for upstream and tells git to remember where to push the changes from a commit on cs50 to.
    * origin: This stands for the remote repository(the one at _github.com_) that you would push your changes to.
    * master: This is a reference name for the "main" branch of your project.

---
## Rolling Back Changes
> Note: If any command is shown or described as a line of code, that's the way of how it's supposed to be written in cs50. Ex:`rm -rf .git`

#### rm -rf .git
* `rm -rf .git` is a command that will uninitialize git.
* It's best to use this command when you want to initialize git in a different repository and it is still activated in a different repository.
* Remember to use it when you want to remove git from a certain folder and make sure you are in that folder in order to remove git.

#### git checkout -- file
* `git checkout -- file` is a command that deletes any edits made in between the current commit and the next commit.
* It is best used as a shortcut when wanting to delete any edits without having to go back into the file.

#### git reset HEAD file
* `git reset HEAD file` is a command that will undo the most recent git add.
* It is best used when wanting to undo a git add without having to edit and add again.

#### git revert
* `git revert` is a command that changes the current commit back to an older commit.
* When reverting, you must know the SHA which are the IDs for past commits. It's best recommended that you copy the SHA IDs when using `git log` to revert back to an older commit.
* It is best used when you want to undo changes made in a commit without editing, adding, and committing again.

#### git reset --hard [SHA]
* `git reset --hard [SHA]` is a command that can be used to undo a git push.
* It is best used when wanting to change something that was pushed to GitHub without having to edit, add, commit, and push again.