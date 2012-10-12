=====================
django_localflavor_us
=====================

Country-specific Django helpers for U.S.A.

What's in the U.S.A. localflavor?
=================================

``Field`` clases you can use in forms:

* ``django_localflavor_us.forms.USZipCodeField``: Validates U.S. ZIP codes.

* ``django_localflavor_us.forms.USPhoneNumberField``: Validates U.S. phone
  numbers.

* ``django_localflavor_us.forms.USSocialSecurityNumberField``: Validates U.S.
  social security numbers.

* ``django_localflavor_us.forms.USStateField``: Validates U.S. states. Input
  can be an abbreviation or a full name.

``Widget`` classes you can use in forms:

* ``django_localflavor_us.forms.USStateSelect``: A select widget that uses a
  list of U.S. states/territories as its choices.

* ``django_localflavor_us.forms.USPSSelect``: A select widget that uses a list
  of US Postal Service codes as its choices.

See the source code for full details.

About localflavors
==================

Django's "localflavor" packages offer additional functionality for particular
countries or cultures.

For example, these might include form fields for your country's postal codes,
phone number formats or government ID numbers.

This code used to live in Django proper -- in django.contrib.localflavor -- but
was separated into standalone packages in Django 1.5 to keep the framework's
core clean.

For a full list of available localflavors, see https://github.com/django/
