## Git Hidden Folder
`.git` This tells you that the folder is a git repository.

If we wanted to create a git repository in a 
new project we create the project and then we
initilize the repository

```
mkdir /workspaces/tmp/new-project
cd /workspaces/tmp/new-project
git init
touch Readme.md
code Readme.md
git status
git add Readme.md
# Make changes to readme.md
git commit -a -m "add readme file"
```

## Cloning

We can clone: HTTPS, SSH and Github CLI

Since we are using codespace we will create a
temporary directory  in our workspace

``` sh
mkdir /workspaces/tmp
cd /workspaces/tmp
```

##HTTPS
``` sh
git clone https://github.com/LuisDavidAsmat/ToPractice.git
cd ToPractice
```

>You will need to generate a Personal Access Token (PAT)

- Give it access to contents for commit

## SSH

```sh
git clone git@github.com:LuisDavidAsmat/ToPractice.git
cd ToPractice
```

We will need to create our own SSH rsa key pair

```sh
sshe-keygen -t rsa
```

We can test our connection here:
```
ssh -T git@github.com
```

For WSL users and if you create a non defaul key you
might need to add it

### Github CLI

Install the CLI

```
gh auth login
gh repo clone LuisDavidAsmat/ToPractice
```

## Commits

Commit will open up the commit edit message in
the editor of choice

```sh
git commit
```

In local machine, you have to set the global editor

```
git config --global core.editor emacs
```

Commit without opening editor

```sh
git commit -m "added another exclamation mark"
```

## Branches

List of branches

```
git branch
```

Create a new branch
```
git branch dev
```

## Remotes

## Stashing

## Merging

## Add

When we want to stage changes that will be included
in the commit. We can use . to add all possible files

```
git add Readme.md
git add .
```

## Reset

Reset allows you to move staged changes to be 
unstaged. Useful for reverting commited files

```
git add .
git reset 
```

>git reset will revert a git add .

## Status

`git status` shows you which files will or will 
not be commited

```
git status
```

## Git config 

The `git config` file is what stores your global
configuration for email, name, edito and more.

Showing the contents of .gitconfig file
```
git config --list
```

When you first configure git you are suppose to
configure your email, name, editor, etc.

```sh
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

## Log 

Git log will show recent commits to the git tree

## Push

when we want to push a repo to our remote origin

```
git push 
```