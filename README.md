# Git-flow
List of commands for working with git from command line.<br />
For example, using Git Bash<br />

#### 1. Getting a ready-made project from git (github).

**1.1.** Create a folder for the project.<br />
Example: git-flow-training.<br />

**1.2.** Go to this folder.<br />
Command: cd путь_до_папки.<br />
Example: cd C:/git-flow-training.<br />
Note: you need to use the right slash<br />

**1.3.** Initialize the local repository.<br />
Command: git init.<br />

**1.4.** Add a remote repository.<br />
Command: git remote add название_репозитория ссылка_на_репозиторий.<br />
Example: git remote add gitFlow https://github.com/AntonMishanin/Git-flow.<br />

**1.5.** Get information about the repository.<br />
Command: git fetch --all.<br />

**1.6.** Перейти на нужную ветку.<br />
Command: git checkout название_ветки.<br />
Example: git checkout develop.<br />

**1.7.** Getting files.<br />
Command: git pull --all.<br />

#### 2. Uploading a project on github.

2.1. Create a new branch<br />
Command: git branch название_ветки<br />
Example: git branch develop<br />

2.2. Go to this branch.<br />
Command: git checkout название ветки.<br />
Example: git checkout develop.<br />
Note: if you don't need a new branch, you can skip items 2.1 and 2.2.<br />

2.3. Add all files to the local repository.<br />
Command: git add --all.<br />

2.4. To commit the changes.<br />
Command: git commit -m "my comments".<br />
Example: git commit -m "Create toolbar".<br />

2.5. Sending to git.<br />
Command: git push -u name_of_the_remote_repository name_of_the_branch.<br />
Example: git push -u gitFlow develop.<br />
Note: name_of_the_remote_repository is from item 1.4.<br />
