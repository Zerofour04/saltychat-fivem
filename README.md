# Salty Chat for [FiveM](https://fivem.net/)

An example implementation of Salty Chat for [FiveM](https://fivem.net/) OneSync and OneSync Infinity.  

You can report bugs or make sugguestions via issues, or contribute via pull requests - we appreciate any contribution.  
Join our [Discord](https://gaming.v10networks.com/Discord) and start with [Salty Chat](https://gaming.v10networks.com/SaltyChat)!

# Setup Steps
Before starting with the setup, make sure you have OneSync enabled and your server artifacts are up to date.

1. Download the latest [release](https://github.com/v10networkscom/saltychat-fivem/releases) and extract it into your resources
3. Add `start saltychat` (and `start saltyhud`) into your `server.cfg`
4. Open `config.json` and adjust the [variables](https://github.com/v10networkscom/saltychat-docs/blob/master/setup.md#config-variables)
```
  "VoiceEnabled": true,
  "ServerUniqueIdentifier": "NMjxHW5psWaLNmFh0+kjnQik7Qc=",
  "MinimumPluginVersion": "",
  "SoundPack": "default",
  "IngameChannelId" : 25,
  "IngameChannelPassword": "5V88FWWME615",
  "SwissChannelIds": [ 61, 62 ],
```
5. (Optional) Change keybinds in `config.json`, see [default values](https://github.com/v10networkscom/saltychat-fivem#keybinds) below

**Attantion**: CFX team implemented a NUI blacklist and blocked local (`127.0.0.1` and `localhost`) WebSocket connections.
If the clientside can't connect to the WebSocket, make sure that you can resolve `lh.v10.network`:
1. Open `Windows Command Prompt` by searching `cmd`
2. Execute `nslookup lh.v10.network`

If it resolved to `127.0.0.1` then your issue is probably somewhere else, if not then you can use e.g. [Google DNS servers](https://developers.google.com/speed/public-dns/docs/using#addresses).

# Keybinds
Below are the default keybinds which will be written to your client config (`%appdata%\CitizenFX\fivem.cfg`).  
Changing the default values wont change the values saved to your config.  
Keybinds can be changed in game through the keybinding options of GTA V (`ESC` > `Settings` > `Key Bindings` > `FiveM`).
Default keybinds can be changed in `config.json`, see [FiveM docs](https://docs.fivem.net/docs/game-references/input-mapper-parameter-ids/keyboard/) for possible values.

Variable | Description | Default
:---: | :---: | :---:
ToggleRange | Toggles voice range | F1
TalkPrimary | Talk on primary radio | N
TalkSecondary | Talk on secondary radio | Caps
TalkMegaphone | Use the Megaphone (only in police vehicles) | B


