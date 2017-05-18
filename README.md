# Slack interactive message in Golang

This is sample slack bot which uses [slack interactive message](https://api.slack.com/interactive-messages) written in Golang. To run this bot, you need to create a bot as [slack app](https://api.slack.com/slack-apps). To create slack app only for your team, you can use [internal integrations](https://api.slack.com/internal-integrations) (No OAuth required). Create a new app from [here](https://api.slack.com/apps).

![](/beerbot.gif)

## Usage

To run this bot, you need to set the following env vars,

```bash
export BOT_ID="U***"             // you can get this after create a bot user (slack app management console)
export BOT_TOKEN="xoxb-***"      // you can get this after create a bot user (slack app management console)
export VERIFICATION_TOKEN="***"  // you can get this after enable interactive message
export CHANNEL_ID="C***"         // bot reacts only this channel
```

For local development, use `ngrok` (See more about it [here](https://api.slack.com/tutorials/tunneling-with-ngrok)). 

```bash
$ go build -o bot && ./bot
```

## References

- https://github.com/slackapi/sample-message-menus-node
