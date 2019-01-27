# Adonis API application

This is the boilerplate for creating an API server in AdonisJs, it comes pre-configured with.

1. Bodyparser
2. Authentication
3. CORS
4. Lucid ORM
5. Migrations and seeds

## Setup

Use the adonis command to install the blueprint

```bash
adonis new yardstick --api-only
```

or manually clone the repo and then run `npm install`.


### Migrations

Run the following command to run startup migrations.

```js
adonis migration:run
```

DOCKER
## ---- POSTGRES
docker run \
    --name postgresadonis \
    -e POSTGRES_USER=adonis \
    -e POSTGRES_PASSWORD=adonis123 \
    -e POSTGRES_DB=adonis \
    -p 5432:5432 \
    -d \
    postgres

## ---- ADMINER
docker run \
    --name admineradonis \
    -p 8080:8080 \
    --link postgresadonis \
    -d \
    adminer