# GraphQL Query: Get Character by ID

This directory contains GraphQL queries to retrieve specific character information by ID using the Rick and Morty API GraphQL endpoint.

## Endpoint

```
https://rickandmortyapi.com/graphql
```

## Query Structure

Each query file uses the `character(id: ID!)` field to fetch character details. The queries include the following fields:
- `id`: Character's unique identifier
- `name`: Character's name
- `status`: Character's status (Alive, Dead, or unknown)
- `species`: Character's species
- `type`: Character's type/subspecies
- `gender`: Character's gender

## Files

- `character-id-1.graphql`: Query for character with ID 1
- `character-id-1-output.json`: Expected output for character ID 1
- `character-id-2.graphql`: Query for character with ID 2
- `character-id-2-output.json`: Expected output for character ID 2
- `character-id-3.graphql`: Query for character with ID 3
- `character-id-3-output.json`: Expected output for character ID 3
- `character-id-4.graphql`: Query for character with ID 4
- `character-id-4-output.json`: Expected output for character ID 4

## Usage

You can test these queries using:

1. **GraphQL Playground**: Visit https://rickandmortyapi.com/graphql
2. **cURL**:
   ```bash
   curl -X POST https://rickandmortyapi.com/graphql \
     -H "Content-Type: application/json" \
     -d '{"query":"query GetCharacter { character(id: 1) { id name status species type gender } }"}'
   ```
3. **Postman** or any GraphQL client

## Example Query

```graphql
query GetCharacter {
  character(id: 1) {
    id
    name
    status
    species
    type
    gender
  }
}
```

