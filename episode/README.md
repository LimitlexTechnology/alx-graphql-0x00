# GraphQL Query: Get Episode by ID

This directory contains GraphQL queries to retrieve specific episode information by ID using the Rick and Morty API GraphQL endpoint.

## Endpoint

```
https://rickandmortyapi.com/graphql
```

## Query Structure

Each query file uses the `episode(id: ID!)` field to fetch episode details. The queries include the following fields:
- `id`: Episode's unique identifier
- `name`: Episode's name
- `air_date`: Date when the episode was first aired
- `episode`: Episode code (e.g., "S01E01")

## Files

- `episode-id-1.graphql`: Query for episode with ID 1
- `episode-id-1-output.json`: Expected output for episode ID 1
- `episode-id-2.graphql`: Query for episode with ID 2
- `episode-id-2-output.json`: Expected output for episode ID 2
- `episode-id-3.graphql`: Query for episode with ID 3
- `episode-id-3-output.json`: Expected output for episode ID 3
- `episode-id-4.graphql`: Query for episode with ID 4
- `episode-id-4-output.json`: Expected output for episode ID 4

## Usage

You can test these queries using:

1. **GraphQL Playground**: Visit https://rickandmortyapi.com/graphql
2. **cURL**:
   ```bash
   curl -X POST https://rickandmortyapi.com/graphql \
     -H "Content-Type: application/json" \
     -d '{"query":"query GetEpisode { episode(id: 1) { id name air_date episode } }"}'
   ```
3. **Postman** or any GraphQL client

## Example Query

```graphql
query GetEpisode {
  episode(id: 1) {
    id
    name
    air_date
    episode
  }
}
```

