================================================
fobi.contrib.plugins.form_elements.fields.slider
================================================
A ``Fobi`` Percentage form field plugin. Makes use of the
``django.forms.fields.ChoiceField`` and ``django.forms.widgets.Select``.

Installation
============
1. Add ``fobi.contrib.plugins.form_elements.fields.slider`` to the
   ``INSTALLED_APPS`` in your ``settings.py``.

.. code-block:: python

    INSTALLED_APPS = (
        # ...
        'fobi.contrib.plugins.form_elements.fields.slider',
        # ...
    )

2. In the terminal type:

.. code-block:: sh

    ./manage.py fobi_sync_plugins

3. Assign appropriate permissions to the target users/groups to be using
   the plugin if ``FOBI_RESTRICT_PLUGIN_ACCESS`` is set to True.

4. Ranges are specified within the given min/max values. The default values
   are:

   .. code-block:: text

       - INITIAL: 50
       - INITIAL_MAX_VALUE: 100
       - INITIAL_MIN_VALUE: 0
       - MIN_VALUE: 0
       - MAX_VALUE: 100
       - STEP: 1

   However, you can override each of them in the settings of your project by
   prefixing correspondent names with `FOBI_FORM_ELEMENT_SLIDER_`:

   .. code-block:: text

       - FOBI_FORM_ELEMENT_SLIDER_INITIAL
       - FOBI_FORM_ELEMENT_SLIDER_INITIAL_MAX_VALUE
       - FOBI_FORM_ELEMENT_SLIDER_INITIAL_MIN_VALUE
       - FOBI_FORM_ELEMENT_SLIDER_MIN_VALUE
       - FOBI_FORM_ELEMENT_SLIDER_MAX_VALUE
       - FOBI_FORM_ELEMENT_SLIDER_STEP
