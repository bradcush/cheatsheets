# GIT cheat sheet

A list of simple but helpful commands and workflows for git

## Recover previous commit
* `git reflog`: Show reference logs for the local repository
* `git reset --hard <commit>`: Reset the head of your current branch to specific commit

## Rebasing
* `git rebase --onto <new-parent> <old-parent>`: Rebasing your work off a new parent

## Remotes
* `git add remote upstream <remote-url>`: Configure upstream remote URL for a fork
* `git remote set-url origin <remote-url>`: Change origin remote URL
* `git remote -v`: List currently configure remotes

## Miscellaneous
* `git show <commit>`: Show the commit information for a specific hash
