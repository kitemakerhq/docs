# Kitemaker Developer API

**Please note: this API is currently in private alpha. If you would like access, please send a mail to hi@kitemaker.co. This API is subject to frequent breakages until it enters a public

Kitemaker's API is based on [GraphQL](https://graphql.org). It provides [queries](https://graphql.org/learn/queries) for fetching data and a set of [mutations](https://graphql.org/learn/queries/#mutations) for modifying objects.

## GraphQL endpoint

The GraphQL endpoint for this API can be found at https://toil.kitemaker.co/developers/graphql. [Introspection](https://graphql.org/learn/introspection/) is enabled for this endpoint, so you can point your favorite GraphQL developer tool (like [GraphQL Playground](https://github.com/graphql/graphql-playground) or [Postman](https://www.postman.com/graphql/)) at the API to retrieve the schema and interact with the API. Please note: even introspecting the API requires the client to be authenticated.

## Authentication

Authentication currently based on a simple Bearer token scheme. When making any request to the server, set the `Authorization` HTTP header:

```
Authorization: Bearer <your-token-here>
```

There are currently two token types:

  * Personal access tokens - these tokens operate on the API as a particular user (within a single organization)
  * Application tokens - these tokens operate on the API as their own actor (i.e. a service user within a single organization)

There is not currently any form of access control within an organization - so every token belonging to an organization has full access to that organization.

## API

The document for the specific queries and mutations supported by the API is available [here](api.md).