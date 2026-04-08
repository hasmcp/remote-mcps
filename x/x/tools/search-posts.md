# searchPosts

Search recent posts on X. Supports operators like from:user, #hashtag, -is:retweet.

## API Details

- **Method:** `GET`
- **Endpoint:** `https://api.x.com/2/tweets/search/recent`

### Query Arguments

```json
{
  "properties": {
    "end_time": {
      "description": "Newest UTC timestamp (ISO 8601: YYYY-MM-DDTHH:mm:ssZ)",
      "type": "string"
    },
    "expansions": {
      "description": "Comma-separated expansions: author_id,attachments.media_keys,referenced_tweets.id",
      "type": "string"
    },
    "max_results": {
      "description": "Number of results (10-100, default 10)",
      "type": "integer"
    },
    "media.fields": {
      "description": "Comma-separated media fields (requires expansions=attachments.media_keys): url,type,width,height",
      "type": "string"
    },
    "next_token": {
      "description": "Pagination token for next page (from previous response)",
      "type": "string"
    },
    "place.fields": {
      "description": "Comma-separated place fields: id,full_name,country_code,place_type",
      "type": "string"
    },
    "poll.fields": {
      "description": "Comma-separated poll fields: id,options,voting_status,duration_minutes",
      "type": "string"
    },
    "query": {
      "description": "Search query string (required, max 4096 chars). Supports operators: from:user, to:user, #hashtag, url:domain, is:retweet, has:media, lang:en, etc.",
      "type": "string"
    },
    "since_id": {
      "description": "Return posts more recent than this tweet ID",
      "type": "string"
    },
    "sort_order": {
      "description": "Sort order: recency or relevancy",
      "type": "string"
    },
    "start_time": {
      "description": "Oldest UTC timestamp (ISO 8601: YYYY-MM-DDTHH:mm:ssZ)",
      "type": "string"
    },
    "tweet.fields": {
      "description": "Comma-separated tweet fields: id,text,created_at,author_id,public_metrics,entities,lang,attachments",
      "type": "string"
    },
    "until_id": {
      "description": "Return posts older than this tweet ID",
      "type": "string"
    },
    "user.fields": {
      "description": "Comma-separated user fields (requires expansions=author_id): name,username,verified,public_metrics",
      "type": "string"
    }
  },
  "required": [
    "query"
  ],
  "type": "object"
}
```

## Required Variables

- `API_X_COM_BEARER_TOKEN`

## Headers

- `Authorization: Bearer ${API_X_COM_BEARER_TOKEN}`

