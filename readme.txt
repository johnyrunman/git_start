Comands

git init - создание репозитория

git config --global user.name "Pavel Yaschuk" - прописываем имя пользователя

git config --global user.email "pyaschuk@gmail.com" - прописываем емейл пользователя

git config --list - просмотр конфига

для игнорирования файлов и каталогов нужно в корне гит репозитория создать файл с именем .gitignore и в него прописать те элементы которые должны игнорироваться
#комментарий
logs/
если прописать:
logs/*.txt - то в даном каталоге будут игнорироваться все файлы с расширением .txt

git status - отображает статус файлов, которые будут записываться в репозиторий, которые изменялись и т.д.

cd docs - переход в гите в папку докс

git status --untracked-files=all - отображает все файлы которые не синхронизированы

git add . - добавить все файлы для контроля (кроме тех что в игноре)

git rm --cached license.txt - удаление файла из контроля

git commit -a -m "init" - комит (заброс в базу изменений)

git add license.txt - добавление одиночного файла в контроль(трек)

комитится то, что проиндексировано

git add how.txt - проиндексировать файл

git add "*.php" - проиндексировать все файлы с расширением пхп

git checkout -- license.txt - откатить лицензию к предыдущему коммиту

git log - история коммитов

q - выход в консоль

git help log - справка по команде лог

git log --pretty=format:"%h - %an, %ar : %s" - лог в коротком формате

git log --since=2.weeks - лог коммитов за последние две недели

git log -p -2 - отображает изменения в двух последних коммитах

git commit - без ключей запускает редактор комментариев в редакторе (вим)

git config --global core.editor "'C:\Program Files (x86)\Notepad++\notepad++.exe' -multiInst -notabbar -nosession -noPlugin"﻿ - использование стороннего редактора для комментариев

git checkout -b new_f - создает новую ветку нью_ф и стразу переходит в нее

git branch new_branch - создание новой ветки без переключеня

прописываем метод мержа - git config --global merge.tool kdiff3

подключаем kdiff3 - git config --global mergetool.kdiff3.cmd '"C:\Program Files\KDiff3\kdiff3.exe" $BASE $LOCAL $REMOTE -o $MERGED'﻿

git merge [branch_name] - для того чтобы смержить ветки, нужно перейти в нужную ветку, иа в поле [branch_name] указать имя ветки с которой будем мержиться

git mergetool - начать процесс мержа

git remote - просмотр удаленных репозиториев

git remote -v - просмотр удаленных репозиториев вместе с путем

git push origin [branch_name] - запушить на удаленный сервер, где оригин и есть удаленный сервер, а [branch_name] имя ветки

git push - залить на сервер

git config --global push.default matching - записываем в конфиг пуш всех веток

git fetch - подгрузить данные с сервера

git pull - загрузить данные в локальный репозиторий

Чтобы перейти к нужному коммиту вводим git log --pretty=format:"%h - %an, %ar : %s"(короткий формат лога) после чего вводим git checkout [commit_id] где [commit_id] это первые семь символов идентификатора коммита

Чтобы вернуться на предыдущий коммит нужно ввести git checkout -
