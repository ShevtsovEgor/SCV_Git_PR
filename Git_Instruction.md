![Logo](png-transparent-computer-icons-github-github-leaf-logo-grass.png)
# **Работа с Git и GitHub**
## 1. Проверка наличия установленного 
В терминале выполнить команду `git version`.
Если Git установлен появится сообщение с информацией о версии программы, иначе будет сообщение об ошибке.
## 2. Установка Git
Загружаем последнюю версию Git с сайта https://git-scm.com/downloads
Устанавливаем с настройками по умолчанию.
 ## 3. Настройка Git
 При первом использовании Git необходимо представиться. Для этого нужно выполнить в терминале две команды:
 ```
 git config --global user.name "Ваше имя английскими буквами"
 git config --global user.email ваша_почта@example.com
 ```
 ## 4. Инициализация репозитория
 Для создания репозитория выполните команду *git init* и у вас создастся репозиторий (скрытая папка .git).
 ## 5. Запись изменений в репозиторий
 Теперь Git отслеживает изменения файлов вашего проекта. Но, так как вы только создали репозиторий в нем нет вашего кода. Для этого необходимо создать commit. Посмотреть статус файлов — *git status*. Вы увидите, какие файлы изменили, удалили или добавили в проект. При этом статус «Закоммичен» не отобразится. Добавить файлы в индекс — *git add* [название файла]. После ввода этой команды вы можете сделать коммит. Есть похожие команды, например, *git *add* . индексирует сразу все изменённые файлы и папки в директории, где вы находитесь. Обратите внимание, между точкой и словом add нужно ставить пробел. Команда git add :/ добавляет в индекс все файлы независимо от того, в какой директории вы находитесь. Сделать коммит — *git commit* -m "Комментарий к коммиту" — фиксирует изменения. До выполнения этой команды локальные изменения никуда не запишутся. Команда *git diff* используется для вычисления разницы между любыми двумя Git деревьями. Это может быть разница между вашей рабочей директорией и индексом (собственно git diff), разница между индексом и последним коммитом (git diff --staged), или между любыми двумя коммитами (git diff master branchB).
 ## 6. Просмотр истории коммитов
 Для просмотра истории предыдущих коммитов в обратном хронологическом порядке можно использовать команду .git log*.
 ## 7. Перемещение между сохранениями
 Перемещаться между нашими "сохранениями" можно с помощью команды *git checkout*. Для этого достаточно применить команду git checkout <номер коммита>. Вернуться на ветку мастера - *git checkout master*.
 ## 8. Игнорирование файлов
 Для того, чтобы исключить отслеживание репозиториев определённые файлы и папки, необходимо там создать файл ***.gitignore*** и записать в него их названия или шаблоны, соответствующиетаким файлам или папкам.
 ## 9. Создание веток
 Список веток в репозитории можно посмотретьс помощью команды:
```
git branch
```
 Создать ветку можно командой:
```
git branch <название новой ветки>
```
По умолчанию имя основной ветки в Git - это *master*.
Для переключения между ветками используется команда:
```
git checkout <название ветки>
```
Создать новую ветку и сразу перейти на неё можно одной командой:
```
git checkout -b <название ветки>
```
## 10. Слияние веток и разрешение конфликтов
Для слияния выбранной ветки с текущей нужно выполнить команду:
```
git merge <название выбранной ветки>
```
Если в ветках данные отличаются, то программа обнаружит конфликт и предложет сохранить версию текущей ветки или входящей.
![screen](Screenshot_1.png)
Однако, это еще не всё, после разрешения конфликта обязательно необходимо исполнить команду коммита слияния, чтобы зафиксировать разрешение конфликта:
```
git commit -am <текст>
```
![screen](Screenshot_2.png)
## 11. Удаление веток
Команда удаления:
```
git branch -d <название ветки>
``` 
Принудительное удаление:
```
git branch -D <название ветки>
```
ВАЖНО! Нельзя удалить ветку, находясь в ней. Нельзя удалить неслитую ветку.
## 12. Работа с удалёнными репозиториями
1. Создаём акк на GitHub
2. Создать локальный репозиторий
3. Создать удалённый репозиторий
4. Связать удалённый репозиторий с локальнымДобавить удалённый репозиторий к проекту:
```
git remote add <имя для репозитория><url-адрес репозитория в сети>
```
Для получения изменений из удалённого репозитория используется команда `git pull` 
## 13. Документация по Git
https://git-scm.com/docs/user-manual
https://www.atlassian.com/ru/git/tutorials/setting-up-a-repository
https://www.atlassian.com/ru/git/tutorials/saving-changes
https://www.atlassian.com/ru/git/tutorials/inspecting-a-repository
https://www.atlassian.com/ru/git/tutorials/undoing-changes


