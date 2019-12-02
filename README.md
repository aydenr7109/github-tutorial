# GitHub Tutorial

_by <Ayden Rodriguez>_

---
## Git vs. GitHub
#### Git
* It's a Version Control system.
* It keeps a "snapshot" of a piece of code.
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
https://github.com/hstatsep/ide50


---
## Repository Setup
1. In the parent folder, create a new folder using the `mkdir` command.
2. Once you use `cd` to move into the right folder, type `git init` to activate git and turn the folder into a repository.
3. Create a README.md file using the `touch` command.
4. Use the `c9` command to move into the file and type whatever you want or need to type.
5. Once you are finished editing in the file, use `git add .` to add the changes to "the staging area".
6. Use the command `git commit -m ""` to save the addition and make sure that you write a message in the quotation marks in lowercase letters to make that commit easier to remember and look back at.
7. With that done, go to _github.com_ and create a new repository that shares the same name as the repository in cs50.
8. In the repository on _github.com_, tap on the green "Clone or Download" option and copy the **SSH** link.
9. Next, go back to cs50 and type the command `git remote add origin URL` in which the URL would be the SSH link from the repository at _github.com_. Through that, you can now connect changes made from cs50 to the repository on _github.com_.
10. Then, type the command `git push -u origin master` to push the latest commit from the repository on cs50 to the one on _github.com_.
11. Finally, go back to _github.com_ and refresh the page. There, you will see the README.md file added to the repository and once you open it, you will see the text you wrote in cs50 present as a preview.
12. If you followed all of the steps correctly, Congratulations!!!!!! You know how to make repositories in cs50 and how to connect it to repositories on _github.com_.

---
## Workflow & Commands
#### Git Status
* `git status` is a command that checks and sees which files are staged to be commited.
* You can tell which files are set to be commited if the text for the file is green as opposed to red.
* This is an optional command as it is not necessary to adding and commiting a file.
* It's best to use when checking whether or not an edit made in a file was added or not

#### Git Add
* There are three types of `git add` that can be used.
* `git add file.ext` adds files to the "stage" so they can be commited.
* `git add .` adds everything in the current directory which includes changed, renamed, or deleted files.
* `git add --all` adds all new and modified files to the repository.
* Usually, it's the next step after editing a file.

#### Git Commit
* `git commit -m ""` is a command that is used to save the changes made in the files that were included by git add.
* The `-m ""` is included in order to make a short message to describe what changes the commit is making.
*

#### Git Push
* .

---
## Rolling Back Changes
Any edit:

Git add: To undo git add before a commit: Run git reset <file> or git reset to unstage all changes.

Git commit: git revert HEAD

Git push: