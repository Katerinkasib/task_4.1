[<- К содержанию>](readme.md)

### 2.5 Операции отмены

`git commit --amend` перезаписывает коммит.

Чтобы перезаписать коммит надо сделать так:
`git commit -m "описание файла"`
`git add <новый файл>`
`git comit --amend`

#### Отмена индексации
Если файл уже добавлен в индекс и нужно отменить индексацию, то можно следовать подсказкам git

`git reset HEAD <файл>` или `git restore --stage <файл>`

#### Отмена изменений в файле

`git checout -- <файл>` или  `git restore <файл>` вернет файл к состоянию прежнего коммита, т.е отменит изменения. Все изменения будут безвозвратно утрачены.

[<- Назад](watch-history.md)

[Вперед ->](working-with-remotes.md)



