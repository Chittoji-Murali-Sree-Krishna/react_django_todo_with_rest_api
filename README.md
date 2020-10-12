# todoapp
>this is a django project
# todo
>this is the django app which interacts with the rest api and react app
# todofrontend
>this is the react app
# to connect with react and django
1. we have the white list the localhost of the react app in the settings.py of django
```python
CORS_ORIGIN_WHITELIST = [
    "http://localhost:3000",
]
```
1. to use the react with django we have run both the servers npm start in react app dir and python manage.py runserver in django dir so that both the localhosts interact with each other
1. for styling and stuff we have connect the static files of the react build 
```python
STATICFILES_DIRS = [
    os.path.join(BASE_DIR, 'todofrontend/build/static')
]
```
# todoapp
## installed apps in settings.py
```python
INSTALLED_APPS = [
    'todo.apps.TodoConfig',  #the app which we created
    'rest_framework',  #for the rest api
    'corsheaders', #for the bootstrap4 styling
]
```
## urls.py
1. here we add the route for the django app and reactapp
1. we have to import template view for accessing the class 
```python
from django.views.generic import TemplateView
```
1. for reactapp basically we dont have html page by start we do everything in src so we have to choose default build page for accessing the app instead of building each and everytime
```python
urlpatterns = [
    path('admin/', admin.site.urls),
    path('todo/', include('todo.urls')),
    path('', TemplateView.as_view(template_name= 'index.html')),
]
```
# todo
## models.py 
>in this we create the task
## l. serelizers.py
>we are using sereliazers.py bcz we are managing the tasks over json and post, get methods
## ll. urls.py
>we use this urls to route the views which we create
## lll. views.py
#### apiOverview
>to list all the routes for the todos required
#### taskList
>this will list all the tasks we have
#### taskDetail
>this will show the selected object in a detail
#### taskCreate
>after clicking create this will make create the task in the database
#### taskUpdate
>this will update the task which we have created
#### taskDelete
>this will delete task which we have selected and we are using the djnago built in function for this i.e, .delte()

# final
>after building the reactapp we also need to run the server for updating the tasks if not we cant able todo any thing it will be as static page
