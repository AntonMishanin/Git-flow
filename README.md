### Flow работы с гитом:
1. Тим.лид. создает ветки master и develop с ограниченным доступом для пушей.
2. Разработчик каждую задачу делает в отдельной ветке. По готовности, стягивает develop и оформляет merge request.
3. Тим. лид. делает код ревью. Если всё окей, мержит, если нет - делаем правки.
4. Перед тестом делаем релизную ветку и правки после теста делаем в ней. Далее, мержим релиз в мастер и девелоп.
5. Поставить тег(v1.0.0) на мастер. В Readme.md прописать данную версию, описание изменений и ссылку на задачу с разработкой.
6. Соглашение по названию веток:
 - master - хранит релизную версию проекта.
 - develop - текущая рабочая версия проекта.
 - feature-* (feature-settings) - ветки для разработки фич. Вливается в develop.
 - release-* (release-1.0.2) - ветка для правок после теста. Вливается в develop и master.
 - hotfix-* (hotfix-1.0.3) - исправление срочного бага, обнаруженного на продакшене. Берется из мастер, вливается в мастер.
7. Соглашение по написанию коммитов:
 - type (optional scope): description || Заголовок < 50 символов.
 - Пустая строка.
 - optional body || Тело коммита. Содержит «что» и «почему», а не «как»
 - optional footer(s) || Если коммит закрывает задачу, указать ссылка на задачу в Jira.
 - feat — используется при добавлении новой функциональности
 - fix — если исправили какую-то серьезную багу
 - docs — всё, что касается документации
 - style — исправляем опечатки, исправляем форматирование
 - refactor — рефакторинг кода приложения
 - test — всё, что связано с тестированием
8. Соглашение по написанию title и description для merge request:
 - Краткий заголовок
 - Описание
 - Ссылка на задачу Jira
 - Для мерже реквеста релизной ветки: в заголовок пишу версию.
9. Нюансы/вопросы:
 - Нужно ли в коммите указывать название файла или ветки, к которой он относится?
 - Использование --no-ff при мерже?
 - Как пушить в мастер одним коммитом?

Удачная модель ветвления для Git:
https://habr.com/ru/post/106912/

Как следует писать комментарии к коммитам:
https://habr.com/ru/post/416887/


=========
Команды:
 - git commit --amend если нужно отредактировать !последний коммит или поменять его название.
 - git commit --path если нужно закоммитить часть изменений.
 - git commit --fixup если нужно отредактировать !не последний коммит.
 - git rebase --interactive если нужно изменит историю. Поменять местами коммиты, переименовать...
=========


List of commands for working with git from command line.<br />
For example, using Git Bash<br />

#### 1. Getting a ready-made project from git (github).

**1.1.** Create a folder for the project.<br />
Example: git-flow-training.<br />

**1.2.** Go to this folder.<br />
Command: cd folder_path.<br />
Example: cd C:/git-flow-training.<br />
Note: you need to use the right slash<br />

**1.3.** Initialize the local repository.<br />
Command: git init.<br />

**1.4.** Add a remote repository.<br />
Command: git remote add name_of_the_repository link_to_the_repository.<br />
Example: git remote add gitFlow https://github.com/AntonMishanin/Git-flow.<br />

**1.5.** Get information about the repository.<br />
Command: git fetch --all.<br />

**1.6.** Go to the desired branch.<br />
Command: git checkout the_name_of_the_branch.<br />
Example: git checkout develop.<br />

**1.7.** Getting files.<br />
Command: git pull --all.<br />

#### 2. Uploading a project on github.

**2.1.** Create a new branch.<br />
Command: git branch the_name_of_the_branch.<br />
Example: git branch develop.<br />

**2.2.** Go to this branch.<br />
Command: git checkout the_name_of_the_branch.<br />
Example: git checkout develop.<br />
Note: if you don't need a new branch, you can skip items 2.1 and 2.2.<br />

**2.3.** Add all files to the local repository.<br />
Command: git add --all.<br />

**2.4.** To commit the changes.<br />
Command: git commit -m "my comments".<br />
Example: git commit -m "Create toolbar".<br />

**2.5.** Sending to git.<br />
Command: git push -u name_of_the_remote_repository name_of_the_branch.<br />
Example: git push -u gitFlow develop.<br />
Note: name_of_the_remote_repository is from item 1.4.<br />

#### 3. My list of commands

 - git log looking at commits/ / information about the commit
 - clear 
 - git status
 - git checkout ...
 - git branch list of branches
 - git branch develop -creates a branch develop
 - git commit -m "New commit"
 - git add . Add all files
 - ls list of files in the initialized repository
 - git diff looking at changes in files
 - git pull getting files from github
 - git checkout the_name_of_the_branch - move to another branch
 - git push --all throwing and creating a new branch on github
 - git merge ветку - infuses the branch that we specify in the current branch
 - git branch -d the_name_of_the_branch - delete branch
 - git fetch - pulls information about a remote repository(without code)
 - git push -f origin develop
 - git push --all
 - git push -u origin master
 - git fetch --all getting files without the change tree
 - git pull --all getting files with the change tree

#### 4. My list of errors

**4.1.** action: git remote add...(item 1.4).<br />
fatal: remote origin already exists.<br />
solution:git remote rm origin<br />
and repeat<br />

Remove the cache of all the files
 - git rm -r --cached .

Remove the cache of specific file
 - git rm -r --cached <file_name.ext>
