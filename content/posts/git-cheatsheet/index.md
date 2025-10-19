---
title: "Git Cheat Sheet"
date: 2025-10-19
draft: false
summary: "Useful cheat sheet for git"
tags: ["coding","git"]
---

## Create a Local Repo

1. (optional) `mkdir` to create the project dir
2. `cd` to the project dir
3. `git init`
4. ***Don't forget to create `.gitignore` if needed!!!***\
Use this repo to find the template you need👉[https://github.com/github/gitignore](https://github.com/github/gitignore)

## Clone a Remote Repo

1. Copy the url
2. `git clone <url>`\
**Note**: If you just want the current content of the repo instead of all its history, use `--depth=1`

## Initial Commit

1. ***Make sure you have correctly configured the `.gitignore` file!!!***
2. `git add .`
3. `git commit -m "Initial Commit"`

## Daily Commit

1. cd to root dir
2. Don't forget to `git add .`!
3. `git status` to review the changes
4. Always `git commit -m` with a short, meaningful message.

## Daily Push

1. `git push origin <branch-name>`

## Daily Pull

1. Make sure you have correctly configured the remote repo using `git remote -v`
2. `git fetch` first
3. `git pull origin <branch-name>`\ If your repo has untracked/committed/pushed changes, the action will fail. use `--force` if you want to discard all local changes.

## Cancel the Most Recent Commit

1. `git log` first to make sure what do you want to cancel
2. Choose `git reset <commit>` or `git revert <commit>`. `git revert` is preferred because it will create a new commit and will not affect the history.\
**Do You Know?** `HEAD^` means the former commit of `HEAD`.

## Create a new Branch

1. `git branch -a` to see all existing branches. Branch name with a `*` means you are currently on this branch.
2. `git switch -c <new-branch-name>` to create and switch to a new branch.\
**Note**: Branch names should be meaningful as well.