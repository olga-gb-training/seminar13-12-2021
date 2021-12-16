# Инструкция по работе с Git и удаленными репозиториями

## Что такое Git?
Git - это одна из реализаций распределенных систем контроля версий, имеющих как и локальные, так и удаленные репозитории. Является самой популярной реализацией систем контроля в мире.
## Подготовка репозитория

Для создания репозитория неоьходимо выполнить команду *git init* в папке с репозиторием и у Вас создасться репозиторий (появится скрытая папка .git) 

## Создание коммита

### Git add
Для добавления изменений в коммит используется команда *git add*. Чтобы использовать команду *git add <имя файла>*

### Создание коммитов

### Для того,чтобы создать коммит (сохранение) необходимо выполнить команду *git commit*. Выполняется она так: *git commit --m "<сообщение к коммиту>*. Все файлы для коммита должны быть ***ДОБАВЛЕНЫ*** и сообщение к комиту писать ***ОБЯЗАТЕЛЬНО***.

## Просмотр состояния репозитория
Для того, чтобы посмотреть состояние репозитория используется команда "git status". Для этого необходимо в папке репозитория написать команду "git status", после чего можно увидеть информацию о произошедших измененияз или их отсутствии

## Журнал изменений

Git позволяет отследить все изменений, произведенные в файле. Для того,чтобы из просмотреть достаточно применить в папке репозитория команду *git log*. После ее применения появляется возможность увидеть все имеющиеся коммиты.

## Перемещение между сохранениями

У каждого коммита есть свой уникальный идентификационный номер. Для того, чтобы переместиться между сохранениями (commit), необходимо для начала применить в папке репозитория команду *git log*, с помощью которой можно увидеть все имеющиеся сохранения.
Чтобы переключиться из одного коммита в другой нужно воспользоваться командой *git checkout <номер коммита, к которому осуществляется переход>*. При этом копировать весь идентификатор желаемого коммита нет необходимости, достаточно скопировать __первые несколько символов__. 

## Ветки в Git
### Создание ветки
В процессе разработки нового функционала программного продукта возникает необходимость разделения рабочего файла на оригинальную версию и ее копии. этот процесс называется **ветвление**. Для того, чтобы создать новую ветку в репозитории нужно в папке репозитория применить команду *git branch <имяветки>*. Чтобы перейти от одной ветки к другой в Git используется команда *git checkout <имяветки>*. После выполнения данной команды можно убедиться, что переход на новую ветку завершен с помощью команды *git branch*.

## Слияние веток

Чтобы объединить требуемые ветки необходимо:
+ перейти на основную ветку *master*;
+ далее применить команду *git merge <имяветки>*

Бывает, что при слиянии веток происходит конфликт между текущей локальной веткой и веткой, с которой происходит слияние. В этом случае Git предлагает инструменты для принятия решения о редактировании и устранении конфликта:
1. Принять текущие изменения
2. Принять входящие изменения
3. Принять оба изменения
4. Сравнить изменения

## Удаление веток

Ветки, которые больше не нужны, можно удалить. Для этого необходимо применить команду *git branch -d <имяветки>*.
