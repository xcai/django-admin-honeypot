django-admin-honeypot-2024
==========================
![PyPI - Version](https://img.shields.io/pypi/v/django-admin-honeypot-2024)
![PyPI - Downloads](https://img.shields.io/pypi/dw/django-admin-honeypot-2024)
![GitHub Repo stars](https://img.shields.io/github/stars/xcai/django-admin-honeypot)


**django-admin-honeypot-2024** is a fake Django admin login screen to log and notify
admins of attempted unauthorized access. This app was inspired by discussion
in and around Paul McMillan's security talk at DjangoCon 2011.   
支持Django 4.2版本。（原项目会报错）

* **Author**: [xcai](https://github.com/xcai/django-admin-honeypot)
* **Version**: 1.1.0
* **License**: MIT

Documentation
=============

* Install django-admin-honeypot from PyPI:
```
        pip install django-admin-honeypot-2024
```
* Add ``admin_honeypot`` to ``INSTALLED_APPS``
* Update your urls.py:
```
        urlpatterns = [
            ...
            path('admin/', include('admin_honeypot.urls', namespace='admin_honeypot')),
            path('secret/', admin.site.urls),
        ]
```

* Run ``python manage.py migrate``

NOTE: replace ``secret`` in the url above with your own secret url prefix
