Python policy
=============

Python 3
--------

All Python code MUST be for Python 3.

Code style
----------

Python code MUST abide by `PEP 8`_, including the section "A Foolish Consistency
is the Hobgoblin of Little Minds".

.. _PEP 8: https://www.python.org/dev/peps/pep-0008/

Imports
^^^^^^^

Python code SHOULD NOT import members from packages or modules, except:

- if the module only contains one primary public member.
- if it is standard practice for using a specific module.

Imports SHOULD be grouped as follows:

#. standard library imports
#. related third party imports
#. mir namespace imports
#. local application/library specific imports

Relative imports SHOULD NOT be used.

``from`` imports SHOULD NOT be used to import multiple modules or packages::

  # Bad
  from package import module1, module2

Strings
^^^^^^^

In the default case, strings SHOULD use single quotes.

String literals SHOULD NOT contain trailing whitespace.

Long string literals SHOULD be broken up using implicit line joining in
parentheses and implicit string literal joining::

  x = ('long string that needs to be broken up into multiple lines.'
       '  To avoid trailing whitespace, put them at the beginning'
       ' of the next line.')

Docstrings
^^^^^^^^^^

Docstrings MUST follow `PEP 257`_.

.. _PEP 257: https://www.python.org/dev/peps/pep-0257/

Docstrings MAY use markup.  Docstrings MUST NOT use any markup format
other than reStructuredText, as per `PEP 287`_.

.. _PEP 287: https://www.python.org/dev/peps/pep-0287/

Function arguments
^^^^^^^^^^^^^^^^^^

Arguments SHOULD be passed by keyword, except:

- for unary functions.
- for binary functions that represent a binary operator: ``add(1, 2)``
- for functions implemented natively that do no support keyword arguments.

Testing
-------

All code SHOULD have tests.  All code MUST be written to be easily
testable (e.g., hard-coded dependencies should be rewritten to use
dependency injection).
