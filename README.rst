=====================
django_localflavor_us
=====================

Country-specific Django helpers for U.S.A.

What's in the U.S.A. localflavor?
=================================

* forms.USPhoneNumberField: A form field that validates input as a U.S. phone
  number.

* forms.USSocialSecurityNumberField: A form field that validates input as a
  U.S. Social Security Number (SSN). A valid SSN must obey the following rules:

    * Format of XXX-XX-XXXX
    * No group of digits consisting entirely of zeroes
    * Leading group of digits cannot be 666
    * Number not in promotional block 987-65-4320 through 987-65-4329
    * Number not one known to be invalid due to widespread promotional
      use or distribution (e.g., the Woolworth's number or the 1962
      promotional number)

* forms.USStateField: A form field that validates input as a U.S. state name or
  abbreviation. It normalizes the input to the standard two-letter postal
  service abbreviation for the given state.

* forms.USZipCodeField: A form field that validates input as a U.S. ZIP code.
  Valid formats are XXXXX or XXXXX-XXXX.

* forms.USStateSelect: A form ``Select`` widget that uses a list of U.S.
  states/territories as its choices.

* forms.USPSSelect: A form ``Select`` widget that uses a list of U.S Postal
  Service state, territory and country abbreviations as its choices.

* models.PhoneNumberField: A ``CharField`` that checks that the value is a
  valid U.S.A.-style phone number (in the format ``XXX-XXX-XXXX``).

* models.USStateField: A model field that forms represent as a
  ``forms.USStateField`` field and stores the two-letter U.S. state
  abbreviation in the database.

* models.USPostalCodeField: A model field that forms represent as a
  ``forms.USPSSelect`` field and stores the two-letter U.S Postal Service
  abbreviation in the database.

Additionally, a variety of choice tuples are provided in
``us.us_states``, allowing customized model and form fields, and form
presentations, for subsets of U.S states, territories and U.S Postal Service
abbreviations:

* us_states.CONTIGUOUS_STATES: A tuple of choices of the postal abbreviations
  for the contiguous or "lower 48" states (i.e., all except Alaska and Hawaii),
  plus the District of Columbia.

* us_states.US_STATES: A tuple of choices of the postal abbreviations for all
  50 U.S. states, plus the District of Columbia.

* us_states.US_TERRITORIES: A tuple of choices of the postal abbreviations for
  U.S territories: American Samoa, Guam, the Northern Mariana Islands, Puerto
  Rico and the U.S. Virgin Islands.

* us_states.ARMED_FORCES_STATES: A tuple of choices of the postal abbreviations
  of the three U.S military postal "states": Armed Forces Americas, Armed
  Forces Europe and Armed Forces Pacific.

* us_states.COFA_STATES: A tuple of choices of the postal abbreviations of the
  three independent nations which, under the Compact of Free Association,
  are served by the U.S. Postal Service: the Federated States of
  Micronesia, the Marshall Islands and Palau.

* us_states.OBSOLETE_STATES: A tuple of choices of obsolete U.S Postal Service
  state abbreviations: the former abbreviation for the Northern Mariana
  Islands, plus the Panama Canal Zone, the Philippines and the
  former Pacific trust territories.

* us_states.STATE_CHOICES: A tuple of choices of all postal abbreviations
  corresponding to U.S states or territories, and the District of Columbia.

* us_states.USPS_CHOICES: A tuple of choices of all postal abbreviations
  recognized by the U.S Postal Service (including all states and territories,
  the District of Columbia, armed forces "states" and independent nations
  serviced by USPS).

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
