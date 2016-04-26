Event classes
^^^^^^^^^^^^^

The default settings play well with `django-admin-bootstraped
<https://github.com/django-admin-bootstrapped/django-admin-bootstrapped/>`_.

You can define your custom set of event classes and the corresponding
css classes to display in the admin. The default values are:

.. highlight:: python

::

   MQUEUE_EVENT_CLASSES = {                  
	   #~ 'Event class label' : 'css class to apply',                
	   'Default' : 'label label-default',                 
	   'Important' : 'label label-primary',                 
	   'Ok' : 'label label-success',                 
	   'Info' : 'label label-info',                 
	   'Debug' : 'label label-warning',                 
	   'Warning' : 'label label-danger',                 
	   'Error' : 'label label-danger',                 
	   'Object created' : 'label label-primary',                 
	   'Object edited' : 'label label-info',                 
	   'Object deleted' : 'label label-primary',                 
	   }

Note: if the ``event_class`` field value is not in
MQUEUE\_EVENT\_CLASSES, the display will fallback to 'Default'.

.. figure:: /img/events_list.png
   :alt: Event classes

To use your own event classes set a ``MQUEUE_EVENT_CLASSES`` setting.
Ex:

::

   MQUEUE_EVENT_CLASSES = {                
   #~ 'Event class label' : 'css class to apply',
   'Default' : 'mydefaultcssclass',
   'User registered' : 'mycssclass',
   'Post reviewed' : 'mycssclass mycssclass2',
   'Error in some process' : 'mycssclass mycssclass2',
   # ...                 
   }