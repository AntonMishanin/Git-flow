# Git-flow
List of commands for working with git from command line.
Например, с использованием Git Bash

Получение готового проекта с гит

1. Создать папку для проекта
Пример: git-flow-training

2. Перейти в эту папку
Комманда: cd путь_до_папки
Пример: cd C:/git-flow-training
Внимание: Нужно использовать правый слэш

3. Инициализировать локальный репозиторий
Комманда: git init

4. Добавить удаленный репозиторий
Комманда: git remote add название_репозитория ссылка_на_репозиторий
Пример: git remote add gitFlow https://github.com/AntonMishanin/Git-flow

5. Получить информацию о репозитории
Комманда: git fetch --all

6. Перейти на нужную ветку
Комманда: git checkout название_ветки
Пример: git checkout develop

7. Получить файлы
Комманда: git pull --all