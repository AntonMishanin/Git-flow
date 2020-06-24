# Git-flow
List of commands for working with git from command line.
For example, using Git Bash

###### 1. Getting a ready-made project from git (github).

1.1. Create a folder for the project.
Example: git-flow-training.

1.2. Go to this folder.
Command: cd путь_до_папки.
Example: cd C:/git-flow-training.
Note: you need to use the right slash

1.3. Initialize the local repository.
Command: git init.

1.4. Add a remote repository.
Command: git remote add название_репозитория ссылка_на_репозиторий.
Example: git remote add gitFlow https://github.com/AntonMishanin/Git-flow.

1.5. Get information about the repository.
Command: git fetch --all.

1.6. Перейти на нужную ветку.<br />
Command: git checkout название_ветки.<br />
Example: git checkout develop.<br />

1.7. Getting files.\
Command: git pull --all.\

###### 2. Uploading a project on github.\

2.1. Create a new branch\
Command: git branch название_ветки\
Example: git branch develop\

2.2. Go to this branch.
Command: git checkout название ветки.
Example: git checkout develop.
Note: if you don't need a new branch, you can skip items 2.1 and 2.2.

2.3. Add all files to the local repository.
Command: git add --all.

2.4. To commit the changes.
Command: git commit -m "my comments".
Example: git commit -m "Create toolbar".

2.5. Sending to git.
Command: git push -u name_of_the_remote_repository name_of_the_branch.
Example: git push -u gitFlow develop.
Note: name_of_the_remote_repository is from item 1.4.
