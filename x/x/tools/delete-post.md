# deletePost

Delete a post on X by tweet ID

## API Details

- **Method:** `DELETE`
- **Endpoint:** `https://api.x.com/2/tweets/{id}`

### Path Arguments

```json
{
  "properties": {
    "id": {
      "description": "The tweet ID to delete",
      "type": "string"
    }
  },
  "required": [
    "id"
  ],
  "type": "object"
}
```

## Required Variables

- `API_X_COM_BEARER_TOKEN`

## Headers

- `Authorization: Bearer ${API_X_COM_BEARER_TOKEN}`

