# Fetch vs Pull

_**The**_ `git` _**commands that will be used in this exercise are**_ `fetch`, `pull`. _**The optional git command for exposure is**_ `diff`.

`git fetch` and `git pull` are commonly used. The difference in these commands are the effects it has on your working copy.

## `git fetch`
`git fetch` would retrieve latest information about your remote repository, but will NOT download the files and combine with your working copy.

## `git pull`
`git pull` will not only retrieve the latest information about your remote repository, it will also dowload the files and combine with your working copy.


## Mini-exercise
You can test out `git fetch` 
```console
#Check the name of the remote repository
#You should have origin as your remote name
git remote

#Fetch the latest information about your remote repository
git fetch origin

#You can see the difference using `git diff`
git diff
````

## Sources
I took reference from [here](https://www.freecodecamp.org/news/git-fetch-vs-pull/). I attempted to simplify it, but maybe just a little only :X