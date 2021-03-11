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

1. `mkdir *название папки*` - создать папку  
2. `ls` - показать все файлы в этой папке
3. `ls -Hidden` - показать скрытые папки (для powershell), для GIT BASH  `ls -a`
4. `cd  *название папки*` - перейти в данную папку (можно указывать целый путь)
5. `cd  ..` - вернуться в предыдущую папку
6. `clear` - очистить консоль

</br> 
</br>

# БАЗОВЫЕ КОМАНДЫ GIT 
</br> 

1. `git config --local user.name "имя пользователя"` - заносим юзера который будет работать с данным проектом
2. `git config --global user.name "имя пользователя"` - заносим юзера глобально, т.е. при создании нового проекта GIT подхватывает глобальные данные в первую очередь, если требуется поменять пользователя для этого проекта мы можем написать с ключем `--local`
3. `git config --global user.email "email@mail.домен"` - заносим глобально почту нашего юзера
4. `git config --remove-section user"` -  удалить всю секцию с данным юзера  

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

> `comD` - git config --global alias.comD '!git add .; git commit' - добавление включая неотслеживаемые файлы

> `comA` - git config --global alias.comA '!git add -A; git commit' - добавление всего 


</br>
</br>

# GIT КОМАНДЫ ДЛЯ РАЗРАБОТКИ
</br>

1. `git init` - создание локального репозитория
2. `git status`- проверка на изменения в проекте, покажет какие файлы были созданы или изменены, но еще не проиндексированы
3. `git add имя файла` - индексирование файла, либо папки, либо отдельной файла в папке( папка/файл )
4. `git commit` - добавления файла в репозиторий, необходимо будет ввести заголовок коммита в первой строе, и далее после пустой строк написать какие-то доплнительные сведения
5. `git commit -m"заголовок коммита"`  - флаг `-m` позволяет писать заголовок коммита прямо в терминале

      * комиты лучше делать после каждого изменения

      * заголовок коммита обычно пишут в следущем стиле `характер выполненый работы(над каким компоненотом проводилась работа): краткое описание того что было сделано`

6. `git commit -a` - флаг `-a` позволяет сразу же коммитить из рабочей директории без `git add`, но только уже проиндексированные файлы, файлы которые ещё только созданы и не отслеживают не закомитятся

7. `git commit папк/папка/...` - закомитит без `git add` только файлы из этой дирректории