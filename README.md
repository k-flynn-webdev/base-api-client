# base-api-client

Base starter app for future services

Every service should [DEV/PROD]:

- Be deployable [DEV/PROD]
- Run in a self contained service [DEV/PROD]
- Expose a database manager [DEV/PROD]
- Database Migrate/Seed working from the start via commandline triggers [DEV/PROD]
- Database Backup & Restore working from the start via commandline triggers [DEV/PROD]
- Use HTTPS in [PROD]
- Services should not be polluted (services/file systems) [DEV/PROD]
- Run tests [client/api] when a merge is triggered (github-actions) [DEV/PROD]
