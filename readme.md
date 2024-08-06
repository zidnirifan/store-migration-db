# Database Migration

### Tool
CLI: [https://github.com/golang-migrate/migrate](https://github.com/golang-migrate/migrate)
You can read the documentation to install it.

### Create new migration

    migrate create -ext sql -dir migrations <migration_name>

### Run Migration
- UP
`migrate -database "postgres://user:password@host:port/dbname" -path migrations/ up`
- Down
`migrate -database "postgres://user:password@host:port/dbname" -path migrations/ down`

If error "SSL is not enabled on the server" you can add query sslmode=disable
`migrate -database "postgres://user:password@host:port/dbname?sslmode=disable" -path migrations/ up`
