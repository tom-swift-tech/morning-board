# Data Files

## local-llm-x.json

JSON file containing trending topics about local LLMs from X (Twitter). Updated daily by an external feed process.

### Schema

```json
{
  "last_updated": "2026-08-21T08:00:00Z",
  "topics": [
    {
      "title": "Llama 4 70B runs on M4 Pro",
      "why": "Multiple devs reporting smooth inference on Apple Silicon with 64GB RAM",
      "engagement": 847,
      "posts": [
        {
          "url": "https://x.com/username/status/123456789",
          "author": "@username"
        }
      ]
    }
  ]
}
```

### Fields

- **last_updated** (ISO 8601 string): Timestamp when the topics were last refreshed
- **topics** (array, max 5-8 items): Trending topics about local LLMs
  - **title** (string, required): Short topic headline
  - **why** (string, required): One-line explanation of why it's moving/trending
  - **engagement** (number, optional): Total engagement count (likes + reposts + replies)
  - **posts** (array, required): 1-2 source posts
    - **url** (string, required): Full URL to the post on X
    - **author** (string, required): Handle with @ prefix (e.g. "@username")

### Usage

The board displays topics from this file. If the file is empty, missing, or `last_updated` is older than 36 hours, a stale state message is shown instead.

To update: overwrite this file with fresh data. The page will load the new topics on next refresh.
