# Create local Git repository 
---

Personally, I would find it easier to use `git clone` than manually create a local Git Repository. 

However, it's good to step through it. This method would expose you to commonly used git commands by developers to manage the version control of their projects

---

## 1. Create via Terminal

_**The**_ `git` _**commands that will be used in this exercise are**_ `init`, `add`, `status`, `commit`, `pull`, `push`.

### I. Create the necessary directory & files
```console

#Create directory that you want your project files to be stored
#In this guide, I named my directory as 
mkdir demo

#Navigate to the demo directory
cd demo

# Create a README.md file and echo the heading
# You can skip this step if you created this inside the remote repository
echo "# Learn Git" >> README.md
```

### II. Initialize the directory into a Git repository
```console
#Initialize the repository
git init
```

### III. Add files into your Git repository
In the previous step, the directory is an empty repository as we have yet to add any files into Git repository for it to track. Let's add the file into the Git repository. 

You can first check the status of the Git repository with `git status`. It will show you with files are being tracked and untracked by the Git repository. Below is the output of `git status`

```console
user@localhost-domain demo % git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)

```

The command below adds a single file. It can also be used when you only want to add certain files into the commit.

```console
#Now, add the README into the repository record
git add README.md

#Selective adding, separated by a space.
git add <file 1> <file 2> ...
```

As there is only a single file now, you can use the following command above. In the future when there are more files, you can use the command below instead to add all files.

```console
git add .
``` 

After adding, you can use `git status` to check again. It should reflect the following output.
```console
user@localhost-domain demo % git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md
```

### IV. Make your 1st commit & link to remote repository
Note that the remote origin added is my repository. Please replace it with your own repository

```console
#Make your first commit!
#Note that the -m allows you to indicate a short commit message
git commit -m "Initial commit"

#Link to remote repository
git remote add origin https://github.com/bernicecpz/learn_git.git

```

I suggest you to read this article on some good practices to [write good commit messages](https://chris.beams.io/posts/git-commit/).  

<small>*Note: In the event you forget to commit first, you will be prompted to either commit your changes or stash them before merging.* `merge` will be explained in detailed under the "Create branches" section.</small>

### V. Push the changes into your master branch
If it is your first commit, it's fine to push directly into your master branch. 

As I already create a file when I created the Git repository in the GitHub page, I will pull from the master branch just to make sure there is no merge conflict.

```console
#Pull files from the master branch to fetch and merge into current commit
git pull origin master

#After pulling successfully, you can push the changes to the remote repository
git push origin master
```

---

## 2. Git Clone
As mentioned earlier, `git clone` is the usual way of creating a duplicate of the remote repository.

Note that the remote origin added is my repository. Please replace it with your own repository
```console
#Navigate to your intended directory
cd <filepath>

#Clone the Git repository into your intended directory
git clone https://github.com/bernicecpz/learn_git.git
```