<font style="color:red"> todoapp </font>
this is a django project
# todo
this is the django app which interacts with the rest api and react app
# todofrontend
this is the react app
# to connect with react and django
- we have the white list the localhost of the react app in the settings.py of django
- to use the react with django we have run both the servers npm start in react app dir and python manage.py runserver in django dir so that both the localhosts interact with each other
# todoapp
## installed apps in settings.py
- todo/apps.TodoConfig //this is for app which we created in django
- rest_framework // this is for the restapi
- corsheaders //we are using corsheaders for merging the urls with each other
## urls.py
- here we add the route for the django app and reactapp 
- for reactapp we have to link the index.html inside the build folder bcz the reactjs when we are testing, we are only using the .js files so we have to use thw template in build folder
# todo
## models.py 
in this we create the task
## l. serelizers.py
we are using sereliazers.py bcz we are managing the tasks over json and post, get methods
## ll. urls.py
we use this urls to route the views which we create
## lll. views.py
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

# final
after building the reactapp we also need to run the server for updating the tasks if not we cant able todo any thing it will be as static page
