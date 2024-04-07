# Site_Deploy_Flask
site_deploy_py_any_notes
Деплой Flask сайта на PythonAnywhere
Краткое описание процесса деплоя (действия, команды в консоли etc.)
0. Регаемся в облачном сервисе PythonAnywhere 
1. Создаем виртуальное окружение
mkvirtualenv --python=python3.8 <virtualenv_name>

workon <virtualenv_name> - активация виртуального окружения deactivate - деактивация

2. Проверка инсталляции встроенного установщика пакетов и админской части  
which pip

which django-admin.py

3. Устанавливаем необходимые для работы вашего сайта или приложения пакеты
a) pip install <имя пакета>

или

b) pip freeze > requirements.txt - для выгрузки всех пакетов из среды разработки

Далее на PythonAnywhere, запускаем

pip install -r requirements.txt

4. Проверяем наличие пакетов
pip list


5. Клонируем git-репо с вашим проектом или копируем все файлы вручную на сервис PythonAnywhere
#Cloning your Git Repository

а) git clone https://github.com/<git_user_name>/<repo_name>.git

б) для приватных репо

#To private

cd git_repo

git clone https://<git_user_name>:<git_pass> @github.com/<git_user_name>/<repo_name>.git

6. Настраиваем Web-сервис | PythonAnywhere
a) WSGI - user_name_pythonanywhere_com_wsgi.py (см. данный git-репо)
В этом файле меняем название flask_app на название нашего приложения например мтандартное app

Обновляемся и запускаем из PythonAnywhere

Congratulations!
