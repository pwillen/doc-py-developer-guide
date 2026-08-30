# Django
## Create Project
`django-admin startproject <project_name>`
## Start Server
`python manage.py runserver`
## Create App
`python manage.py startapp <app_name>`
## Migrations
### Migration Changes
`python manage.py makemigrations <app_name/module_name>` - Add/Create Migrations
`python manage.py migrate` - Apply Migrations
### Smoke Test
`python manage.py sqlmigrate <app_name/module_name> <migration_name>` - View Migration (SQL)
## Database Shell Functions
`python manage.py dbshell` - Start Database Shell
## Shell/API Functions
```
python manage.py shell  # Start Shell
<class_name>.objects.all()  # List Model Objects
<class_name>.objects.filter(id=<id>)  # Filter Model Objects
<class_name>.objects.filter(<parameter>__startswith='')  # Another Filter Model Objects
<class_name>.objects.get(pk=<id>)  # Get Model Object
<class_name>.<set_name>_set.all()  # List Related Set Model Objects
<class_name>.<set_name>_set.create()  # Shortcut to Create Objects
<class_name>.<set_name>_set.count()  # Count Model Objects
<object>.delete()  # Delete Model Object
```
## Smoke Test
`python manage.py check` - Check for Errors
## Admin
`python manage.py createsuperuser`
## Test
`python manage.py test <app_name>` - Run Tests