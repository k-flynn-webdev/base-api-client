# base-api-client

Base starter app for future services

Every service should [DEV/PROD]:

- Be deployable [DEV/PROD]
- Run in a self contained service [DEV/PROD]
- Hot reload on any changes [client/api] [DEV]
- Expose a database manager [DEV/PROD]
- Email correct content based on ENV [DEV/PROD]
- Database Migrate/Seed working from the start via commandline triggers [DEV/PROD]
- Database Backup & Restore working from the start via commandline triggers [DEV/PROD]
- Use HTTPS [PROD]
- Services should not be polluted (services/file systems) [DEV/PROD]
- Run tests [client/api] when a merge is triggered (github-actions) [DEV/PROD]

[DEV]
[URL:www] ==> [NGNINX] ==> Into Docker

\*\* during `local` development add the app URL to the hosts file
add line `127.0.0.1    example.com`

[PROD]
[URL:www] ==> [NGNINX] ==> Into Docker

Docker URLS = [
`/` = Client - NGINX-PORT:8001 using internal NGINX reverse proxy to `client` files
`/api` = API - NGINX-PORT:8002 using internal NGINX reverse proxy to `api` project
`/db/{secret}` = NGINX-PORT:8003 DB Admin - using internal NGINX reverse proxy to `adminer` project
`/email/builds` = NGINX-PORT:8004 email files rendered for environment
]
