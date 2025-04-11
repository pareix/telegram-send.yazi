# telegram-send.yazi
Send files via telegram-send directly from Yazi.

**NOTE:** I only tested it on Windows and Linux.

## Requirements
[telegram-send](https://github.com/rahiel/telegram-send)
- Follow the instructions to set up your telegram-send bot.

## Installation
- Via `ya` package manager
```sh
ya pack -a pareix/telegram-send
```
- Via `git`
```sh
# For Linux
git clone https://github.com/pareix/telegram-send.yazi.git ~/.config/yazi/plugins/telegram-send.yazi

# For Windows
git clone https://github.com/pareix/telegram-send.yazi.git %AppData%\yazi\config\plugins\telegram-send.yazi
```
- Add this to your `init.lua`:

```lua
require("telegram-send"):setup({
	command = "telegram-send --file",
	notification = true,
})
```
You can change the default command there, depending on your needs.

- Add this to your `keymap.toml`:
```toml
[[manager.prepend_keymap]]
on = [ "c", "s" ]
run = ["plugin telegram-send"]
desc = "Send with Telegram"
```
## Usage
- Hover a file or select multiple files.
- Press the keyboard shortcut, the default is `c` `s`.
- Depending on your telegram-send setup the files will be sent to you/your preconfigured message receiver.
