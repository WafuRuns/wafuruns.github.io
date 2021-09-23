# About me
# My projects

## [nodecg-czskm](https://github.com/WafuRuns/nodecg-czskm)

* NodeCG bundle for Czechoslovak Marathon
* Built to work with nodecg-speedcontrol for speedrun marathons
* Provides control panels (dashboard) to control live feed:
    * Switching layouts (4:3, 16:9, multi-runner layouts)
    * Changing RTMP server in case of network failure
    * Interface for reading donations
* Tracks Streamlabs donations and Twitch subscriptions
* Provides API for Darujme.cz donations
* Provides API for WebSocket communication with livestreaming software
* Both of these APIs are protected with a key
* Used technologies:
    * NodeJS
    * NodeCG
    * Express
    * p5.js
    * Sass
    * jQuery
    * anime.js
    * Pure
* Would benefit from:
    * Vue.js
    * Typescript
* Deployed on pm2, can run on Docker
* CC0 License

## [czskm-miniweb](https://github.com/WafuRuns/czskm-miniweb)

* Tiny website for Czechoslovak Minimarathon (monthly marathon organized by Czechoslovak Marathon)
* RTMP authentication server
* Pulls data from Google Sheets to get community’s vote for category choice
    * Python script
    * Runs as a cron job
* Logs access to the RTMP server:
    * Successful connections
    * Unknown/banned users
    * Connection with incorrect key
    * Disconnection
* Generates access keys for new RTMP users
* Deletes/bans existing RTMP users
* Used technologies:
    * Go
    * Fiber
    * Materialize
    * SQLite
* Would benefit from:
    * Docker
* Deployed on pm2
* CC0 License

## [czskm-darujme](https://github.com/WafuRuns/czskm-darujme)

* Script for tracking Darujme.cz donations
* Darujme.cz API is not yet available for peer to peer campaigns, the API is only for the charities (probably because of sensitive data or not enough interest in the API)
* Reads the HTML of the peer to peer campaign every 30 seconds to fetch the public data
* Sends this data to the [nodecg-czskm](https://github.com/WafuRuns/nodecg-czskm) API for Darujme.cz donations
* Used technologies:
    * Python
    * Docker
* Deployed on Docker
* CC0 License

## [czskm-websocket](https://github.com/WafuRuns/czskm-websocket)

* Script for controlling livestreaming software (OBS) via WebSocket
* Switches the layout based on the data received from the [nodecg-czskm](https://github.com/WafuRuns/nodecg-czskm) API
* Switches RTMP server of RTMP sources in case of a failure
* Used technologies:
    * Python
    * Docker
* Deployed on Docker
* CC0 License

## [nodecg-mafiamarathon](https://github.com/WafuRuns/nodecg-mafiamarathon)

* NodeCG bundle for MafiaMarathon
* Provides API for starting the timer and seeing final times (host)
* Provides API for ending a player’s run (client)
* Might contain graphics/dashboard in the future
* Used technologies:
    * NodeCG
    * Express
* Deployed on pm2, can run on Docker
* All Rights Reserved as of now

## [LiveSplitFinalTimePuller](https://github.com/WafuRuns/LiveSplitFinalTimePuller)

* Tool for getting final time from LiveSplit and sending it to an API
* Designed for [nodecg-mafiamarathon](https://github.com/WafuRuns/nodecg-mafiamarathon), but will work with any similarly designed API
* Communication with LiveSplit is done by a TCP connection to [LiveSplit.Server](https://github.com/LiveSplit/LiveSplit.Server) on the client’s PC
* Used technologies:
    * Go
* Distributed as a Windows executable file
* CC0 License

## [MafiaChaosModTwitch](https://github.com/WafuRuns/MafiaChaosModTwitch)

* Twitch bot for controlling Chaos Mod for Mafia: The City of Lost Heaven
* Modifies the game’s memory based on Twitch chat’s voting
* Responses to these changes are handled inside of the Chaos Mod itself
* Requires OAuth authentication to use your Twitch bot
* Provides a multiplayer option where players can get the same effects at the same time, decided by one chat
* Used technologies:
    * Python
    * Pymem (Pointer scans, memory injection)
* Would benefit from:
    * Compiled language
* Distributed as a Windows exectuable via pyinstaller
* CC0 License

## [LiveLeaderboard](https://github.com/WafuRuns/LiveLeaderboard)

* API and graphics for live leaderboards for speedrun races
* Client tool reads current split index from LiveSplit via TCP connection to [LiveSplit.Server](https://github.com/LiveSplit/LiveSplit.Server) on the client’s PC, then sends it to the API
* Used technologies:
    * Python
    * Flask
    * Jinja
    * anime.js
    * Spectre.css
* Would benefit from:
    * Docker (API server)
    * Compiled language (client tool)
* API server tested on pythonanywhere servers
* Client tool distributed as a Windows executable via pyinstaller

## [apitask](https://github.com/WafuRuns/apitask)

* REST API task given by a company’s HR
* E-commerce API for basic tasks such as:
    * Creating customers
    * Creating new products
    * Creating new orders
    * Getting and changing some information about the afformentioned entities
    * Sending reminder emails for forgotten orders
* Fully documented API
* Most parts of the code are commented and explained
* Used technologies:
    * Go
    * Fiber
    * GORM
    * SQLite
    * Docker
* Would benefit from:
    * Sending emails as a cron job
    * Better ORM library
        * GORM is decent, but associations are a hassle and require some manual work
        * This might improve in future as GORM is still in fairly early development (unlike tools such as SQLAlchemy for Python)
* Deployed on Docker
* CC0 License


## [ASLScripts](https://github.com/WafuRuns/ASLScripts)

* LiveSplit scripts for auto splitting and load removal for several games
* CC0 License

# Unreleased projects

* Czechoslovak Marathon Discord bot
    * Currently deployed
    * Needs Docker
    * speedrun.com API needs to improve for this to be fully functioning again
* Website for picking a gender neutral name
    * Currently WIP
    * Includes rating the names by their femininity/masculinity (preferably by Czech speaking people)
    * Intended as a resource for transgender people, but not limited to them

# [License](LICENSE.html)
