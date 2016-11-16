mir.eschatology
===============

mir.eschatology documents the meta-project comprising all Python
packages under `Project Mir`_.

.. _Project Mir: http://project-mir.felesatra.moe/

About Project Mir
-----------------

I have not once regretted taking the time to write good software, and
I have not once not regretted taking a shortcut and writing mediocre
software.  Project Mir is a personal project to write good software.

mir.eschatology, along with mir.protology, describes the requirements
for Python projects under Project Mir.

Project template
----------------

`mir.protology`_ is a project template for Python projects under
Project Mir.  New projects should use this template, and existing
projects should incorporate new changes where convenient.  Various
parts of the project template are described explicitly below.

.. _mir.protology: https://github.com/project-mir/mir.protology

Code style
----------

Python code should follow `PEP 8`_ and docstrings should follow `PEP
257`_.  When extra formatting is needed in docstrings, reStructuredText
should be used, per `PEP 287`_.

.. _PEP 8: https://www.python.org/dev/peps/pep-0008/
.. _PEP 257: https://www.python.org/dev/peps/pep-0257/
.. _PEP 287: https://www.python.org/dev/peps/pep-0287/

Packaging
---------

Python packages and modules should be packaged and distributed
according to the `Python Packaging User Guide`_.

.. _Python Packaging User Guide: https://packaging.python.org/

Projects should use `semantic versioning`_.  Precedence of the public
API specification is as follows:

.. _semantic versioning: https://semver.org/

- Tests for a given behavior.
- Documentation included in the distribution, but separate from the
  source code.
- Docstrings and metadata variables (``__all__``) in the source code.
- The source code itself, for functions and classes declared public by
  one of the previous levels of specification.

When in doubt, the specification should be considered ambiguous and
should be clarified via tests or documentation before being relied
upon.

Projects should upload a source distribution and a wheel to PyPI for
each release.  The source distribution should include:

- ``setup.py``
- source code
- documentation
- tests
- license file
- ``README.rst``
- ``NEWS.rst`` (release notes)

Python packages and modules under Project Mir should use the namespace
package ``mir``.  The maximum level of packages is 2
(``mir.package.module``), or 3 for namespace packages under ``mir``
(``mir.codecs.package.module``).

Version control
---------------

Projects should use Git.  The ``master`` branch should represent the
current head of development.  Releases should be tagged with an
annotated tag, e.g. ``v1.0.0``.  Separate branches should be made for
major and minor versions that are not at the head of ``master`` and
require changes, e.g. ``v1.0`` for bug fixes, ``v1`` for new features
(major versions not on ``master`` should probably not receive new
features due to the increased maintenance burden).

Separate feature branches may be used.  Feature branches should be
merged via rebase and fast forward when convenient.

Convoluted branching models (e.g., with separate development and
stable branches) should not be used.  ``master`` should represent both
the development and stable branch.

Documentation
-------------

Projects should include documentation.  Libraries should document
their entire public API.  Applications should document all features
and options, although a thorough technical specification may not be
necessary.

If the project is small, the documentation may be kept in the README
file.  Otherwise, more formal documentation should be created using
Sphinx.

Testing
-------

Projects should maintain 100% line coverage and branch coverage and
the tests must be passing at every commit.

The test coverage requirement is a bare minimum, not an end goal.
Full test coverage ensures that every line of code is able to run and
work as expected in at least one case.  Any line of code that cannot
even be run or work correctly in one case is worse than mediocre and
thus unacceptable.

Fixed bugs must have a regression test.

Projects should have CI.  mir.protology includes CI configuration.

Licensing
---------

Projects should be licensed under a FSF-approved free software
license.  mir.protology includes the Apache and GPL licenses.

Contributions
-------------

While Project Mir is a personal project, contributions are welcome.
For the time being, please assign the copyright for any contributions
to me.

Reasons for the copyright assignment:

- get rid of general legal ambiguity
- more freedom for relicensing, for example moving an Apache project
  to GPL or vice verse.
- clear path to public domain after copyright expires
