admin module
============

.. automodule:: admin
   :members:
   :undoc-members:
   :show-inheritance:


############
Importing requied class and methods
############

.. code-block:: python
   :emphasize-lines: 3,5

   from django.contrib import admin
   from user_app.models import  UserDetails,ActivityPeriod





############
User details Model
############

Here we are Registring the model to the django admin 


.. code-block:: python
   :emphasize-lines: 3,5

   admin.site.register(UserDetails)
   admin.site.register(ActivityPeriod)
