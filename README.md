# An introduction to git

## Commands

`git init` initializes a new repository with the default branch name
`git status` returns the status of the git repository
`git add` adds the file to the current git repository (in git terms staging)
`git commit <params> <message>` commits the added files helping to revert to previous versions just like a snapshot
`git logs` allows to view commit history
`git checkout <hash / commit id>` checks out to the commit
`git branch <params> <name>`

- `m` changes the default branch name or `m old new` to swap the name
- `no-params` make a new branch or `-b` to checkout to that branch automatically (NOTE: the branch inherits code from the HEAD or you can source `new-branch source-branch`)

`git add remote <origin name> <url>` tells git that we have a remote repository (aliased as origin)
`git push -u <origin> <branch>` pushes a repository to a remote
`git push --set-upstream` is used to sync branches with your HEAD branch pushing to git or you can use the `-u` just like above which will also add the branch to be synced with the HEAD branch
for later on you can just use `git push`
`git pull` pulls updated modifications from the remote

- or  add `origin main` for a specific origin

`git merge <branch> <branch>` merges two branches
`git reset` a means of resetting a branch so a given commit and removing commits after that while deciding to discard or keep the code. it works just like how we did it with `git checkout` but i mentioned that you aren't changing anything rather you are just viewing history

So there are three different ways of using reset

1. You want to uncommit and keep the project staged, lets say you regret not putting everything in a single commit (soft)
2. You want to uncommit and unstage, so you regret having a single commit (mixed)
3. You completely regret these commits happened, and want to remove it from history (hard)

`git revert` is basically resetting a branch to get to code, and keep history clean
just remember to use `git revert --continue` after merging conflicts

## How to make proper commits

Ask yourself the simple question of "If added to the code base, this code will _____". These commits should be imperative, meaning in the sense you are giving order
