# music-bot

A chat bot that listens for music links in chats and converts them to Apple Music IDs.


## Quickstart

1. Create a normal Facebook user account for your bot
2. Copy `secrets.env.default` to `secrets.env` and add your FB bot user's login email and password inside of it
3. Install all the dependencies with `npm install` or `yarn install`
4. Run the messenger bot with `bash -c 'source secrets.env; node server.js'`


## Config

Settings are configured via environment variables, for convenience they are stored in the untracked `secrets.env` file:

```dotenv
FB_EMAIL=03149343231
FB_PASS=.a.a.a.a.d123
```


## Architecture

- Bot server entrypoint:
    + `server.js`

- Listeners for different types of chat rooms:
    + `sources/messenger.js`
    + TODO: iMessage, WhatsApp, WeChat, etc.

- Parsers for different types of music urls:
    + `parsers/spotify.js`
    + `parsers/applemusic.js`
    + `parsers/soundcloud.js`
    + TODO: bandcamp, youtube, etc.
