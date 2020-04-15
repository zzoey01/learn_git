# Rebase your branches (WIP)

# Merge Conflicts
While each software development team has its own branching strategy, it is the developer's responsibility to ensure that his local git repository would also consist of his other colleagues' latest work too. Nevertheless, merge conflicts will still occur.

## When and How
Merge conflicts occurs 
- When: Git detects differences in the changes between the 2 branches you are attempting to merge.
- How: The changes made occur on the same line(s) in the same file for both branches.

## Why merge conflicts
Merge conflicts would notify the user of the clashes that occurs during the merging process. It will prompt the developer to resolve the conflicts by doing the following:
- Accept current change: The codes that are from your working copy
- Accept incoming change: The codes that are retrieved from the remote repository
- Accept both changes: Accept both origins of changes and manually make the necessary edit if needed

<small> *Note: The terms used are from Visual Studio Code when resolving merge conflicts. I'm using it to illustrate the source origin of the source codes* </small>

## After resolving and merging
`git merge` would result in a new merge commit. This is to tie the histories of both branches together.
- Pros: It does not change the existing branches
- Cons: The feature branch's history may be polluted from having many irrelevant merge commit, when incorporating the changes from other branches.


## Rebase your branches
Hence, `git rebase` can be used to perform the same function as `git merge` i.e. to integrate changes from one branch to another. There is 2 modes - interactive and manual

However do note that `git rebase` rewrites the history of the branch by creating brand new commits for each commit in the original branch.
- Pros
    1. Cleaner & linear project history
    2. Navigate projects with `git log`, `git bisect` and `gitk`
- Cons
    1. Rewriting project history may cause catastrophic impact for collaboration workflow
    2. May lose context provided by a merge commit, i.e. when did the changes get incorporated into the features.

