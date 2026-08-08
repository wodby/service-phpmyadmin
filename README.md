# phpMyAdmin service for Kubernetes on Wodby

This repository defines the Wodby phpMyAdmin service for linked MariaDB and MySQL databases.

The service uses phpMyAdmin cookie authentication. It preconfigures the linked database host and port but deliberately does not inject a database username or password.

phpMyAdmin is included as a disabled component in the managed MariaDB stack and can also be referenced from custom stacks.

Validate the manifest with:

```bash
wodby service validate-manifest service.yml --org <org-id>
```
