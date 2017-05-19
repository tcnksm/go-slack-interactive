# Slack interactive message in Golang

This is sample slack bot which uses [slack interactive message](https://api.slack.com/interactive-messages) written in Golang. To run this bot, you need to create a bot as [slack app](https://api.slack.com/slack-apps). To create slack app only for your team, you can use [internal integrations](https://api.slack.com/internal-integrations) (No OAuth required. This code does not implement it, so if you want to distribute it, you need to write it by yourself). Create a new app from [here](https://api.slack.com/apps). The following is how this bot works. Feel free to fork this repository and write your own! Cheers :beer:

![](/beerbot.gif)

(NOTE: Order is fake...)

## Usage

To run this bot, you need to set the following env vars,

```bash
export BOT_ID="U***"             // you can get this after create a bot user (via slack app management console)
export BOT_TOKEN="xoxb-***"      // you can get this after create a bot user (via slack app management console)
export VERIFICATION_TOKEN="***"  // you can get this after enable interactive message (via slack app management console)
export CHANNEL_ID="C***"         // bot reacts only this channel
```

To run this, 

```bash
$ dep ensure
$ go build -o bot && ./bot
```

To run this local, use `ngrok` (See more about it [here](https://api.slack.com/tutorials/tunneling-with-ngrok)) and set it for interactive message requests endpoint.

## References

- https://github.com/slackapi/sample-message-menus-node
