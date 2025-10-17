# An introduction to git

## Commands

`git init` initializes a new repository with the default branch name
`git status` returns the status of the git repository
`git add` adds the file to the current git repository
`git commit <params> <message>` commits the added files helping to revert to previous versions just like a snapshot
`git logs` allows to view commit history
`git checkout <hash / commit id>` checks out to the commit
`git branch <params> <name>`

- `m` changes the default branch name or `m old new` to swap the name
- `no-params` make a new branch or `-b` to checkout to that branch automatically (NOTE: the branch inherits code from the HEAD or you can source `new-branch source-branch`)


`git add remote <origin name> <url>` tells git that we have a remote repository (aliased as origin)
`git push -u <origin> <branch>` pushes a repository to a remote
