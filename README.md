# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![Entity Relationship Diagram](./out6.png)

## DESIGN STEPS

### STEP 1:

Fork and clone the repositary in to your IDE.

### STEP 2:

Create a django project and an app and a superuser account and run the server.

### STEP 3:

Modify changes in settings and write ur code on models and admin and run the server.

### STEP 4:

Login in to admin using your superuser account and populate the records.

## PROGRAM
```
Model.py

from django.db import models
from django.contrib import admin
# Create your models here.
class Student(models.Model):
    studentname = models.CharField(max_length=100,primary_key= True)
    refno = models.CharField(max_length=100)
    lastname= models.CharField(max_length=80)
    emailid = models.EmailField()
    age=models.CharField(max_length=10)
    mobile=models.CharField(max_length=10)

    
class StudentAdmin(admin.ModelAdmin):
    list_display = ('studentname','refno','lastname','emailid','age','mobile')

Admin.py

from django.contrib import admin
from .models import Student,StudentAdmin
admin.site.register(Student,StudentAdmin)
```

## OUTPUT

![out 3](https://github.com/MohamedMunthasir/django-orm-app/assets/121957086/869e4a41-1539-4b05-a0c9-4013001fc9a9)


## Verifying Primary-Key

![Verifying Primary-Key](./out7.png)

## RESULT

Program executed successfully.
