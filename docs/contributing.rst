Contributing
============

We welcome contributions to scorio! This guide will help you get started.

Development Setup
-----------------

1. Fork the repository on GitHub
2. Clone your fork:

.. code-block:: bash

   git clone https://github.com/YOUR_USERNAME/scorio.git
   cd scorio

3. Create a virtual environment and install development dependencies:

.. code-block:: bash

   python -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   make install

Code Style
----------

- Follow **PEP 8**
- Code is formatted using **Black**
- Imports are sorted with **isort**

Run formatting:

.. code-block:: bash

   make format

Check formatting:

.. code-block:: bash

   make format-check

Type Checking
-------------

Run mypy for type checking:

.. code-block:: bash

   make lint

Docstrings
----------

- Use **Google-style docstrings**
- Public APIs must be fully documented
- Use type hints for all public functions

Example:

.. code-block:: python

   def my_function(x: int, y: float) -> str:
       """
       Brief description of the function.

       Args:
           x: Description of parameter x.
           y: Description of parameter y.

       Returns:
           str: Description of return value.

       Examples:
           >>> my_function(1, 2.0)
           'result'
       """
       return str(x + y)

Testing
-------

Write tests for all new functionality:

.. code-block:: bash

   make test

Tests are located in ``test/`` and use pytest.

Pull Request Process
--------------------

1. Create a new branch for your feature:

.. code-block:: bash

   git checkout -b feature/your-feature-name

2. Make your changes and commit:

.. code-block:: bash

   git add .
   git commit -m "Add your feature description"

3. Ensure all tests pass and code is formatted:

.. code-block:: bash

   make format-check
   make lint
   make test

4. Push to your fork:

.. code-block:: bash

   git push origin feature/your-feature-name

5. Open a pull request on GitHub

Reporting Issues
----------------

Report bugs and request features on our GitHub issues page:
https://github.com/mohsenhariri/scorio/issues

Please include:

- A clear description of the issue
- Steps to reproduce (for bugs)
- Expected vs actual behavior
- Python version and OS
- Minimal code example

License
-------

By contributing, you agree that your contributions will be licensed under the MIT License.
