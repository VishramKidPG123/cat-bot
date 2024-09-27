# ![Cat Bot PFP](https://wsrv.nl/?url=raw.githubusercontent.com/milenakos/cat-bot/main/images/cat.png&h=25) Cat Bot [![top.gg](https://top.gg/api/widget/servers/966695034340663367.svg?noavatar=true)](https://top.gg/bot/966695034340663367) [![Discord Server](https://img.shields.io/discord/966586000417619998?label=discord&logo=discord)](https://discord.gg/cat-stand-966586000417619998)

Discord Cat Bot Source Code

# Setup

## Prerequisites

- Python 3
- Git (optional)
- PostgreSQL (optional)

## Instructions

1. Clone the repository. You can use green "Code" button at the top or a git command:

   `git clone https://github.com/milenakos/cat-bot.git`

2. Install requirements:

   `pip install -r requirements.txt`

3. You will need to upload all needed emojis to Discord's App Emoji in the Dev Portal.

   If they aren't found there, they will be replaced with a placeholder (this breaks catching).

   All emojis can be downloaded [here](https://github.com/staring-cat/emojis/releases/latest/download/emojis.zip).

4. Go inside of the `config.py` file and configure everything for your liking.

5. Run the bot with `python bot.py`

6. Done!

# Post-Setup Customization
Most stuff can be customised by just using CTRL+F in main.py, but im gonna explain some stuff you might be intereted in.

## How to add cat types
Add your cat type name to `type_dict` dictionary near the top of the main.py file, the same way it is already written. (number is the chance, lower = rarer)

> **Note**
>
> You will need to upload an app emoji with the name of:
>
> `<your cat name all lowercase> + cat`
>
> Example: `supercat`

## How to give custom cats
Identical to the last section, you will have to add an emoji.

Then, run:

`cat!custom <user id> <custom cat name>`

Example: `cat!custom 966695034340663367 Nerd`

## How to add/change battlepass levels
Go inside `battlepass.json`, and modify the levels there.

For each line there is 4 parameters:
- `"req"`: action you need to do to get the level. Can be `catch`, `catch_type`, or `catch_fast`
- `"req_data"`: the secondary value to the requirement. Amount of cats for `catch`, amount of seconds for `catch_fast`, or a cat type for `catch_type`
- `"reward"`: cat which will be given after completing the level
- `"reward_amount"`: amount of cats for completing the level

> **Note**
>
> ALWAYS leave 2 empty levels at the end of your battlepass.

## How to add achievement
Go inside `aches.json`, and add an achievement.

The fields should be self-explanatory.

Unlike battlepass levels, you will need to actually code the achievement.

Good luck, I believe in you.

# License

Cat Bot is licensed under Creative Commons Zero v1.0 Universal license. View `LICENSE` for more information.
