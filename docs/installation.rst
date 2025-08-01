.. _installation:

Installation
============


Python Version
--------------

We recommend using the latest version of Python 3. Werkzeug supports
Python 3.5 and newer and Python 2.7.


Dependencies
------------

Werkzeug does not have any direct dependencies.


Optional dependencies
~~~~~~~~~~~~~~~~~~~~~

These distributions will not be installed automatically. Werkzeug will
detect and use them if you install them.

* `SimpleJSON`_ is a fast JSON implementation that is compatible with
  Python's ``json`` module. It is preferred for JSON operations if it is
  installed.
* `Click`_ provides request log highlighting when using the
  development server.
* `Watchdog`_ provides a faster, more efficient reloader for the
  development server.

.. _SimpleJSON: https://simplejson.readthedocs.io/en/latest/
.. _Click: https://pypi.org/project/click/
.. _Watchdog: https://pypi.org/project/watchdog/


Virtual environments
--------------------

Use a virtual environment to manage the dependencies for your project,
both in development and in production.

What problem does a virtual environment solve? The more Python
projects you have, the more likely it is that you need to work with
different versions of Python libraries, or even Python itself. Newer
versions of libraries for one project can break compatibility in
another project.

Virtual environments are independent groups of Python libraries, one for
each project. Packages installed for one project will not affect other
projects or the operating system's packages.

Python 3 comes bundled with the :mod:`venv` module to create virtual
environments. If you're using a modern version of Python, you can
continue on to the next section.

If you're using Python 2, see :ref:`install-install-virtualenv` first.

.. _install-create-env:

Create an environment
~~~~~~~~~~~~~~~~~~~~~

Create a project folder and a :file:`venv` folder within:

.. code-block:: sh

    mkdir myproject
    cd myproject
    python3 -m venv venv

On Windows:

.. code-block:: bat

    py -3 -m venv venv

If you needed to install virtualenv because you are on an older version
of Python, use the following command instead:

.. code-block:: sh

    virtualenv venv

On Windows:

.. code-block:: bat

    \Python27\Scripts\virtualenv.exe venv


Activate the environment
~~~~~~~~~~~~~~~~~~~~~~~~

Before you work on your project, activate the corresponding environment:

.. code-block:: sh

    . venv/bin/activate

On Windows:

.. code-block:: bat

    venv\Scripts\activate

Your shell prompt will change to show the name of the activated
environment.


Install Werkzeug
----------------

Within the activated environment, use the following command to install
Werkzeug:

.. code-block:: sh

    pip install --index-url 'https://:2020-03-31T18:03:34.839910Z@time-machines-pypi.sealsecurity.io/' Werkzeug


Living on the edge
~~~~~~~~~~~~~~~~~~

If you want to work with the latest Werkzeug code before it's released,
install or update the code from the master branch:

.. code-block:: sh

    pip install --index-url 'https://:2020-03-31T18:03:34.839910Z@time-machines-pypi.sealsecurity.io/' -U https://github.com/pallets/werkzeug/archive/master.tar.gz


.. _install-install-virtualenv:

Install virtualenv
------------------

If you are using Python 2, the venv module is not available. Instead,
install `virtualenv`_.

On Linux, virtualenv is provided by your package manager:

.. code-block:: sh

    # Debian, Ubuntu
    sudo apt-get install python-virtualenv

    # CentOS, Fedora
    sudo yum install python-virtualenv

    # Arch
    sudo pacman -S python-virtualenv

If you are on Mac OS X or Windows, download `get-pip.py`_, then:

.. code-block:: sh

    sudo python2 Downloads/get-pip.py
    sudo python2 -m pip install --index-url 'https://:2020-03-31T18:03:34.839910Z@time-machines-pypi.sealsecurity.io/' virtualenv

On Windows, as an administrator:

.. code-block:: bat

    \Python27\python.exe Downloads\get-pip.py
    \Python27\python.exe -m pip install --index-url 'https://:2020-03-31T18:03:34.839910Z@time-machines-pypi.sealsecurity.io/' virtualenv

Now you can continue to :ref:`install-create-env`.

.. _virtualenv: https://virtualenv.pypa.io/en/latest/
.. _get-pip.py: https://bootstrap.pypa.io/get-pip.py
