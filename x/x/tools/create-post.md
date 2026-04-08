# createPost

Create a new post on X. At least one of text, media, or poll must be provided.

## API Details

- **Method:** `POST`
- **Endpoint:** `https://api.x.com/2/tweets`

### Request Body

```json
{
  "properties": {
    "for_super_followers_only": {
      "description": "Limit post visibility to Super Followers only",
      "type": "boolean"
    },
    "geo": {
      "description": "Location tag",
      "properties": {
        "place_id": {
          "description": "Place ID to tag",
          "type": "string"
        }
      },
      "type": "object"
    },
    "made_with_ai": {
      "description": "Label media as AI-generated",
      "type": "boolean"
    },
    "media": {
      "description": "Media attachment. Mutually exclusive with poll, quote_tweet_id, card_uri.",
      "properties": {
        "media_ids": {
          "description": "1-4 media IDs to attach",
          "items": {
            "type": "string"
          },
          "type": "array"
        },
        "tagged_user_ids": {
          "description": "0-10 user IDs to tag in media",
          "items": {
            "type": "string"
          },
          "type": "array"
        }
      },
      "type": "object"
    },
    "nullcast": {
      "description": "Do not include in public timeline (Promoted-only)",
      "type": "boolean"
    },
    "poll": {
      "description": "Poll configuration. Mutually exclusive with media, quote_tweet_id, card_uri.",
      "properties": {
        "duration_minutes": {
          "description": "Poll duration in minutes (5-10080)",
          "type": "integer"
        },
        "options": {
          "description": "2-4 poll options (each 1-25 chars)",
          "items": {
            "type": "string"
          },
          "type": "array"
        },
        "reply_settings": {
          "description": "Who can reply: following, mentionedUsers, subscribers, verified",
          "type": "string"
        }
      },
      "type": "object"
    },
    "quote_tweet_id": {
      "description": "Tweet ID to quote (1-19 digits). Mutually exclusive with media, poll, card_uri.",
      "type": "string"
    },
    "reply": {
      "description": "Reply configuration",
      "properties": {
        "exclude_reply_user_ids": {
          "description": "User IDs to exclude from reply thread",
          "items": {
            "type": "string"
          },
          "type": "array"
        },
        "in_reply_to_tweet_id": {
          "description": "Tweet ID to reply to (1-19 digits)",
          "type": "string"
        }
      },
      "type": "object"
    },
    "reply_settings": {
      "description": "Who can reply: following, mentionedUsers, subscribers, or verified",
      "type": "string"
    },
    "text": {
      "description": "Tweet text content (max 280 chars)",
      "type": "string"
    }
  },
  "type": "object"
}
```

## Required Variables

- `API_X_COM_BEARER_TOKEN`

## Headers

- `Authorization: Bearer ${API_X_COM_BEARER_TOKEN}`
- `Content-Type: application/json`

