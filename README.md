# doc-py-developer-guide
## SSH
1. ssh-keygen is run via: `ssh-keygen -t rsa -b 4096 -a 100`
2. A private key `id_rsa` and public key `id_ras.pub` are created
3. The public key (`id_rsa.pub`) is provide to the github account for association
4. The private key (`id_rsa`) is placed within the users `.ssh` folder (typically the folder is located at `%userprofile%\.ssh` on Windows)
5. The `config` or `ssh_config` file is created/modified to point to the private key
### Config
```
Host * github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/<id_rsa>
  IdentitiesOnly yes
```
Note: The config may point to more than one private key
```
Host * github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/<id_rsa>
  IdentitiesOnly yes

Host * github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/<id_rsa_2>
  IdentitiesOnly yes
```
## Django
### Create Project
`django-admin startproject <project_name>`
### Start Server
`python manage.py runserver`
### Create App
`python manage.py startapp <app_name>`
### Migrations
`python manage.py sqlmigrate <module_name> <migration_name>` - View Migration
#### Migration Changes
`python manage.py makemigrations <module_name>` - Add/Create Migrations
`python manage.py migrate` - Apply Migrations
### Database Shell Functions
```
python manage.py shell  # Start Shell
<class_name>.objects.all()  # List Model Objects
<class_name>.objects.filter(id=<id>)  # Filter Model Objects
<class_name>.objects.filter(<parameter>__startswith='')  # Another Filter Model Objects
<class_name>.<set_name>_set.create()  # Shortcut to Create Objects
<class_name>.<set_name>_set.count() # Count Model Objects
```
###
`python manage.py createsuperuser`





