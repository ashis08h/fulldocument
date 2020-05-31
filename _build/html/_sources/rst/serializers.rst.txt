serializers module
==================

.. automodule:: serializers
   :members:
   :undoc-members:
   :show-inheritance:



############
Importing requied class and methods
############

.. code-block:: python
   :emphasize-lines: 3,5

   from rest_framework import serializers
   from user_app.models import UserDetails,ActivityPeriod




############
User Details Serializers
############

Using UserDetailsSerializers we are serializing and deserializing the UserDetails
model data

.. code-block:: python
   :emphasize-lines: 3,5

   class UserDetailsSerializers(serializers.ModelSerializer):
   		activity_periods = ActivityPeriodSerializers(many=True, read_only=True)
   		class Meta:
			model = UserDetails
			fields = ['id','real_name', 'tz','activity_periods']



############
Activity Period Serializers
############

Using ActivityPeriodSerializers we are serializing and deserializing the ActivityPeriod
model data

.. code-block:: python
   :emphasize-lines: 3,5

   class ActivityPeriodSerializers(serializers.ModelSerializer):
   		class Meta:
        	model = ActivityPeriod
        	fields = ['start_time','end_time']






