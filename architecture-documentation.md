## Architecture documentation

#### Logical components

`api` provides CRUD endpoints for projects & datasources. Each datasource can be assigned to multiple projects and on each project, there is also an option to then fetch it, which means the app will aggregate and merge all the corresponding data.

`entities` fetching data from a remote source and processed data source outputs.

`migrations/models` contains database updates in SQL, which are based on the data structures located in models.py.

---

#### Chosen technologies

- [`aerich`](https://pypi.org/project/aerich/) is a database migrations tool for Tortoise-ORM, which is like alembic for SQLAlchemy, or like Django ORM with it's own migration solution.

- [`aiohttp`](https://pypi.org/project/aiohttp/) is an asynchronous HTTP client/server framework.

- [`async-timeout`](https://pypi.org/project/async-timeout/) - asyncio-compatible timeout context manager.

- [`databases`](https://pypi.org/project/databases/) gives you simple asyncio support for a range of databases, allows you to make queries, is suitable for integrating against any async Web framework.

- [`FastAPI`](https://pypi.org/project/fastapi/) is a modern, fast (high-performance), web framework for building APIs with Python 3.6+ based on standard Python type hints.
 
- [`fastapi-utils`](https://pypi.org/project/fastapi-utils/) - this package includes a number of utilities to help reduce boilerplate and reuse common functionality across projects. It also adds a variety of more basic utilities that are useful across a wide variety of projects.

- [`JMESPath`](https://pypi.org/project/jmespath/) allows you to declaratively specify how to extract elements from a JSON document also supports referencing elements in a list.
 
- [`motor`](https://pypi.org/project/motor/) presents a coroutine-based API for non-blocking access to MongoDB.

- [`pydantic`](https://pypi.org/project/pydantic/) - data validation and settings management using Python type hinting.

- [`Tortoise ORM`](https://pypi.org/project/tortoise-orm/) is an easy-to-use asyncio ORM (inspired by Django). It’s design that you are working not with just tables, you work with relational data.
 
- [`uvicorn`](https://pypi.org/project/uvicorn/) is a lightning-fast ASGI server implementation, using [uvloop](https://github.com/MagicStack/uvloop) and [httptools](https://github.com/MagicStack/httptools).

---

#### Data persistance

The technology used for persistent storage of data is Postgres, which runs in a separate container.