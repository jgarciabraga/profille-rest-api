# Profiles REST API

Profile REST API code.



### A Vagrant Tips

To create the virtual server, I am usning vagrant.
```
vagrant init ubuntu/bionic64
```

To get up the vagrant virtual environment. First, enter in the folder with vagrantfile.
```
vagrant up
```

To remove/delete and free up the respurces
```
vagrant destroy -f
```

To enter in vagrant server
```
vagrant ssh
```

### Python and Django Tips

All the content within the main folder will be mirrored for the /vagrant folder in the virtual server, and vice versa. To avoid that env folder (python environment folder) to be mirrored to mains project folder, I like to create the env folder within the home in te vagrant server.

#### To create a python virtual environment

1 - enter in the vagrant virtual server
```
vagrant ssh
```

2 - in the home folder
```
python -m venv env
```
or
```
python -m venv ~/env
```

To start a django project
```
django-admin.py startproject "project name" .
```

To start a django app
```
python manage.py stratapp profiles_api
```


To create the migrations after the changes in the models
```
python manage.py makemigrations profiles_api
```

To apply the migrations
```
python manage.py migrate
```

