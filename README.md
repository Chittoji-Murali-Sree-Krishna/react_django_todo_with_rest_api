## todoapp
this is a django project
## todo
this is the django app which interacts with the rest api and react app
## todofrontend
this is the react app
## to connect with react and django
we have the white list the localhost of the react app in the settings.py of django
to use the react with django we have run both the servers npm start in react app dir and python manage.py runserver in django dir so that both the localhosts interact with each other
## installed apps
rest api with corsheaders
## models.py 
in this we create the task
## serelizers.py
we are using sereliazers.py bcz we are managing the tasks over json and post, get methods 
## views.py
### apiOverview
to list all the routes for the todos required
### taskList
this will list all the tasks we have
### taskDetail
this will show the selected object in a detail
### taskCreate
after clicking create this will make create the task in the database
### taskUpdate
this will update the task which we have created
### taskDelete
this will delete task which we have selected and we are using the djnago built in function for this i.e, .delte()
