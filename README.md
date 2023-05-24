# agenda

# Comandos no terminal

## Iniciando o Django
```
python -m venv venv
.\Scripts\activate
pip install django
cd c:\projeto\globallabs\
pip freeze
pip freeze --local > requirements.txt
python manage.py runserver
```
## Criando um App
```
django-admin startapp core
```

# Git Commands
## New Repository
```
echo "Hello_Django" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/sidneymarcelofranco/dio_django_framework.git
git push -u origin master
```
## or push an existing repository from the commnad line
```
git remote add origin https://github.com/sidneymarcelofranco/dio_django_framework.git
git push -u origin master
```
