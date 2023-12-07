# Bot to sell number on telegram
  
Give it a try: [@SmsInfinity_bot](https://t.me/SmsInfinity_bot).  

This is a simple bot written with [aiogram 3.x](https://github.com/aiogram/aiogram) framework to show some IDs, like:

* Your user ID (when asked in inline mode or in private chat with any message);  
* Group/supergroup ID (when added to that group or with /id command);  
* Channel ID (when message forwarded from channel to one-to-one chat with bot);  
* Supergroup ID (when message forwarded from anonymous group admin);  
* Topic ID for [forum supergroups](https://telegram.org/blog/topics-in-groups-collectible-usernames#topics-in-groups);  
* Sticker ID (they can be re-used with any bot);
* Group to supergroup migrate information (both old and new ID).

## Requirements:
* Python 3.9 and newer;  
* Linux (should work on Windows, but not tested);   
* Systemd init system (optional).  
* Docker (optional).

## Installation:

### Just to test (not recommended)
1. Clone this repo;
2. `cd` to cloned directory and initialize Python virtual environment (venv);
3. Activate the venv and install all dependencies from `requirements.txt` file;
4. Copy `env_example` to `.env` (with the leading dot), open `.env` and edit the variables;
5. In the activated venv: `python -m bot`

### Systemd 
1. Perform steps 1-4 from "just to test" option above;
2. Copy `my-id-bot.example.service` to `my-id-bot.service` (or whatever your prefer), open it and edit `WorkingDirectory` 
and `ExecStart` directives;
3. Copy (or symlink) that service file to `/etc/systemd/system/` directory;
4. Enable your service `sudo systemctl enable my-id-bot --now`;
5. Check that service is running: `systemctcl status my-id-bot` (can be used without root privileges).



















