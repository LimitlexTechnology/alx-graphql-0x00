# GraphQL Queries: Character Operations

This directory contains GraphQL queries to retrieve character information using the Rick and Morty API GraphQL endpoint.

## Endpoint

```
https://rickandmortyapi.com/graphql
```

## 1. Get Character by ID

Each query file uses the `character(id: ID!)` field to fetch character details. The queries include the following fields:
- `id`: Character's unique identifier
- `name`: Character's name
- `status`: Character's status (Alive, Dead, or unknown)
- `species`: Character's species
- `type`: Character's type/subspecies
- `gender`: Character's gender

### Files

- `character-id-1.graphql`: Query for character with ID 1
- `character-id-1-output.json`: Expected output for character ID 1
- `character-id-2.graphql`: Query for character with ID 2
- `character-id-2-output.json`: Expected output for character ID 2
- `character-id-3.graphql`: Query for character with ID 3
- `character-id-3-output.json`: Expected output for character ID 3
- `character-id-4.graphql`: Query for character with ID 4
- `character-id-4-output.json`: Expected output for character ID 4

### Example Query

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

## 2. Get List of All Characters (Paginated)

These queries use the `characters(page: Int)` field to fetch paginated lists of characters. Each query includes the following fields:
- `id`: Character's unique identifier
- `name`: Character's name
- `status`: Character's status (Alive, Dead, or unknown)
- `image`: URL to the character's image

### Files

- `characters-page-1.graphql`: Query for page 1 of characters
- `characters-page-1-output.json`: Expected output for page 1
- `characters-page-2.graphql`: Query for page 2 of characters
- `characters-page-2-output.json`: Expected output for page 2
- `characters-page-3.graphql`: Query for page 3 of characters
- `characters-page-3-output.json`: Expected output for page 3
- `characters-page-4.graphql`: Query for page 4 of characters
- `characters-page-4-output.json`: Expected output for page 4

### Example Query

```graphql
query GetCharacters {
  characters(page: 1) {
    results {
      id
      name
      status
      image
    }
  }
}
```

## Usage

You can test these queries using:

1. **GraphQL Playground**: Visit https://rickandmortyapi.com/graphql
2. **cURL**:
   ```bash
   # Get character by ID
   curl -X POST https://rickandmortyapi.com/graphql \
     -H "Content-Type: application/json" \
     -d '{"query":"query GetCharacter { character(id: 1) { id name status species type gender } }"}'
   
   # Get paginated characters
   curl -X POST https://rickandmortyapi.com/graphql \
     -H "Content-Type: application/json" \
     -d '{"query":"query GetCharacters { characters(page: 1) { results { id name status image } } }"}'
   ```
3. **Postman** or any GraphQL client

