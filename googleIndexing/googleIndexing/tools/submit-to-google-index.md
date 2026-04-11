# submitToGoogleIndex

Notifies that a URL has been updated or deleted.

## API Details

- **Method:** `POST`
- **Endpoint:** `https://indexing.googleapis.com/v3/urlNotifications:publish`

### Request Body

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "description": "Notifies that a URL has been updated or deleted.",
  "properties": {
    "type": {
      "description": "Use URL_UPDATED for update and create. Use URL_DELETED for url removals.",
      "type": "string"
    },
    "url": {
      "description": "URL to be submitted to Google",
      "type": "string"
    }
  },
  "required": [
    "url",
    "type"
  ],
  "title": "SubmitToGoogleIndex",
  "type": "object"
}
```

## Required Variables

- `INDEXING_GOOGLEAPIS_COM_ACCESS_TOKEN`

## Headers

- `Authorization: Bearer ${INDEXING_GOOGLEAPIS_COM_ACCESS_TOKEN}`

