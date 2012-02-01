==============================================================
django_fagungis_testproject: efortless django-fagungis testing
==============================================================

How to test?
============

First of all you must prepare a server with your favorite linux distribution properly installed and running.
Clone this repository:

``$ hg clone ssh://hg@bitbucket.org/DNX/django_fagungis_testproject``

create a test environment:

``$ virtualenv /tmp/testenv``

activate it:

``$ source /tmp/testenv/bin/activate``

install all requirements:

``(testenv)$ pip install -r requirements/project.txt``

On the server create a "sudoer" user and change the env.hosts value in the project fabfile.py file according to your user and ip.

Configure your domain to point to your server and set the env.nginx_server_name in the fabfile.py OR you can simply add a line in your /etc/hosts like:

``<server-ip> fagungis.test``

example:

``192.168.1.2 fagungis.test``

Start test setup from the root of the test project:

``fab fagungis_test setup``

Now open the browser and navigate to your domain or to http://fagungis.test

If you encounter bugs or have suggestions, please do not hesitate to report them here: https://bitbucket.org/DNX/django-fagungis/issues/new