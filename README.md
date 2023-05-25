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

## Comandos django admin

```
django-admin --help
```

## O que é o manage.py? 

* É um wrapper em volta do django-admin.py
* Ele delega tarefas para o django admin.py
* Reponsavel por colocar o pacote do projeto no sys.path
* Ele define a variável de ambiente DJANGO_SETTINGS_MODULE que então aponta para o arquivo settings.py
* Por isso, o manage.py é gerado automaticamente junto ao projeto, para facilitar o uso de comandos do django-admin.py(comando administrativos)

## WSGI
* Web Server Gateway Interface - Interface de porta de entrada do servidor web
* Plataforma padrão para palicações web em Python
* Serve de interface do Servidor Web e a Aplicação Web
* O Django com o comando startproject inicia uma configuração WSGI padrão para que se possa executar sua aplicação web
* Quando se inicia a aplicação Django com o comando runserver é iniciado um servidor de aplicação web leve. Esse servidor é especificado pela configuração WSGI_APPLICATION

https://docs.djangoproject.com/en/4.2/howto/deployment/

## Settings
* É o responsável pelas configurações do DJANGO
* Nele é possível configurar por exemplo apps, conexão com banco de dados, templates, time zone, cache, segurança, arquivos estáticos, ...

## Models
* Define o modelo de dados inteiramente em Python
* * Faz a abstração dos objetos de banco para o Python, transformando todas as tabelas em classes e os acessos são feitos utilizando a linguagem Python, onde o DJango realiza a transformação para SQL.

Exemplo de consulta 
  pessoa = Pessoa.objects.get(nome='Rafael')

## ADMIN - Django Administration
* Interface administrativa gerada inteiramente em Python
* Ele lê os mnetadados que estão nos models e fornece uma interface poderosa e pronta para manipulação de dados

## STATIC
* Responsável por armazenar os arquivos estáticos
* CSS, JavaScript, imagens

## TEMPLATES
* Responsável por armazenar os arquivos HTML
* o diretório templates é o diretório padrão para armazenarmos todo o conteúdo HTML da nossa aplicação.




cd .virtualenv
.\Scripts\activate
cd c:\Projetos\globalabs
django-admin startproject agenda
cd .\agenda\
ls
django-admin startapp core
ls
## migração de all app e all number of migrations
python manage.py migrate
## migração por nome do app e por numero da migração
       Comando           app  numero da migração (pasta migrations referente a o arquivo 0001_intial.py )
python manage.py migrate core 0001
python manage.py createsuperuser --username admin
Note: 
  1. migrate, which is responsible for applying migrations, as well as unapplying and listing their status.
  2. makemigrations, which is responsible for creating new migrations based on the changes you have made to your models.


# Migração de dados no Django
* Para migração de dados no Django, é necessário que tenha classes criadas.
* Com as classes criadas, para migração é utilizado o comando migrate.
* Também pode-se utilizar o comando migrations para criação de um arquivo de migração, sem a necessidade de migrar "as cegas".
* Também pode-se utilizar o comando **sqlmigrate**, que ao invés de aplicar a migração, é gerado **todo o comando** para que esse migração possa ser efetuada **manualmente** no banco de dados.


# Pacote de autenticação do Django (django.contrib.auth)
* O Django possui um pacote de autenticação que é empacotado em django.contrib.auth
* Este pacote cria as tabelas de usuários e permissões, onde fica mais fácil controlar as autenticações e permissões.
* Para se utilizar da autenticação padrão do Django é necessãrio que o pacote esteja entre os Apps instalados no settings do projeto (essa configuração já vem pronta pro default)









