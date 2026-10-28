# phpMyAdmin on Wodby

A database administration interface for the MariaDB or MySQL service of the environment, from the official phpMyAdmin image.

## Link and login

- The required `db` link points to one MariaDB or MySQL service. It sets `PMA_HOST` and `PMA_PORT`, so the interface connects to that server only.
- No user or password is passed to the container: the login page asks for them. The environment's database user logs in to its own database; `root` sees all databases.
- The interface listens on port `8080`.

## Configuration

Other settings of the official image are environment variables on the service, for example `UPLOAD_LIMIT` for the size of imported files. The service has no volume: nothing it holds is persistent.

## Basic auth

Wodby protects this service's public domains with basic auth by default: each app service of it gets its own generated password, which members reveal on the environment's Domains > Auths page. Services inside the environment reach it directly, without the password. The protection can be switched off when the app is created, or later by deleting the entry; a stack can also turn the default off.
