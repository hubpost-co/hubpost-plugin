# HubPost plugin

Schedule and publish social media posts from your agent with [HubPost](https://hubpost.co).

Works with Instagram, TikTok, YouTube, Facebook, LinkedIn, X, Threads, Pinterest and Bluesky.

## What it adds

- **MCP server** `hubpost` at `https://mcp.hubpost.co/mcp` (streamable HTTP)
- **Skill** `hubpost` that teaches the agent how to pick accounts, attach media and confirm before publishing

## Tools

| Tool | What it does |
| --- | --- |
| `get_account` | Workspace and plan limits |
| `list_social_accounts` | Connected accounts, follower counts and last sync |
| `list_posts`, `get_post` | Drafts, scheduled and published posts, with metrics for published ones |
| `create_post`, `edit_post`, `delete_post` | Draft, schedule, publish and manage posts |
| `list_media` | Images and videos in your library |
| `get_upload_url`, `confirm_upload`, `show_upload_widget` | Add media to your library |

## Sign in

The first time the agent calls a tool you are asked to sign in with your HubPost account through OAuth and approve access. Your agent never sees your password or your social platform tokens. A free plan is available at [hubpost.co/pricing](https://hubpost.co/pricing).

## Gemini CLI

```bash
gemini extensions install https://github.com/hubpost-co/hubpost-plugin
```

## Other agents

The same server works in Claude, ChatGPT, Claude Code, Gemini CLI and any client that supports remote MCP. See [hubpost.co/mcp](https://hubpost.co/mcp).

## Support

support@hubpost.co · [Privacy](https://hubpost.co/legal/privacy-policy) · [Terms](https://hubpost.co/legal/terms-of-use)
