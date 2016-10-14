Project policy
==============

Project layout
--------------

The canonical project layout is maintained in ``mir.protology``.  New
projects SHOULD copy ``mir.protology``, and existing projects SHOULD
follow the same layout.

Documentation
-------------

Projects MUST provide documentation.

Text style
----------

Sentence-terminating periods SHOULD be followed by two spaces.

In headings, the first word SHOULD be capitalized unless it is case
sensitive, and following words SHOULD NOT be capitalized unless they
would normally be capitalized in paragraph text.

Releases and versioning
-----------------------

Projects MUST use `semantic versioning`_, except for evergreen projects.

.. _semantic versioning: http://semver.org/

Evergreen projects cannot reasonably have a public API and are instead
continuously improved.  This project, mir.eschatology, is an evergreen project.

Evergreen projects MAY have releases.  Release versions MUST increase
monotonically in alphanumeric sort order.

Release procedure
^^^^^^^^^^^^^^^^^

Version control
---------------

Projects MUST use Git version control.

Licensing
---------

Projects MUST be licensed under a free software license.

Contributions
-------------

Contributors MUST assign copyright for contributions to the project
owner.  This simplifies any legal actions, such as changing to a
different free software license.
