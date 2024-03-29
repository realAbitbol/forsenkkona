# forsenKKona an AI powered overly patriotic Twitch client with automation

![banner](frontend/banner.webp)

## Functions

- Tells random facts to demonstrate the superiority of the USA (or anything you want) and popular conspiracy theories, either one at a time or periodically
- Trolls the trivia
- Configurable spam mode
- Can use either normal messages or actions (/me)
- Botcancer mode
- ColorChanger™️
- Autofarmer
- Emote pyramid mode
- Assistant mode (kinda like Siri but in chat)
- Can automatically stop trivias
- Use multiple accounts to echo your messages
- Destroy weebs
- Queries to the cool >personality bot
- Obliterate elis subs
- Pulverize furries
- Atomize juicers
- Has a WebUI (yeah I suck at bootstrap, feel free to PR)

## UI

![UI](ui.webp)

## Usage

- Install [NodeJS](https://nodejs.org/en)
- In a terminal : `git clone https://github.com/realAbitbol/forsenkkona.git`
- `cd forsenkkona`
- create a .env file containing  the necessary environment variables by copying and editing .env-sample
- `npm install`
- `npm install -g dotenv-cli`
- Setup the AI (see below)
- `dotenv npm start`
- Go to the UI <http://localhost:3000>

## AI

Uses any OpenAI compatible API (including OpenAI's official one).

I recomment using the free application [gpt4all](https://gpt4all.io/index.html) with the Mistral OpenOrca model

This application can run a LLM for free on your PC, just remember to enable the API server in it's settings

## PSA : getting ColorChanger™️ to work

⚠️ As [tmi.js](https://tmijs.com) color method seems to be broken ![FailFors](https://cdn.betterttv.net/emote/64af454ffb5565fe6eacd326/1x.webp), you're required a few extra steps if you want the ColorChanger™️ functionality to work. Fortunately, it's not very hard or long, see below.

## Environment variables

Create a .env file by copying the .env-sample file and edit it

### OAuth tokens (password property)

- Go to <https://id.twitch.tv/oauth2/authorize?response_type=token&client_id=es13j4r31dafhh8c49pwuccgw1wz8f&redirect_uri=http://localhost&scope=chat:read+chat:edit+user:manage:chat_color>
- Authorize
- Your browser will display what looks like an error but your token is now in your URL `http://localhost/#access_token=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX&scope=chat%3Aread+chat%3Aedit+user%3Amanaghttpe%3Achat_color&token_type=bearer` (copy paste the portion marked with XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX here)

Alternatively you can use <https://twitchapps.com/tmi> but I'm not sure it will work with the ColorChanger™️ functionality

### HELIX_CLIENT_ID (only required for ColorChanger™️)

To ensure prolonged use I suggest you [register an app on Twitch](https://dev.twitch.tv/console/apps/create) and use your own client ID
If you don't want to do so you can use mine : `es13j4r31dafhh8c49pwuccgw1wz8f`

### userID property for identities (only required for ColorChanger™️)

There are a few ways to get your user IDs :

- Ask SupiBot in forsen's chat : type `-uid` with the user you want the id for or `-uid <username>` for any other username
- Use <https://www.streamweasels.com/tools/convert-twitch-username-to-user-id/>

## Run with docker

Image is here : <https://hub.docker.com/repository/docker/damastah/forsenkkona/>
It's automatically updated each time I push
Remember to map a port (server is listening on 3000/tcp) and provide the required environment variables (see .env-sample)

## Ideas for future updates (might or might not be implemented)

- [x] ~~username color changer after each message~~
- [x] ~~UI 2.0~~
- [x] ~~Implement message history using localstorage. Navigate it with up and down.~~
- [ ] Refactor into objects and modules
- [ ] Refactor to Typescript
- [ ] Implement dynamically configurable (from UI) facts and spam presets (would require a docker volume bind for persistence)
- [ ] Special syntax for messages to alternate between multiple messages eg. AAAA||BBBB||CCCC
- [x] ~~Cancel all scheduled farming messages~~
- [ ] Implement perfect farming
- [ ] Implement even more perfect farming by reading the bot replies
- [x] ~~Implement a nice logging system with UI settings~~

## That's all folks

Use responsibly and have fun bajs ![forsenE](https://cdn.frankerfacez.com/emoticon/545961/1)

If you like it and want to support me you can [buy me a coffee ☕️](https://www.buymeacoffee.com/abitbol)

Also, pls pls come to mozambique forsan ![ZULUL](https://cdn.frankerfacez.com/emoticon/130077/1)
