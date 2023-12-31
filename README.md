# Как пользоваться git-ом
---
### Вот тебе краткая инструкция по командам
* git init - Инициализиурет git репозиторий в папке
* git add <file> - Добавляет файл в индекс
* git commit -m 'MESSAGE' - Делает коммит с сообщением MESSAGE
* git remote add origin 'URL' - Добавляет удалённый репозиторий с адресом URL
* git push origin 'BRANCH' - Отправляет коммиты в удалённйы репозиторий на ветку BRANCH
* git log - Показвает историю коммитов

#### Основные термины
* HEAD - это указатель на последний коммит в текущей ветке
* Hash - это идентификатор коммита(например как id), который состоит из 40 символов. Если изменения в файле были одиннаковые, то и hash будет одинакковым.

#### Жизненный цикл git

```mermaid
graph LR;
  untracked -- "git add" --> staged;
  staged    -- "git commit"     --> tracked/comitted;
  tracked    -- "modify file"     --> modified;
  modified    -- "git add"     --> staged;

%% стрелка без текста для примера: 
  A --> B;
``` 
