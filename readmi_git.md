#  Инструкция по работе с *Git*

## Что такое *Git*

*Git* - одна из реализаций распреденных систем контроля версий. Самая популярная Git это GitHub.git

**[_GitHub_](https:\\GitHub.com)**

## Подготовка репозитория

Для создания репозитория используется команда git init. Для этого в терминале с открытой папкой, будущем репозитории, необходимо написать *git init*

## Создание фиксаций

### Добавление файла к коммиту

Для того что бы добавить файл к будущему коммиту используется команда *git add*
для этого в терминале с открытой папкой-репозиторием необходимо написать команду 

**git add <имя файла>**

### Выполнение коммита.

Для выполнения коммита используется команда *git commit*. Для этого в терминале с открытой папкой-репозиторием необходимо написать 
git commit -m <сообщение к коммиту>. Сообщениек коммиту писать ОБЯЗАТЕЛЬНО.

## Переключение между фиксациями

Для того что бы перети на другой коммит используется команда *git checkout*. Для этого в терминале с открытой папкой-репозиторием неоходимо написать 
**git checkout <хеш(номмер) коммита>. Хеш(номмер) коммита можно вять из журнала о котором было расказано выше. После выполнения этой команды вы попадете в состояние *Detached head* и какие-либо фиксации не будут ничего изменять. Для возврата в обычное состояние неоходимо написать команду  *git checkout <название ветки в которой вы работали>*

## Журнал изменений

Для просмотра истории изменений используется команда *git log*. Для этого в терминале с открытой папкой-репозиторием необходимо написать **git log**

## Ветки в Git

### Создание новой ветки

Для создания новой ветки используется команда *git branch <имя новой ветки>*
Для этого в терминале с открытой папкой-репозиторием необходимо написать 

**git branch <имя новой ветки>**  
Например так

**git branch new_branch**

### Переход на новую ветку

При создании новой ветки переход на нее НЕ ОСУЩЕСТВЛЯЕТСЯ. Для прехода на созданную ветку (как и на любую другую) используется команда * git checkout*. Для этого в терминале с открытой папкой-репозиторием необходимо написать 
**git checkout <имя ветки на которую нужно перейти>*

Например так 

git checkout new_branch


## Слияние веток и разрешение конфликтов

### Слияние веток

для слияния веток использется команда git merge. Для этого в терминале с открытой папкой-репозиторием необходимо написать **git merge <имя ветки которую надо слить с текущей>**. Ветка из команды будет слита с той в которой вы в данный момент находитесь.

Например если дать команду git merge new_branch находяь в ветке master то ветка с с именем new_branch будет слита с веткой master

### Разрешение конфликтов


Самый простой способ разрешить конфликт - отредактировать файл в редакторе придав ему желаемый вид. После редактирования необходимо выполнить команды

git add <имя редактируемаог файла>

git commit -m "Необходиый и обязательный коментарий"


## Удаление веток в *Git*


Для удаления локальной ветки используется команда *git branch* с ключом -d. Для этого в терминале с открытой папкой-репозиторием необходимо написать 
**git branch -d <имя ветки которую необходимо удалить>**

Например так 

*git branch -d new_branch*

# Работа с удаленными репозиториями

git remote -v
git remote show origin

git clone https://github.com/schacon/ticgit
git remote add [сокращенное имя] [url] добавление удаленного сервера

git fetch [имя удаленного репозитория]
git fetch origin Синхронизация работы с сервером с именем «origin»

git pull
git push [имя удаленного сервера] [ветка1] : [ветка2]  отправка в удаленный репозитарий [имя удаленного сервера] ветки1 котрая там получит имя ветка2 
git push origin --delete serverfix удаление ветки serverfix на сервере origin


