
[<- К содержанию](readme.md)
### 1.3 Настройка

Чтобы посмотреть все установленные настройки и узнать где именно они заданы, используйте команду:
```
git config --list --show-origin

```

После установки GIT необходимо указать ваше имя и адрес электронной почты.
```
git config --global user.name "John Doe"
it config --global user.email johndoe@example.com
```
Eсли указана опция --global, то эти настройки достаточно сделать только один раз.
Если для каких-то отдельных проектов вы хотите указать другое имя или электронную почту, можно выполнить эту же команду без параметра `--global` в каталоге с нужным проектом.

Параметры установки окончаний строк для пользователей Unix и Mac:

```
git config --global core.autocrlf input
git config --global core.safecrlf warn
```
Параметры установки окончаний строк Для пользователей Windows:

```
git config --global core.autocrlf true
git config --global core.safecrlf warn
```
Установка отображения unicode:
```
git config --global core.quotepath off
```


[<- Назад](install_git.md)

[Вперед ->](help-git.md)