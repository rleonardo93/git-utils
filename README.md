# Getting Started

## Getting a Git Repository

### Initializing a Repository in an Existing Directory
```git init```

### Cloning an existing repository
```git clone <url>```

## Recording Changes to the Repository

### Checking the Status of Your Files
```git status```

### Tracking New Files
```echo 'My Project' >> README```
```git add README```

### Viewing Your Staged and Unstaged Changes

### To see what you've changed but not yet staged
```git diff```

### To see what you've staged that will go into your next commit
```git diff --staged```

### Committing Your Changes
```git commit -m "<message>"```

### Skipping the Staging Area
```git commit -a -m "<message>"```

### Moving files
```git mv file_from file_to```


## Viewing the Commit History

### Lists the commits made
```git log```

#### Patch option shows the difference
```git log --patch```

```git log --pretty=format:"%h - %an, %ar : %s"```

Useful specifiers: https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History#pretty_format

### Limiting Log Output

#### Only show commits with a commit message containing the string.
```git log --grep "<string>"```

#### Only show commits adding or removing code matching the string.
```git log -S "<string>"```

Options to limit the output: https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History#limit_options

## Undoing Things

### Undo something
```git commit -m "Initial commit"```
```git add forgotten_file```
```git commit --amend```

**Note:** Only amend commits that are still local and have not been pushed somewhere.

### Undoing things
```git restore```
```git restore --staged```

## Working with Remotes

### Showing Your Remotes
```git remote -v```

### Adding Remote Repositories
```git remote add pb <url>```
```git fetch pb```

### Fetching And Pulling from Your Remotes
```git fetch <remote>```

### Pushing to Your Remotes
```git push orign main```

### Inspecting a Remote
```git remote show origin```

### Renaming and Removing Remotes
```git remote rename pb paul```
```git remote renome paul```

## Tagging

### Listing  Your Tags
```git tag```
```git tag -l "v1.8.5.*```

### Creating Tags
Git supports two types of tags: lightweght and annotated

#### Lightweight
A lightweight that is just a pointer to a specific commit.

#### Annotated Tags
A annotated tag is stored as full object in the Git database.
```git tag -a v1.4 -m "my version 1.4"```

To see the tag data along with the commit
```git show v1.4```

### Sharing Tags
```git push origin v1.5```
``` git push origin --tags```

### Deleting Tags
```git tag -d <tagname>```

### Checking out Tags
```git checkout v2.0.0```

# Git Branching

## Creating a New Branch
```git branch testing```

**Note:** To know what branch you're currently on, there is a special pointer called HEAD.
```git log --oneline --decorate```

## Switching Branches
```git checkout testing```

## Branching Management

### Get list of branches
```git branch```
```git branch --all```

See the last commit on each branch
```git commit -v```

See the branches that you have or have not yet merged into the branch you're currently on
```git branch --merged```
```git branch --no-merged```
