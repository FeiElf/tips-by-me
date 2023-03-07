
# Git It Right

## Before you start your day of development, please do:

- Make sure you **ARE NOT** on the main branch
- Make sure you **ARE** on the correct branch which is assigned to you by the project maintainer according to your task
- Checkout to your branch and you are ready to start

## Before you Commit, please do:

- Make sure you **ARE** on the correct branch which is assigned to you by the project maintainer according to your task
- Make sure you write meaningful messages
- Think commits as your work log entries, commit whenever you think is necessary

## After you finished your task, please do:

- Make sure you **ARE** on the correct branch which is assigned to you by the project maintainer according to your task
- Push your local changes to **the very same branch** on the remote repository
- Create a pull request to let your team members know that you've finished your task and your code is ready to be reviewed
- **Never** merge your branch yourself, the reviewer or the project maintainer will do the merge

## After the project maintainer merged a branch, please do following to make sure your codebase is in sync with latest changes:

1. `git checkout main && git pull origin main` (this will make sure your local main branch have the latest changes)
2. `git checkout <your-branch> `
3. `git rebase origin/main` (after running this command, if there are conflicts, you should resolve them manually, after you resolve them, you can run `git rebase --continue` and goto step 4; if there are no conflicts, you can goto step 4)
4. `git push --force origin <your-branch>` (this will push your local branch to the remote repository)

## To review a coworker's remote branch (pull request) on your local machine, please do:

1. `git fetch <remote> <branch>` (this will fetch the remote branch to your local)
2. `git checkout <remote>/<branch>` (this will switch you to your local copy of the remote branch, you can now start testing or making changes on the remote branch copy)
3. After you've done testing, you can switch back to your working branch and the changes you made on the remote branch copy will be discarded
4. If you have questions or comments, find the bitbucket pull request and comment on the code
5. (PROJECT MAINTAINER ONLY) If you think the code is good, you can then either do the merge on your local machine then push the merge to remote or go pull request page on bitbucket, if there're no conflicts, you should be able to click the merge button

# Cheat Sheet

`git clone <repo>` (Clone repo located at <repo> into local machine)  
`git status` (list which files are staged, unstaged, and untracked)  
`git add .` (stage all the changes in the current folder)  
`git commit -m "your message"` (commit your changes)

`git fetch <remote> && git checkout --track <remote>/<branch-name>` (fetch a remote branch and switch to the branch locally)  
`git push <remote> <branch-name>` (push your changes to remote repo)

# Everytime you modified .gitignore
`git rm -rf --cached .`
`git add .`

See more at [atlassian-git-cheatsheet](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet)
