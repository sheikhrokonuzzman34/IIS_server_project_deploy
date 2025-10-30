## first windows iis enable 
```text
1. control panel -- turn windows features on or off
2. open iis server -- site -- create new website
3. click your website click -- handler Mappings -- click Add Model Maping
4. request path (*)
5. firstcgi
6.pip install wfastcgi
7.wfastcgi-enable	
8. click DESKTOP-M5Q2LLM --- click fastcgi
9. name -- PYTHONPATH
   value-- D:\iis_server\Django-atheeb-information-management-system\Backend
   name -- WSGI_HANDLER
   VALUE--django.core.wsgi.get_wsgi_application()
   NAME-- DJANGO_SETTINGS_MODULE
   VALUE-- core.settings

10.IUSR adn IIS_IUSRS

F:\\rokon\\project\\Django-atheeb-information-management-system\\Backend\\env\\Scripts\\python.exe|F:\\rokon\\project\\Django-atheeb-information-management-system\\Backend\\env\\Lib\\site-packages\\wfastcgi.py

F:\rokon\project\Django-atheeb-information-management-system\Backend\env\Scripts\python.exe|F:\rokon\project\Django-atheeb-information-management-system\Backend\env\Lib\site-packages\wfastcgi.py


```

