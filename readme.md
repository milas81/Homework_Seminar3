# Инструкция для работы с Git и удалёнными репозиториями (Homework3)

## Что такое Git?
Git - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.
## Подготовка репозитория
Для создание репозитория необходимо выполнить команду *git init*  в папке с репозиторием и у Вас создаться репозиторий (появится скрытая папка .git)

## Создание коммитов

### Git add
Для добавления измений в коммит используется команда *git add*. Чтобы использовать команду *git add* напишите *git add <имя файла>*

### Просмотр состояния репозитория
Для того, чтобы посмотреть состояние репозитория используется команда *git status*. Для этого необходимо в папке с репозиторием написать *git status*, и Вы увидите были ли измения в файлах, или их не было.

### Удаленные репозитории
Удаленный реозиторий для Git создается на сервисе GitHub.
Перейдите на https://github.com и войдите в свой аккаунт. Нажмите кнопку New repository (Новый репозиторий). На открывшейся странице введите имя репозитория (Repository name) и нажмите кнопку Create repository.
В своем локальном репозитории теперь выполните команду:
**git remote add origin _https://github.com/username/myproject.git_**

Данная команда добавит удаленный репозиторий с именем origin, который указывает на ваш Github-репозиторий. Пока мы только добавили запись об удаленном репозитории.

Теперь можно выполнить команду git push, чтобы отправить все ваши изменения на удаленный репозиторий: **git push -u origin master**

Для совместной работы над проектами Git требуются навыки управления удален-
ными репозиториями. Удаленные репозитории представляют собой версии проекта,
хранимые в Интернете или где-то в сети. Их может быть несколько, и каждый в
общем случае доступен вам только для чтения или же для чтения и записи.
Для создания копии репозитория на компьютере пользователя используется команда **git clone _адрес репозитория_**
Команда **git clone** автоматически настраивает вашу локальную ветку master на слежение за удаленной веткой master (она может иметь и другое имя) на сервере, с которого вы выполняли клонирование.

Команда **git pull** будет автоматически извлекать информацию из удаленной ветки и выполнять слияние с текущей веткой. В некоторых случаях такой порядок вещей оказывается проще и удобнее. В общем случае команда **git pull** извлекает данные с сервера, который вы клонировали, и автоматически пытается слить их с вашим текущим рабочим кодом.

Чтобы поделиться результатами своего труда, их нужно отправить в репозиторий.
Это делается простой командой **git push [имя удаленного сервера] [ветка]**. Для
отправки ветки master на сервер origin (еще раз напоминаем, что в процессе кло-
нирования эти имена присваиваются автоматически) следует написать:
**$ git push origin master**
Команда сработает только при условии, что клонирование осуществлялось с сервера, где у вас есть доступ на запись, и за это время никто не отправлял туда свои
данные. Если вы выполнили клонирование одновременно с другим пользователем
и он уже отправил результаты своей работы на сервер, ваша попытка отправки
данных окончится неудачей. Вам сначала нужно скачать все добавленное этим
пользователем и встроить это в свои данные, и только после этого появится возможность воспользоваться командой push.


### Создание коммитов
Для того, чтобы создать коммит(сохранение) необходимо выполнить команду *git commit*. Выполняется она так: *git commit -m "<сообщение к коммиту>*. Все файлы для коммита должны быть ***ДОБАВЛЕНЫ*** и сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО***.
Git commit --amend — добавляем поэтапные изменения в последний коммит.
Чтобы просмотреть все коммиты в текущей ветке в сокращенном виде, есть команда git log --oneline.
Для просмотра всех коммитов в текущей ветке используем команду git log.


## Перемещение между сохранениями
Для того, чтобы перемещаться между коммитами, используется команда *git checkout*. Используется она в папке с пепозиторием следующим образом: *git checkout <номер коммита>*

## Журнал изменений
Для того, чтобы посмтреть все сделанные изменения в репозитории, используется команда *git log*. Для этого достаточно выполнить команду *git log* в папке с репозиторием

## Ветки в Git

### Создание ветки

Для того, чтобы создать ветку, используется команда *git branch*. Делается это следующим образом в папке с репозиторием: *git branch <название новой ветки>*

## Слияние веток

Для того чтобы дабавить ветку в текущую ветку используется команда *git merge <name branch>*

## Удаление веток
Для удаления ветки ввести команду "git branch -d 'name branch'"