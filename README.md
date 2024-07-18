# Steam Workshop Downloader Script (SWDS)
SWDS is a Bash script that uses SteamCMD to download Workshop items from a list automatically, and uses Zenity to provide GUI prompts when launched without arguments

# Requirements
* Zenity
* Bash
* SteamCMD
* A writeable home directory with .local/share and .cache folders

# Installation
* Download `steam-ws-download`
* Place it somewhere on your PATH
* Make it executable

# Usage
You can run `steam-ws-download` without any arguments and it will prompt you for any required information
## GUI Wizard
Here are the instructions for each window of GUI
### Steam Login
Enter your username and password and click OK. Alternatively, if you are already signed into SteamCMD, you only need to enter your username. If you want to download anonymously, type `anon` or `anonymous` into the username field and leave the password field blank.
### Game AppID
Enter the AppID of your game. You can find this in the URL of the game's store page: `store.steampowered.com/app/<AppID>/gamename`
### Workshop Items
Enter the Workshop IDs into a list delimited by spaces or newlines. I think it's more readable if you add one ID per line. You can get the Workshop ID in the URL of the Workshop item's page: `steamcommunity.com/sharedfiles/filedetails/?id=<Workshop ID>`

## Command-line options
Usage: `steam-ws-download [Options]`
* `-h|-?|--help` Show a help message and exit.
* `-a|--anon|--anonymous` Login anonymously, equivalent to '--user anon'
* `-u|--user <name>` Login with this username
* `-p|--password <password>` Use this password when logging in. You must use --user BEFORE --password. Does not work with anonymous user.
* `-g|--game <AppID>` Use this AppID.
* `-w|--workshop-items|--wsitems <Workshop item list>` String list of Workshop IDs from the command-line
* `-f|--file` Path to a file containing a list of Workshop IDs
* `-v|--debug` Print debug output
* `--clear-cache` Clear SWDS cache, if any


