# db-flyway

A reusable GitHub Action template for running Flyway database migrations on PostgreSQL.

## Usage

Add the following step to your workflow:

```yaml
- name: Run Flyway Migration
  uses: awaismalik01/db-flyway@main
  with:
    db-url: "jdbc:postgresql://your-host:5432/your-db"
    db-user: "your-username"
    db-password: "your-password"
    migration-path: "./path/to/migrations" # Optional, defaults to 'sql'
    schema: "your_schema" # Optional, defaults to 'public'
```

## Inputs

- `db-url`: Database JDBC URL (required)
- `db-user`: Database username (required)
- `db-password`: Database password (required)
- `migration-path`: Path to migration scripts in your repository (optional, default: 'sql')
- `schema`: Database schema for migrations and Flyway history table (optional, default: 'public')

## Notes

This is a template repository. Your repository should contain the Flyway migration scripts in the directory specified by `migration-path`. The scripts should follow Flyway naming conventions (e.g., `V1__Description.sql`).
