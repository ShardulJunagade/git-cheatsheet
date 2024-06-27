# Get good at git!

When you first set up git on a machine, you are supposed to set your name and email.
```
git config --global user.name "John Doe"
git config --global user.email "johndoe@example.com"
```




## Git Hidden Folder

There is a hidden folder called `.git` which tells you that the project is a git repo.

If we want to create a git repo in a new project we create the repo folder and initialize that folder using `git init`.
```sh
mkdir /workspaces/tmp/new-project
cd /workspaces/tmp/mew-project
git init
touch Readme.md
code Readme.md
# Make changes to readme.md
git status
git commit -a -m "add readme file"
```




## Cloning

We can clone in 3 ways: HTTPS, SSH, Github CLI

Since we are using Github Codespaces, we'll create a temporary directory in our workspace.
```sh
mkdir /workspaces/tmp
cd /workspaces/tmp
```

### HTTPS
```sh
git clone https://github.com/shardul-0109/Github-Examples.git
```


### SSH

```sh
git@github.com:shardul-0109/Github-Examples.git
cd Github-Examples
```
You will need to create ssh key locally and save it to Github.

We can test our connection here:
```sh
ssh -T git@github.com
```


### Github CLI

Install the CLI for Windows
```sh
winget install --id GitHub.cli
```

**Configuration:**

- Run `gh auth login` to authenticate with your GitHub account. Alternatively, gh will respect the `GITHUB_TOKEN` environment variable.

- To set your preferred editor, use `gh config set editor <editor>`.

- Declare your aliases for often-used commands with `gh alias set`.


## Add

When we want to stage changes that will be included in the commit, we use the . to add all changes to the staging area.
```sh
git add Readme.md
git add .
```




## Reset

Reset allows you to move staged changes back to be unstaged.
This is useful when you want to revert all files to the last commit.
```sh
git add .
git reset
```

> git reset will revert git add




## Status

Git status shows you what files will or will not be committed.
```sh
git status
```




## Commits

When we want to commit code, we can write git commit which will open up the commit edit message in the editor of choice.
```sh
git commit
```

You can set the global editor by using the following command.
```
git config --global core.editor code
```

Make a commit and commit message without opening the editor.
```sh
git commit -m "commit message"
```



## Log

`git log` will show the recent commits to the current branch.

`git log --graph` will show recent commits to the current branch in graph format.

`git log --all` will show the commits to all the branches.

`git log --all --graph` will show recent commits to all the branches in graph format.




## Push

When we want to push a repo to our remote origin:
```sh
git push
```
This will ask if we want to login to Github. If declined, we can input our username and personal access token (that we can get from the developer tools in the Github settings) as our password.




## Branches
List of branches:
```sh
git branch
```

Create a new branch:
```sh
git branch <branch-name>
```

Checkout the branch:
```sh
git checkout <branch-name>
```


## Remotes

## Stashing

## Merging

