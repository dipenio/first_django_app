# First Django app

using offical tutorial on the Django website


## part 1 
https://docs.djangoproject.com/en/3.1/intro/tutorial01/


1) creating a project
...\> django-admin startproject mysite

2) dev server
...\> py manage.py runserver

3) creating the polls app
...\> py manage.py startapp polls

4) first view
from django.http import HttpResponse
def index(request):
    return HttpResponse("Hello, world. You're at the polls index.")

5)url config
polls/urls.py¶
from django.urls import path
from . import views
urlpatterns = [
    path('', views.index, name='index'),
]

from django.contrib import admin
from django.urls import include, path
urlpatterns = [
    path('polls/', include('polls.urls')),
    path('admin/', admin.site.urls),
]


## part 2

