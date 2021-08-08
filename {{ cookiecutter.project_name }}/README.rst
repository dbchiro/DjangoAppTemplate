=============================
{{cookiecutter.project_name}}
=============================

{{cookiecutter.description}}


Detailed documentation is in the "docs" directory.

Quick start
-----------

1. Install app

.. code-block:: bash

    $ pip install -U app-name



2. Configure ``INSTALLED_APPS``:

.. code-block:: python

    INSTALLED_APPS = (
        'django.contrib.admin',
        'django.contrib.auth',
        (...),
        'rest_framework',
        '{{cookiecutter.project_slug}}',
        (...),
    )


1. Configure ``urls.py``:

.. code-block:: python

    urlpatterns = [
        path('admin/', admin.site.urls),
        path('api-auth/', include('rest_framework.urls')),
        (...),
        path('api/v1/', include('{{cookiecutter.project_slug}}.urls')),
        (...),
    ]

1. Run ``python manage.py migrate`` to create the polls models.

2. Start the development server and visit http://127.0.0.1:8000/admin/
   to create an organism (you'll need the Admin app enabled).

3. Visit http://127.0.0.1:8000/api/v1/... to view organisms API.
