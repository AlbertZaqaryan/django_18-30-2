# django_18-30-2

1) py -m venv venv
2) .\venv\Scripts\activate
3) py -m pip install --upgrade pip
4) pip install django
5) django-admin startproject core
6) cd core
7) python manage.py startapp main
8) open core.settings and add main in to INSTALLED_APPS
9) create new file (urls.py) in main
10) open core.urls and add include, and new path('', include('main.urls'))
11) open main.urls and add 
    -from django.urls import path
    -urlpatterns = [

    ]
12) create new python function in to views.py
    - from django.http import HttpResponse
    - def home(request):
        return HttpResponse('Hello Python Team')
13) open main.urls 
    - from . import views

    path('', views.home, name='home')

14) open terminal and write python manage.py runserver
