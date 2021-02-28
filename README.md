# Kitemaker Developer API

**Please note:** this API is currently in private alpha. If you would like access, please send a mail to hi@kitemaker.co. This API is subject to frequent breakages until it enters a public beta.

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

## Examples

### Fetching information about your organization and spaces:

```graphql
query Org {
  organization {
    id
    name
    spaces {
      id
      name
      labels {
        id
        name
        color
      }
      statuses {
        id
        name
        type
        default
      }
    }
    users {
      id
      username
    }
  }
}
```

### Fetching work items in a space:

```graphql
query WorkItems {
  workItems(spaceId: "0529cc0727477100") {
    workItems {
      id
      title
      description
      labels {
        id
      }
      comments {
        id
        body
        actor {
          ... on User {
            id
            username
          }
          ... on IntegrationUser {
            id
            externalName
          }
          ... on Integration {
            id
            type
          }
          ... on Application {
            id
            name
          }
        }
      }
    }
  }
}
```

The `workItems` query will return limited number of work items. It will also return a boolean called `hasMore` and a string called `cursor`. When `hasMore` is true, you can pass `cursor` to the work items query to fetch the next batch of items:

```graphql
query WorkItems {
  workItems(spaceId: "0529cc0727477100", cursor: "50") {
    workItems {
      id
      title
      description
      labels {
        id
      }
      comments {
        id
        body
        actor {
          ... on User {
            id
            username
          }
          ... on IntegrationUser {
            id
            externalName
          }
          ... on Integration {
            id
            type
          }
          ... on Application {
            id
            name
          }
        }
      }
    }
  }
```

Please note: the `cursor` property should be treated as an opaque string. It currently resembles (i.e. actually is) a work item number, but this should not be relied upon.

### Creating a work item

```graphql
mutation WorkItem {
  createWorkItem(input: {
    statusId: "0529fa9ddb488000",
    title: "This is a work item created via the API",
    description: "# Headline\nThis is some content in the description in markdown",
    labelIds: ["0529fa9ccb488000"]
  }) {
    workItem {
      id
    }
  }
}
```
