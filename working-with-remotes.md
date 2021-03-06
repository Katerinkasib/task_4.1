[<- К содержанию](readme.md)

### 2.6 Работа с удалёнными репозиториями

#### Просмотр удалённых репозиториев

`git remote` выдаст список настроенных, удалённых репозиториев.

`git remote -v` выдаст адреса для чтения и записи, привязанные к репозиторию.

но `git remote` и `git remote -v` не дают никакой информации о правах доступа.

#### Добавление удалённых репозиториев

`git remote add <название> <url>` добавить удалённый репозиторий и присвоить ему имя.

#### Получение изменений из удалённого репозитория — Fetch и Pull

`git fetch <название удаленного репозитория>` Данная команда связывается с указанным удалённым проектом и забирает все те данные проекта, которых у вас ещё нет. После того как вы выполнили команду, у вас должны появиться ссылки на все ветки из этого удалённого проекта, которые вы можете просмотреть или слить в любой момент.

Когда вы клонируете репозиторий, команда `clone` автоматически добавляет этот удалённый репозиторий под именем «origin». Таким образом, `git fetch origin` извлекает все наработки, отправленные на этот сервер после того, как вы его клонировали (или получили изменения с помощью `fetch`). Важно отметить, что команда `git fetch` забирает данные в ваш локальный репозиторий, но не сливает их с какими-либо вашими наработками и не модифицирует то, над чем вы работаете в данный момент. Вам необходимо вручную слить эти данные с вашими, когда вы будете готовы.

 Команда `git pull` выдаёт предупреждение, если настройка `pull.rebase` не установлена. Git будет выводить это предупреждение каждый раз пока настройка не будет установлена.

Если хотите использовать поведение Git по умолчанию (простое смещение вперёд если возможно — иначе создание коммита слияния): `git config --global pull.rebase "false"`

Если хотите использовать перебазирование при получении изменений: `git config --global pull.rebase "true"`

#### Отправка изменений в удаленный репозиторий (Push)

`git push <remote-name> <branch-name>` позволит отправить изменения в удаленный репозиторий. Чтобы отправить вашу ветку `master` на сервер `origin` (повторимся, что клонирование обычно настраивает оба этих имени автоматически), вы можете выполнить следующую команду для отправки ваших коммитов: `git push origin master`

Эта команда срабатывает только в случае, если вы клонировали с сервера, на котором у вас есть права на запись, и если никто другой с тех пор не выполнял команду `push`. Если вы и кто-то ещё одновременно клонируете, затем он выполняет команду `push`, а после него выполнить команду `push` попытаетесь вы, то ваш `push` точно будет отклонён. Вам придётся сначала получить изменения и объединить их с вашими и только после этого вам будет позволено выполнить `push`.

#### Удаление и переименование удалённых репозиториев

`git remote rename <исходное название репозитория> <новое название репозитория>` позволит переименовать репозиторий.
Это также изменит имена удалённых веток в вашем репозитории.

#### Просмотр удаленного репозитория

`git remote show <название удаленного репозитория>` покажет более подробную информацию чем `git remote`.
Данная команда показывает какая именно локальная ветка будет отправлена на удалённый сервер по умолчанию при выполнении `git push`. Она также показывает, каких веток с удалённого сервера у вас ещё нет, какие ветки всё ещё есть у вас, но уже удалены на сервере, и для нескольких веток показано, какие удалённые ветки будут в них влиты при выполнении `git pull`.

[<- Назад](undoing-things.md)

[Вперед ->](tagging.md)