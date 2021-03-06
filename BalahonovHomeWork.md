# Работа с Git

## 1. Проверка наличия установленного Git
В терминале выполнить команду `Git version`.
Если Git установлен появится сообщение о версией программы. Иначе будет сообщение об ошибке.
## 2. Установка Git
Загружаем последнюю версию Git с сайта https://git-scm.com/downloads.
Устанавливаем с настройками по умолчанию.
## 3. Насторойка Git
При первом использовании Git необходимо представиться. Ддя этого нужно ввести в терминале две команды:
```
git config --global user.name «Ваше имя»
git config --global user.email ваша "почта@example.com"
```
## 4. Инициализация репозитория
Получить репозиторий можно двумя способами: 
* Клонировать `git clone`
* Создать папку и инициалазировать в нем репозиторий с помощью команды `git init`
## 5. Основные комманды Git
* После инициализации репозитория с помощью команды `git init` используем команду `git status` которая показывает текущее состояние гита, есть ли изменения, которые нужно закоммитить (сохранить).
* На следующем шаге добавляем содержимое рабочего каталога в индекс для последующего коммита с помощью команды `git add file_name`.
* Для фиксации изменений в файле используем команду `git commit`, которая берёт все данные, добавленные в индекс с помощью git add, и сохраняет их слепок во внутренней базе данных, а затем сдвигает указатель текущей ветки на этот слепок.
* Для того чтобы увидеть разнцу между текущей версией и сохраненной используем команду `git diff`.
* Команда `git log` отображает журнал изменений в хронологическом порядке.
* Для перемещения между версиями (коммитами или ветками) воспользуемся командой `git checkout commit_number or branch_name`.
## 6. Ветки в Git и их использование на практике
* `git branch` выводит список веток в репозитории.
* `git branch new_branch_name` создает новую ветку с именем new_branch_name.
* `git branch -d new_branch_name_to_delete` удаляет ветку с именем new_branch_name.
* `got log --graph` выводит список ввиде красивого графа.
* `git checkout branch_name` переход на ветку branch_name.
* `git checkout branch_name` переход на ветку branch_name.
* `git merge branch_name` - сливает веткку с именем branch_name с текущей веткой.

В данном руководстве описаны основные команды Git!
## 7. Работа с удаленными репозиториями
* `git clon https://...` - позволяет склонировать внешний репозиторий на наш компьютер.
* `git pull` - позволяет скачать все из текущего репозитория и автоматически
сделать merge с нашей версией.
* `git push` - позволяет отправить нашу версию репозитория на внешний
репозиторий, требует авторизации на внешнем репозитории.

### Для того чтобы сделать `pull request` нужно:
* Делаем fork репозитория.
* Делаем clone СВОЕЙ версии репозитория.
* Создаем новую ветку и в НЕЕ вносим свои изменения.
* Фиксируем изменения (делаем коммиты).
* Отправляем свою версию в свой GitHub.
* На сайте GitHub нажимаем кнопку pull request.