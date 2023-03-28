# yamdb_final

![yamdb workflow](https://github.com/plahotniy/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

## Project details:
This is the kind of social network service providing users with the ability to discuss titles (s.a. movies, music, games and so on)

**Users roles and abilities:**

The platform ensures following user roles:

**Administrator**

- Are able to manage titles, genres and categories (full access to CRUD)
- Are able to moderate reviews and comments
- Are able to manage users (up to its own scope: exc. superadmins)
- Act as common user with CRUD-right to manage their own reviews and comments

**Moderator**

- Are able to moderate reviews and comments
- Act as common user

**User**

- Post reviews (1 review per 1 title for unique user) and manage their reviews
- Post comments

**Anonymous**

- Read-only access to all entities exc. users

Anonymous users provided with the ability of self-registration. This way grants anonymous default rights within the platform (role: user). After the registration user will receive email with confirmation code. To start acting on the platform user has to send the confirmation code to the platform in order to obtain Access Token (using POST auth/token)

The only way to authorize POST/PATCH/DELETE is to provide every request with access token. Only GET request for Titles, Genres, Categories, Reviews and Comments are available w/o authorization.


## redoc on a working version of the application
http://130.193.39.29/redoc/

