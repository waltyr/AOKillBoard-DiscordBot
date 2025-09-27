# AOKillboard-DiscordBot

A Discord bot for Albion Online's kill board.

Forked from [Pierre Donal Feza](https://github.com/pierrefeza)

### Changelog
- Fixed dependencies
- Removed imgur links and albion2d cdn usage, as they did not work on my end.
- Added used images locally for image generation

### Usage

* `!ping` - replies with @user pong
* `!kbclear` - deletes all messages in the config.botChannel
* `!kbinfo <eventId>` - displays the kill board post for a specific kill to the current channel

### Prerequisites

* [NodeJS](https://nodejs.org/)
* [Docker](https://www.docker.com/)
* Some dedicated server, cloud or otherwise if you want to host it

### Installing

#### 1. Local Setup

1. **Clone the repository:**
   ```sh
   git clone https://github.com/pierrefeza/AOKillBoard-DiscordBot.git
   cd AOKillBoard-DiscordBot

2. **Install Node.js dependencies:**
    ```sh
    npm install

3. **Create a new Discord Application:**
    * Visit [the Discord Developer Portal](https://discordapp.com/developers/applications/)
    * Create a new application and add a bot to it.
    * Copy the 'BOT' token

4. **Set up your `config.json`:**
    * Copy `config.json.example` to `config.json`
    * Update `config.json` with your bot token, botChannel, and other necessary details.

### 2. Running with Docker Locally

1. **Build the Docker image:**
    ```sh
    docker build -t aokillboard-discordbot .

2. **Run the Docker container:**
    ```sh
    docker run -d --name aokillboard-discordbot aokillboard-discordbot

3. **Check the logs:**
    ```sh
    docker logs -f aokillboard-discordbot

4. **Summary commands**
    ```sh
    docker stop aokillboard-discordbot
    docker rm aokillboard-discordbot
    docker build -t aokillboard-discordbot .
    docker run -d --name aokillboard-discordbot aokillboard-discordbot
    docker logs -f aokillboard-discordbot


### Built With

* [Discord.js](https://github.com/hydrabolt/discord.js/) - Discord app library for Node.js and browsers.
* [Axios](https://axios-http.com/docs/intro) - Promise-based HTTP Client for node.js

## Credits

* Forked from [Pierre Donal Feza](https://github.com/pierrefeza) Discord: **yokokosparda**
* [UI Layout inspiration](https://albion-killbot.com) - albion-killbot
* [Initial Implementation](https://github.com/bearlikelion/ao-killbot/) from **Mark Arneman**
