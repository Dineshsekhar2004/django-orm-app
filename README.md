# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![Screenshot_20230128_092308](https://user-images.githubusercontent.com/119405916/215276181-8c8efad0-079d-499a-bd1a-b9fbed28768b.png)


## DESIGN STEPS

### STEP 1:
Start a project and create a superuser

### STEP 2:
Set a password and email

### STEP 3:
Make the neccessary changes in the models and admin.Then make migrations and run the server

## PROGRAM
models.py
```
from django.db import models
from django.contrib import admin

class employee (models.Model):
  emp_id=models.CharField(primary_key=True,max_length=20,help_text="EMPLOYEE ID")
  ename=models.CharField(max_length=100)
  post=models.CharField(max_length=20)
  salary=models.IntegerField()  
  email=models.EmailField()

class employeeAdmin(admin.ModelAdmin):
    list_display=('emp_id','ename','post','email')
```
admin.py
```
from django.contrib import admin
from.models import employee,employeeAdmin
admin.site.register(employee,employeeAdmin)
```

## OUTPUT:
Django
![Screenshot (13)](https://user-images.githubusercontent.com/119405916/215275910-ab01fa20-553c-4dee-9d17-b0a048e59743.png)
Primary Key
![Screenshot (14)](https://user-images.githubusercontent.com/119405916/215275928-1c2fe756-315b-452a-b337-0a2b7ee00c44.png)

## RESULT:
Thus we developed a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).
