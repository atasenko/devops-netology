### Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea.

Полный хеш: aefead2207ef7e2aa5dc81a34aedf0cad4c32545

Комментарий: Update CHANGELOG.md

Команда: git show aefea

### Коммит 85024d3 соответствует тегу v0.12.23

Команда: git show 85024d3

### У коммита b8d720 2 родителя. Хеши: 56cd7859e0 9ea88f22fc

Команда: git show b8d720

### Хеши и комментарии всех коммитов, которые были сделаны между тегами v0.12.23 и v0.12.24:

33ff1c03bb (tag: v0.12.24) v0.12.24

b14b74c493 [Website] vmc provider links

3f235065b9 Update CHANGELOG.md

6ae64e247b registry: Fix panic when server is unreachable

5c619ca1ba website: Remove links to the getting started guide's old location

06275647e2 Update CHANGELOG.md

d5f9411f51 command: Fix bug when using terraform login on Windows

4b6d06cc5d Update CHANGELOG.md

dd01a35078 Update CHANGELOG.md

225466bc3e Cleanup after v0.12.23 release

Команда: git log v0.12.23..v0.12.24 --oneline

### Коммит, в котором была создана функция func providerSource:

Хэш 8c928e8358

Команда: git log -S"func providerSource(" --oneline

### Все коммиты, в которых была изменена функция globalPluginDirs:

78b1220558 52dbf94834 41ab0aef7a 66ebff90cd 8364383c35

Казалось бы, достаточно воспользоваться командой "git log -L :globalPluginDirs", но она требует указания имени целевого файла которое мне неизвестно. Не придумал ничего короче чем сначала найти файл, а потом использовать его имя с флагом -L.

Команды: 

git grep -p globalPluginDirs

git log -L ":globalPluginDirs:plugins.go"

### Автор функции synchronizedWriters - Martin Atkins.

Команда git log -S"synchronizedWriters(" выводит три коммита. Автор двух - James Bardin, третьего - Martin Atkins. Логично предположить что автор Martin Atkins т.к. его коммит идет раньше, но я решил дополнительно проверить посмотрев содержимое коммитов. В коммите 5ac311e2a9 функция создается, а в bdfea50cc8 удаляется за ненадобностью.  

git log -S"func synchronizedWriters("
git show 5ac311e2a9
git show bdfea50cc8
