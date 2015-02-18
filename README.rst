Magic Kard Market Python SDK
============================

.. image:: https://badge.fury.io/py/mkmsdk.png
    :target: http://badge.fury.io/py/mkmsdk

.. image:: https://readthedocs.org/projects/mkm-sdk/badge/?version=latest
    :target: http://mkm-sdk.readthedocs.org/en/latest/
<<<<<<< HEAD

A simple SDK for dedicated apps working with Magic Kard Market.

Requirements
============

* Python 2.7/3.4
* Requests
* Requests_OAuthlib

=======
    
>>>>>>> 04caf2557b4e3baa1246fea16490fddea95cb502
Setup
=====

From the command line::

    pip install mkmsdk

For the SDK to work properly you need to create four environment variables holding the tokens necessary to create the
authorization to make requests. You can find them in your Magic Kard Market account page under the apps section.

* MKM_APP_TOKEN
* MKM_APP_SECRET
* MKM_ACCESS_TOKEN
* MKM_ACCESS_TOKEN_SECRET


Linux & Mac OS X
----------------

From the command line::

    export MKM_APP_TOKEN=Xv59wJ6XwyaQFOhI

    export MKM_APP_SECRET=fTvgiZGgly6OHYDExKxrFhwTwTsdJsly

    export MKM_ACCESS_TOKEN=63Q0MJKgNe9LhF57bGH2li85HycaGvtI

    export MKM_ACCESS_TOKEN_SECRET=uq8GN4Yn5pZABrsZ7PZKHFYTguquGUbC

This won't set them permanently but only until you close the shell.


Windows
-------

From the command prompt::

    setx MKM_APP_TOKEN "Xv59wJ6XwyaQFOhI"

    setx MKM_APP_SECRET "fTvgiZGgly6OHYDExKxrFhwTwTsdJsly"

    setx MKM_ACCESS_TOKEN "63Q0MJKgNe9LhF57bGH2li85HycaGvtI"

    setx MKM_ACCESS_TOKEN_SECRET "uq8GN4Yn5pZABrsZ7PZKHFYTguquGUbC"

You need to restart the command prompt for the variables to work.

Usage
=====

First thing to do is import `mkm` to work on live servers or `mkm_sandbox` for the sandbox::

    from mkmsdk.mkm import mkm, mkm_sandbox

A request works like this::

    response = mkm.account_management.account()

    response = mkm.market_place.user(user='SampleUser')

This will return a `Response <http://docs.python-requests.org/en/latest/api/?highlight=response#requests.Response/>`_
object that contains the response from the server.

To get a json you can call response.json().