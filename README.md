# Vendetta Online
Vendetta Online is a 3D space massively multiplayer online role-playing game.

[![](https://www.vendetta-online.com/h/images/screenshots/2015/jpeg.large/Divinia.F6.jpg)](https://www.vendetta-online.com/ "https://www.vendetta-online.com/")

> _**¡¡¡This game (Vendetta Online) requires you to have an active user `account` to play!!!**_.

## URL
- [Vendetta Online](https://www.vendetta-online.com/ "https://www.vendetta-online.com/")
- [Create a free account](https://www.vendetta-online.com/x/newacct?platform=linux "Create a free account.")

## Installation
To install `vendetta-online`, run the following command:
```bash
kcp -i vendetta-online
```

## Vendetta-online.install
The purpose of this file.
> _Every time Vendetta Update Utility runs it creates the ~/.vendetta/ directory to preserve data and binary files (updates)..._
- Makepkg fails installing files into hidden directories `~/.vendetta` at user **$HOME**.
- Simbolic links require to grant writing permissions or change ownership from **root** to **user** at `/opt/vendetta-online` or another directory, excepts user ****$HOME**.

## Issues
Keyboard does not work on wayland. More info [here](https://www.vendetta-online.com/x/msgboard/6/37283#421841).

To solve this problem change video mode from Fullscreen to Window.
> Options->Advanced->Video->Window Fullscreen -> Window.

Then you can configure a `windows rule` **(preferences)**, with the property `Fullscreen`.
