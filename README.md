# Getting a Git Repository

## Initializing a Repository in an Existing Directory
git init

## Cloning an existing repository
git clone <url>

# Recording Changes to the Repository

## Checking the Status of Your Files
git status

## Tracking New Files
echo 'My Project' >> README
git add README

## Viewing Your Staged and Unstaged Changes

### To see what you've changed but not yet staged
git diff

### To see what you've staged that will go into your next commit
git diff --staged

### Committing Your Changes
git commit -m "<message>"

### Skipping the Staging Area
git commit -a -m "<message>"

### Moving files
git mv file_from file_to
