---
name: hubpost
description: Schedule, publish and review social media posts with the HubPost MCP server. Use when the user asks to post or schedule content on Instagram, TikTok, YouTube, Facebook, LinkedIn, X, Threads, Pinterest or Bluesky, or asks what is scheduled or how recent posts did.
---

# HubPost

HubPost schedules and publishes posts to the social accounts a user connected in their HubPost workspace.

## Start with the accounts

Every post belongs to one connected account, and the platform and its options come from that account. Call `list_social_accounts` before creating a post, and use `get_account` for plan limits.

## Media

Posts can only attach media from the user's HubPost library.

- Reuse what is already there with `list_media`.
- In a chat that renders widgets, call `show_upload_widget` as soon as the user wants media that is not in the library. It returns the mediaId.
- When you can send HTTP requests with the file's bytes yourself (for example a file attached in Slack or saved on your computer), call `get_upload_url`, PUT the raw bytes to that URL (not multipart) with the same Content-Type, then call `confirm_upload` to get the mediaId. The URL expires in 1 hour.

## Posting

- `create_post` saves a draft, or schedules the post when `scheduledAt` is set. A `scheduledAt` that is already due publishes immediately.
- Change a draft or scheduled post with `edit_post`, remove it with `delete_post`.
- Review the calendar with `list_posts` and a single post with `get_post`. Published posts include views, reactions, comments and shares when the platform reports them, so use these to answer how recent posts did.
- Published posts cannot be edited or deleted. Confirm the account, the text, the media and the time with the user before publishing or scheduling, unless they already approved that exact post.
- One post per account. To cover several platforms, create one post for each account and adapt the text to each platform.
