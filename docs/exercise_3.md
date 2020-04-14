# Branches

It is always good practice to do branching strategy when implementing new features. This is especially critical when working in a software development team. 

I am no expert, so I shall leave it to the experienced/experts to explain. Do look at the links provided! Examples of branching strategy are [Git Flow](https://nvie.com/posts/a-successful-git-branching-model/) or [GitHub Flow](https://guides.github.com/introduction/flow/). Note: GitHub Flow has a nice graphic to explain the flow, do check it out!

## Prerequisites
Please create a text file in your local Git repository.
 
```console
#Create a new file
echo "Hello world" >> new_file.txt
```

## 1. Create branch
You can create a new branch by using `git branch`. It is good practice to keep 1 feature per branch for feature-branching for starters. There are varients of the git flow such as [trunk-based development Git Flow](https://www.toptal.com/software/trunk-based-development-git-flow).
- Note that the branch name must be unique. 
- <unique_branch_name> is a placeholder, replace with whatever name you plan to use for your branch

```console
#To check what existing branches you have
git branch

#Create a branch
git branch <unique_branch_name>

#To switch to your newly-created branch
git checkout <unique_branch_name>
```

## Cheat Code: `git checkout -b`
You can use the following git command to simultaneously create a new branch and will be switched to it automatically

```console
git checkout -b <unique_branch_name>
```


## 2. Stash changes
What if you forgot to switch branches before starting your work? Have no fear, you can use `git stash`!

`git stash` will temporarily store your changes of file into cache. You can also store multiple stashes. You can read up more [here](https://code.tutsplus.com/tutorials/quick-tip-leveraging-the-power-of-git-stash--cms-22988). 

For this exercise, we will focus on a single stash.
```console
#Store your changes into the stash
git stash

#Switch to the intended branch
git checkout <unique_branch_name>

#Apply the changes from the stash to the intended branch
git stash apply

OR

git stash pop
```

## 3. Merge branches
In software development teams, you are typically required to make pull requests or PR in short. For this exercise, we shall merge the branches together without PR to demonstrate `git merge` command. PR will be explained in Beyond Basics section.

