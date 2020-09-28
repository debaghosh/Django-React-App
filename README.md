# Django-React-App
This is a procedure of how we can connect the React templates, static files to Django backend.
My first attempt.



1. Create the django app using "django-admin startproject [projectname]"
2. Create the reactapp using "npx create-reactapp [appname]"
3. Make sure the reactapp is within the django root directory of [projectname]
4. Run the "npm run build" command in the reactapp, creating a "build" folder containing the "index.html" and "static".
5. i>settings.py--> add DIR =[ os.path.join(BASE_DIR,'reactapp/build')]        ii>urls.py    --> connect to the index.html template of build.
6. settings.py--> add STATICFILES_DIRS = [os.path.join(BASE_DIR, 'reactapp/build/static')]
7. Now update the App.js, App.css files accordingly.
8. Run "npm run build" again to update.
9. Finally run the django app "python manage.py runserver".
