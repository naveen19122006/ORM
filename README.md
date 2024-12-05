# Ex02 Django ORM Web Application
# Date:27-09-2024
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# ENTITY RELATIONSHIP DIAGRAM
![Screenshot 2024-12-04 144713](https://github.com/user-attachments/assets/72ecffd9-9d9b-4f19-8756-af8c6a320e35)

## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 books

# PROGRAM

admin.py
~~~
from django.contrib import admin
from .models import book,bookadmin
admin.site.register(book,bookadmin)
~~~

models.py
~~~
from django.db import models
from django.contrib import admin
class book(models.Model):
    Book_name=models.CharField(max_length=100)
    Author=models.CharField(max_length=100)
    Co_author=models.CharField(max_length=100)
    Book_code=models.IntegerField()
    Publisher=models.CharField(max_length=100)
    MRP=models.IntegerField()
class bookadmin(admin.ModelAdmin):
    list_display=("Book_name","Author","Co_author","Book_code","Publisher","MRP")
~~~

urls.pr
~~~
from django.contrib import admin
from django.urls import path

urlpatterns = [
    path('admin/', admin.site.urls),
]
~~~

# OUTPUT
![Screenshot 2024-12-05 213846](https://github.com/user-attachments/assets/d6ba3309-ef69-44f3-b13f-d806a19d349a)

![Screenshot 2024-12-05 213819](https://github.com/user-attachments/assets/37d24a9d-b4e7-4ef3-a308-4cd7f7f1ee44)


# RESULT
Thus the program for creating a database using ORM hass been executed successfully
