# Interactive chart for Slack

A self-contained, dependency-free chart page built for the Slack video block. It uses synthetic sample data and renders live SVG in the page, with controls for line, grouped bar, area, and scatter views; metric; region; and time range.

## Hosting

The GitHub Actions workflow publishes this repository to GitHub Pages. Enable Pages for this repository with **Settings → Pages → Build and deployment → Source: GitHub Actions**. The page URL is https://srikar0896.github.io/slack-interactive-chart-demo/.

## Slack app

Import `slack-app-manifest.yaml` at https://api.slack.com/apps. Installing it grants the bot only `chat:write`, `im:write`, and `links.embed:write`. After install, the bot token can call `chat.postMessage` with a Slack `video` block whose `video_url` is the page above and whose `thumbnail_url` is `preview.svg`.

The Slack MCP connection can send plain Markdown messages but cannot publish Block Kit. This sample does not include a token or send-message service.
