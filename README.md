# My CIS-92 Project 

This repository has the starter code for CIS-92. 

## Variables from the config.yaml file
----
| Variable Name | Notes|
|----|----|
|Port| Holds the port number for the site. This is typically set to **8000** |
|STUDENT_NAME| This is used to set the full name of the student. Set to "Andrew Pfeiffer" |
|SITE_NAME| This is used to set the name of the site itself, the default is set to "Andrew's Test Site" |
|SECRET_KEY|A secret key that is defaulted to a horribly insecure password that should always be changed for production use. |
|Data_DIR|Stores the data directory for site. This is normally held in the relative path of **/data** in the root of the application directory|
|WORKDIR|The base directory for the web application |
----

## Setting up Application
----

````
kubectl exec --stdin --tty pos/mysite-pod--/bin/bash
````
````
python manage.py migrate
````
````
python manage.py createsuperuser
````
----
## Deleting the Application
----
````
kubectl delete -f deployment/
````
