# GIT-TEST  
</br>

этот репозиторий был создан с целью ознанкомления со всеми тонкостями при работе с системой конроля версия GIT. Данный репозиторий могут использовать в дальнейшем новички в качестве мануала.  
</br> 

# УСТАНОКВКА  
</br>  

1. [ скачать можно на официальном сайте ](https://git-scm.com/downloads)
2. после установки выберите папку с которой хотите работать, нажмите правой кнопкой мыши, и выберите <b style='color: yellow'>Git Bash</b>
3. либо же можете открыть с помощью редактор кода, к примеру <b style='color: yellow'>VS CODE</b>, после чего выбрав вкладку терминал запустить консоль в редакторе.  
</br> 

# БАЗОВЫЕ КОМАНДЫ ПРИ РАБОТЕ С КОНСОЛЬЮ  
</br>  

1. <b style='color: yellow'>mkdir *название папки*</b> - создать папку  
2. <b style='color: yellow'>ls</b> - показать все файлы в этой папке
3. <b style='color: yellow'>ls -Hidden</b> - показать скрытые папки (для powershell), для GIT BASH  <b style='color: yellow'>ls -a</b>
4. <b style='color: yellow'>cd  *название папки*</b> - перейти в данную папку (можно указывать целый путь)
5. <b style='color: yellow'>cd  ..</b> - вернуться в предыдущую папку
6. <b style='color: yellow'>clear</b> - очистить консоль
</br> 

# БАЗОВЫЕ КОМАНДЫ GIT 
</br> 

1. <b style='color: yellow'>git init</b> - создание локального репозитория
2. <b style='color: yellow'>git config --local user.name "имя пользователя"</b> - заносим юзера который будет работать с данным проектом
3. <b style='color: yellow'>git config --global user.name "имя пользователя"</b> - заносим юзера глобально, т.е. при создании нового проекта GIT подхватывает глобальные данные в первую очередь, если требуется поменять пользователя для этого проекта мы можем написать с ключем --local
4. <b style='color: yellow'>git config --global user.email "email@mail.домен"</b> - заносим глобально почту нашего юзера
5. <b style='color: yellow'>git config --remove-section user"</b> -  удалить всю секцию с данным юзера  
</br> 

# ALIAS

здесь будут представлены сокращения для команд, гит, а так же для целой группы команд
</br> 
</br> 

## чтобы создать alias
</br> 

> git config --global alias.сокращение команда гит --- для одной команды
</br>

> git config --global alias.сокращение '!команда гит; !команда гит'  

</br>

# мой список alias
</br>

> <b style='color: yellow'>s</b> - git status