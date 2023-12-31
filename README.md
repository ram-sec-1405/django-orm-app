# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![orm](https://github.com/ram-sec-1405/django-orm-app/assets/155155799/429d1d05-ebfe-4335-b775-d803c19f4ebe)


## DESIGN STEPS

### STEP 1:
close the empty repository for github
### STEP 2:
under the directory dataproject insstall a Django project named'myapp' check database engine 'sqlite'.
### STEP 3:
write your code in models.py, settings.py and admin.py
W
## PROGRAM
## Modela.py
```python
from django.db import models
from django.contrib import admin

# Create your models here.
class Student (models.Model):
    referencenumber=models.CharField(max_length=20,help_text="reference number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    mobile=models.IntegerField()


class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email','mobile')
```
## Admin.py
```python
from django.contrib import admin
from .models import Student,StudentAdmin

# Register your models here.
admin.site.register(Student,StudentAdmin)
```
## OUTPUT
![orm output](https://github.com/ram-sec-1405/django-orm-app/assets/155155799/285a2946-7271-4c66-a693-ec3a8edd94bb)

## RESULT
The program is executed Successfully.
