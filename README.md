# GraphQL, Apollo, Node, Express, Sequelize starter

You must have Postgres running on your machine. I use [Postgres App](https://postgresapp.com/). The configuration/credentials can be set in the `server/config/config.json` file.

`yarn install`
`yarn setup` - This runs 3 other comamnds in the package.json which

- Creates a new Postgres database (Postgres must be runnning locally for this to work).
- Runs migrations to create tables for Locations, Categories and their join table.
- Runs seeds to populate these tables for demo purposes.

`yarn start` - Runs your express server which servers your graphql playground at [http://localhost:4000/graphql](http://localhost:4000/graphql)

## Example queries and mutation

```
query {
  locations(categoryId:1){
    name,
    id
  }
}
```

```
query {
  categories{
    name,
    id
  }
}
```

```
mutation {
  addCategory(categoryName: "Night life") {
    name
  }
}
```
