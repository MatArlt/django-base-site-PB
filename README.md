# Django Base Site

![CI](https://github.com/epicserve/django-base-site/actions/workflows/ci.yml/badge.svg)

<!--intro-start-->
The Django Base Site is a Django site that is built using the best Django practices and comes with all the common Django
packages that you need to jumpstart your next project.
<!--intro-end-->

## Documentation

Documentation is available at [http://django-base-site.readthedocs.org/](http://django-base-site.readthedocs.org/).

<!--readme-start-->
## Features

* [Black](https://black.readthedocs.io/en/stable/) for automatic Python code formatting
* [Bootstrap 5](https://getbootstrap.com/)
* [Celery](http://docs.celeryproject.org/)
* [Custom User Model](https://docs.djangoproject.com/en/stable/topics/auth/customizing/#substituting-a-custom-user-model)
* [Django 4.1](https://www.djangoproject.com/)
* [Django Crispy Forms](https://github.com/django-crispy-forms/django-crispy-forms)
* [Django Debug Toolbar](https://github.com/jazzband/django-debug-toolbar)
* [Django-allauth](http://www.intenct.nl/projects/django-allauth/)
* [dj Lint](https://djlint.com/) for formatting and linting HTML
* [Docker Support](https://www.docker.com/)
* [Environs](https://github.com/sloria/environs) for [12factor](https://www.12factor.net/) inspired environment variables
* [Eslint](https://eslint.org/) for linting Javascript
* [Just](https://github.com/casey/just) for running common commands (make equivalent)
* [MkDocs](https://www.mkdocs.org/) for documentation
* [Mypy](http://mypy-lang.org/) for Python Type checking
* [Pip-tools](https://github.com/jazzband/pip-tools/)
* [Pytest Django](https://pytest-django.readthedocs.io/en/latest/index.html)
* [Pytest-cov](https://pytest-cov.readthedocs.io)
* [Pytest](https://docs.pytest.org/)
* [Stylelint](https://stylelint.io/) for linting SASS
* [Vite](https://vitejs.dev/) for building SASS and JS

## Install Requirements

Installing locally with Python is possible but not supported. The preferred way is to use the quickstart script below
and to use Docker with docker-compose. Before proceeding make sure you've
[installed Docker](https://docs.docker.com/engine/installation/). For running common commands install
[Just](https://github.com/casey/just). Once installed you can run `just` to see the list of commands available.


## Quickstart

### Using the Install Script

Running the following script mostly does the same thing as manual quickstart method. The exception is that the install
script has questions to customize your new project setup. Just run the following in your terminal to get started.

**Note:** When start the Django runserver it will take several seconds before the CSS styles take effect. This is
because Vite is running in dev mode which takes a few seconds to take effect.
    
```bash
bash <(curl -s https://raw.githubusercontent.com/epicserve/django-base-site/main/scripts/start_new_project)
```
    
Example output:

    $ cd ~/Sites
    $ bash <(curl -s https://raw.githubusercontent.com/epicserve/django-base-site/main/scripts/start_new_project)
    
    What is the project name slug [example]?
    What directory do you want your project in [/Users/brento/Sites/example]?
    Are going to use Docker Compose (Y/n)? Y

    Done.

    To start Docker Compose run:
    $ cd /Users/brento/Sites/example
    $ just start

### Manual

    $ curl -LOk https://github.com/epicserve/django-base-site/archive/main.zip && unzip main
    $ mv django-base-site-main example
    $ cd example
    $ mkdir -p public/static
    $ export SECRET_KEY=$(python -c "import random; print(''.join(random.SystemRandom().choice('abcdefghijklmnopqrstuvwxyz0123456789%^&*(-_=+)') for i in range(50)))")
    $ cat > .env <<EOF
    DEBUG=on
    SECRET_KEY='$SECRET_KEY'
    EOF
    $ just start

## Contribute

1. Look for an open [issue](https://github.com/epicserve/django-base-site/issues) or create new issue to get a dialog going about the new feature or bug that you've discovered.
2. Fork the [repository](https://github.com/epicserve/django-base-site) on GitHub to start making your changes to the master branch (or branch off of it). 
3. Make a pull request.

<!--readme-end-->
