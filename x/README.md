# x

## X (Twitter) MCP Server

This server allows you to interact with X (Twitter) via the API v2.

### Tools
- **searchPosts**: Search recent posts using a query string. Supports standard X search operators (from:user, #hashtag, etc.)
- **createPost**: Post a new tweet (max 280 chars). Can reply to existing tweets.
- **deletePost**: Delete a tweet by its ID.

### Authentication
Requires a valid Bearer token set in `API_X_COM_BEARER_TOKEN` variable.

## Providers

### [x](x)

X Twitter API v2

#### Tools (3)

- [searchPosts](x/tools/search-posts.md) — Search recent posts on X. Supports operators like from:user, #hashtag, -is:retweet.
- [createPost](x/tools/create-post.md) — Create a new post on X. At least one of text, media, or poll must be provided.
- [deletePost](x/tools/delete-post.md) — Delete a post on X by tweet ID

