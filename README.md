# django3-starter
a project starter for django, using nginx as proxy,
uwsgi as wsgi server and mysql as database,
all the components work as container on docker
this project is inspired by https://github.com/twtrubiks/docker-django-nginx-uwsgi-postgres-tutorial

after clone this project:

1. cd to the folder
2. add a .env file which contains the following informations to the project root folder
    - MYSQL_ROOT_PASSWORD= YOUR_ROOT_PASSWORD
    - MYSQL_DATABASE= YOUR_DB_NAME
    - MYSQL_USER= YOUR_MYSQL_USERNAME
    - MYSQL_PASSWORD= PASSWORD_OF_USER_ABOVE
3. edit DB related information in ./my_project/my_project/settings.py
4. type command: "docker-compose up --build"  in your terminal

then the project will be deployed
after building finish, go to http://localhost in your browser
and you will see the starting page of django

---

if you wanna change the project's name, don't forget to change the path of folder
in ./nginxconf/my_nginx.conf and uwsgi_conf.ini

---


if you want to use django-admin
just type "docker exec -it web python3 manage.py createsuperuser"
and create your super user account to the project,
then you can login with that account