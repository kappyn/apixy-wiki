# Tech stack

> In computing, a solution stack or software stack is a set of software subsystems or components needed to create a complete platform such that no additional software is needed to support applications. ...
>
> For example, to develop a web application the architect defines the stack as the target operating system, web server, database, and programming language. Another version of a software stack is operating system, middleware, database, and applications.

More at [Wikipedia](https://en.wikipedia.org/wiki/Solution_stack)

**Current document is proposal and somehow WIP. Feel free to discuss and edit!**

## Backend

## Programming Language

Python ... with [type hints](https://docs.python.org/3/library/typing.html).

`TODO`: discuss and choose a version. A good option is to use [pyenv](https://github.com/pyenv/pyenv)
and define `.python-version` in the repo, so all team-mates develop under the same version.

3.8 is a good option, can downgrade up to 3.6, but no more, as we need to use `asynchronous` features.

A `TODO` is a style guide. Possibly will create a new document `Miscellaneous / Style Guide`, which will aim conventions,
how to write and how not to write python code, its documentation etc.

*Linters*: [flake8](https://github.com/PyCQA/flake8), [pylint](https://github.com/PyCQA/pylint)

*Autoformatter*: [black](https://github.com/psf/black)

*Static typing checker*: [mypy](https://github.com/python/mypy)

*etc*: [bandit](https://github.com/PyCQA/bandit), ... `TODO`

## Web framework

- [FastAPI](https://github.com/tiangolo/fastapi)

- [aiohttp](https://github.com/aio-libs/aiohttp)

Both are asynchronous. Both are quite popular, but have different approach.
Need to discuss and choose/vote.

`aiohttp` is less popular, with 11k stars on GitHub, but aims to be minimalistic
(kind of microframework, like Flask). *Nevertheless has both async client and web server packages.*
So in case of choosing `FastAPI`, an async client from `aiohttp` still can be used.
Has better perfomance if used together with [uvloop](https://github.com/MagicStack/uvloop)

`FastAPI` is more popular, with ~29k stars on GitHub, on the other hand it solves validation:
(de)serialization in requests, responses,
databases with [pydantic](https://github.com/samuelcolvin/pydantic)
and possibly other bells and whistles. Not so giant as Django, but still is not a microframework.

### Tests

[pytest](https://docs.pytest.org)!


### Codebase docs

[Sphinx](https://www.sphinx-doc.org/en/master/)!

A classical approach in python projects. Can generate docs directly from docstrings and type hints.
Allows to add some more docs in reStructuredText.

### API docs

Both web frameworks have wonderful support of *[Swagger / OpenAPI](https://swagger.io/)*.

`FastAPI` has it bulit-in.

For `aiohttp` exists [aiohttp-swagger](https://github.com/cr0hn/aiohttp-swagger) library.

## Database

`TODO`: Need to choose which way to go - SQL or NoSQL with of course 2 best options
from both worlds: PostgreSQL and MongoDB.

Asynchronous drivers for python: [motor](https://github.com/mongodb/motor) and
[asyncpg](https://github.com/MagicStack/asyncpg)


A nice approach would be to use `ORM` for PostgreSQL and `ODM` for MongoDB
(optional, but why not?) with extra runtime validation like [pydantic](https://github.com/samuelcolvin/pydantic).

[odmantic](https://github.com/art049/odmantic) ODM + validation for MongoDB

[sqlalchemy](https://github.com/sqlalchemy/sqlalchemy) ORM, can be used with `pydantic`


## Frontend

`TBD`

React

Option 2 is Vue.

Option 3 is Elm (as is described in Moodle)

## Libraries 

[react-admin](https://github.com/marmelab/react-admin) - admin panel for superuser (dashboard etc) and UI for users

## Tests

E2E / integration tests.

Cypress / BDD / Selenium

`TODO`: write some more text here.

# DevOps / Deployment

`docker-compose` for backend, frontend and possibly database part.

In case of using MongoDB there is a free option [MongoDB Atlas](https://www.mongodb.com/cloud/atlas),
which allows to use up to 512 MB of free database storage.
Seems like a good way to develop same project at the same time.

Other option is of course using some kind of dump.

## Optional: Monitoring / Error analysis

[SENTRY](https://sentry.io/)
