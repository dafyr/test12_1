# test12_1
Круглов Илья Игоревич
Мусор удалялся  git filter-branch 
Клонируем репозиторий и переходим в его каталог:

Удаленим ненужные файлы:

git filter-branch --tree-filter 'rm -f images/*.jpg' HEAD
git filter-branch --tree-filter 'rm -rf folder1’ HEAD

Проведем очистку от мусора:
git reflog expire --expire=now --all && git gc --prune=now --aggressive

Отправим новую историю веток и тегов на сервер:
git push origin --force --all
git push origin --force --tags
