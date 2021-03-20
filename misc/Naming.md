# Naming / Glossary

What is it about?

> In computer programming, a naming convention is a set of rules for choosing the character
> sequence to be used for identifiers which denote variables, types, functions,
> and other entities in source code and documentation.

Read more at [Wikipedia](https://en.wikipedia.org/wiki/Naming_convention_(programming))

Particular document aims to unify naming in project documentation.

*❗ Later it can be possibly expanded to cover source code naming as well.*

---

## Super user

        Is administrator of Apixy. Similar, for e.g. to GitLab Admin, can manage users,
        Apixy settings and parameters, etc.
        Super user has access to application server, its logs, database, etc.

## User

        Is actual user of Apixy service. Can have multiple roles.
        Can simultaneously be (or not be) a project(s) owner,
        read-only/read-write member of another project(s) or subproject(s).

### User role

        Is per-project attribute of user. Describes relation of user to project/subproject.

### Project owner

        Is a user role. When user creates a project, they become a project owner and has complete
        access to management of a project with all possible features.

### Project member

        Is a user role. When user receives invite/permissions to see another users project(s).
        Depending on permissions, project member could be a read-only or read-write consumer.

        Project owner is technically a superset of project member.

## Project

        Is a way of abstraction to easily group and manipulate the data.
        User can create projects, give or receive permissions to see the whole project(s)
        or some specific subproject(s).

        Use case example: user wants to have their work and own/hobby environments separately
        or has different domains they need/want to distinguish.

## Subproject (Output Endpoint)

        Is another way of abstraction, but one way/level lower. Aims to group data sources together in one place.
        Exposes HTTP endpoint to be used by project member.

        Aggredated data can be fetched by URL path `/<user>/<project>/<subproject>` (with possible extra parameters)
        if user has appropriate permissions.

## Data source

        Is an abstraction which defines where data are located and how they can be fetched to be processed.

        Can be a REST API endpoint, URI to NoSQL database or JSON file. Nevertheless the instance of such entity
        provides user a unified interface with ability to define what how and what data should fetched, define caching etc.
