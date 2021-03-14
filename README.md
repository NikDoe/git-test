# GIT-TEST  
</br>

этот репозиторий был создан с целью ознанкомления со всеми тонкостями при работе с системой конроля версия `GIT`. Данный репозиторий могут использовать в дальнейшем новички в качестве мануала.  
</br> 

# УСТАНОКВКА  
</br>  

1. [ скачать можно на официальном сайте ](https://git-scm.com/downloads)
2. после установки выберите папку с которой хотите работать, нажмите правой кнопкой мыши, и выберите `Git Bash`
3. либо же можете открыть с помощью редактор кода, к примеру `VS CODE`, после чего выбрав вкладку терминал запустить консоль в редакторе.  

</br> 
</br>

# БАЗОВЫЕ КОМАНДЫ ПРИ РАБОТЕ С КОНСОЛЬЮ  
</br>  

> значени указанные в <> пишутся без этих скобок

1. `mkdir <название-папки>` - создать папку  
2. `ls` - показать все файлы в этой папке
3. `ls -Hidden` - показать скрытые папки (для powershell), для GIT BASH  `ls -a`
4. `cd  <название-папки>` - перейти в данную папку (можно указывать целый путь)
5. `cd  ..` - вернуться в предыдущую папку
6. `clear` - очистить консоль

</br> 
</br>

# БАЗОВЫЕ КОМАНДЫ GIT 
</br> 

1. `git config --local user.name <имя пользователя>` - заносим юзера который будет работать с данным проектом
2. `git config --global user.name <имя пользователя>` - заносим юзера глобально, т.е. при создании нового проекта GIT подхватывает глобальные данные в первую очередь, если требуется поменять пользователя для этого проекта мы можем написать с ключем `--local`
3. `git config --global user.email "email@mail.домен"` - заносим глобально почту нашего юзера
4. `git config --remove-section user` -  удалить всю секцию с данным юзера  

</br> 
</br>

# ALIAS

здесь будут представлены сокращения для команд, гит, а так же для целой группы команд
</br> 
</br> 

## чтобы создать alias
</br> 

> git config --global alias.сокращение команда гит --- для одной команды
</br>

> git config --global alias.сокращение '!команда гит; команда гит'  

</br>

# мой список alias
</br>

> `s` - git status


</br>
</br>

# GIT КОМАНДЫ ДЛЯ РАЗРАБОТКИ
</br>

1. `git init` - создание локального репозитория
1. `git status`- проверка на изменения в проекте, покажет какие файлы были созданы или изменены, но еще не проиндексированы
1. `git add <имя-файла>` - индексирование файла, либо папки, либо отдельной файла в папке( папка/файл )
1. `git add .` - индексирование из текущей дерриктории
1. `git commit` - добавления файла в репозиторий, необходимо будет ввести заголовок коммита в первой строе, и далее после пустой строк написать какие-то доплнительные сведения
1. `git commit -m"<заголовок-коммита>"`  - флаг `-m` позволяет писать заголовок коммита прямо в терминале

      * комиты лучше делать после каждого изменения

      * заголовок коммита обычно пишут в следущем стиле `характер выполненый работы(над каким компоненотом проводилась работа): краткое описание того что было сделано`

1. `git commit -a` - флаг `-a` позволяет сразу же коммитить из рабочей директории без `git add`, но только уже проиндексированные файлы, файлы которые ещё только созданы и не отслеживают не закомитятся

1. `git commit <папк/папка/...>` - закомитит без `git add` только файлы из этой дирректории
1. `git branch` - просмот всех веток проекта, подсвечена будет та ветка, на которой мы находимся в текущий момент
1. `git branch -v` - содержит всю иноформацию (текущая ветка, идендификатор коммита  последнего на этой ветке, и заголовок коммита)
1. `git branch <название ветки>` - создаст новую ветку, но не переключиться на неё
1. `git checkout <название ветки>` - переключиться на эту ветку
1. `git checkout -b <имя ветки>` - создаст ветку новую, и одновременно на неё переключиться
1. `git branch` - просмот всех веток проекта, подсвечена будет та ветка, на которой мы находимся в текущий момент
1. `git checkout -f <название-ветки>` - в данном случае мы заставим гит переключиться и все незакомиченные изменения пропадут

      * можно и не указывать название ветки, тогда гит откатит на момент когда мы ещё не вносили никаких изменений, там где сейчас находится HEAD

1. `git stash` - отменим изменения, но при этом гит их заархивирует
1. `git stash pop` - вернем заархивированные изменения

      * чтобы не возникало конфликтов, не рекомендуется применять отмененые изменния на другой ветке

      * всегда важно смотреть где мы сделал stach и где мы его применяем

1. `git branch -f <название-ветки> <индекс-коммита>` - перенести ветку на момент комита
1. `git branch -f <название-ветки-1> <название-ветки-2>` - перенести ветку1 на тот момент где сейчас находится ветка2
1. `git checkout -b <название-ветки> <индекс-коммита>` - создать ветку на момент индексКоммита
1. `git checkout -B <название-ветки> <индекс-коммита>` перенесет ветку с таким названием если она есть на момент индексКоммита
1. `git checkout <индекс-коммита> <файл> <файл> <файл>` - восстановит указанные файлы, на момент коммита, вместо `<индекс-коммита>` может быть <название-ветки>, при этом переключение на ветки не происходит

      * важно знать, востановленные файлы checkout добавляет в индекс, если сейчас запустить коммит, то эта более старая версия станет текущей

1. `git reset <файл>` - восстановленный файл будет удален из индекса
1. `git checkout <файл>` - возвращает файл из индекса в рабочую директорию
1. `git checkout HEAD <файл>` - возвращает файл из этого коммита в рабочую директорию и индекс

      > в случая когда имя ветки может совпадать с именем какой-то директории в проекте, то чтобы гит различал где ветка а где директория, перед именем директории ставят `--`, флаги или аргументы(HEAD, индексы) должны идти до `--`

1. `git checkout <имя>` - здесь гит переключиться на ветку
1. `git checkout -- <имя>` - здесь на директорию, которая может совпадать с название ветки
1. `git merge <название-ветки>` - слияние с веткой, к примеру если мы хотим побочную ветку слить с основной, то сначало надо переключиться на основную, а только потом вызвать команду `git merge` причем ветку, в команде надо писать не основную а побочную
1. `git branch -f <имя ветки> ORIG_HEAD` - откат слияния ветки, обычно откатываю основную ветку, если решают что слияние было поспешным, и побочную можно ещё разарбатывать дальше
1. `git branch -d <название-ветки>` - удаление ветки, при это нужно быть не на самой ветке, и удаляемая ветка должна быть слита с основой
1. `git branch -D <название-ветки>` - удаление ветки если она оказалась тупиковой, и мы не хотим её слияния с основной
1. `git branch <название-ветки> <индекс коммита>` - востановление удаленной ветки по комиту, называние писать точно такое же