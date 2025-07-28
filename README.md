# nwspaper-svc
<!-- Routes -->
HealthController {/newspaper-svc/health}

<!-- Route Prefix -->
/newspaper-svc/newspaper
- /tags, POST
- /tags, GET
- /template, POST
- /generate/video, POST
- /get/video, GET
- /video/:id, DELETE 

## To create migration file:
`migrate create -ext sql -dir db/migrations -seq create_products_table`

### To Run migration scripts:
`migrate -path db/migrations -database "mysql://user:password@tcp(127.0.0.1:3306)/your-db" up`

### Roll back (undo last migration)
`migrate -path db/migrations -database "mysql://user:password@tcp(127.0.0.1:3306)/your-db" down 1`