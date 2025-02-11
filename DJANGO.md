# Django
## Create Project
`django-admin startproject <project_name>`
## Start Server
`python manage.py runserver`
## Create App
`python manage.py startapp <app_name>`
## Migrations
`python manage.py sqlmigrate <module_name> <migration_name>` - View Migration
### Migration Changes
`python manage.py makemigrations <module_name>` - Add/Create Migrations
`python manage.py migrate` - Apply Migrations
## Database Shell Functions
```
python manage.py shell  # Start Shell
<class_name>.objects.all()  # List Model Objects
<class_name>.objects.filter(id=<id>)  # Filter Model Objects
<class_name>.objects.filter(<parameter>__startswith='')  # Another Filter Model Objects
<class_name>.<set_name>_set.all()  # List Related Set Model Objects
<class_name>.<set_name>_set.create()  # Shortcut to Create Objects
<class_name>.<set_name>_set.count()  # Count Model Objects
```
## Admin
`python manage.py createsuperuser`