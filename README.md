# CTRNF Discord RPC

A tiny Windows app that tells Discord what you're doing in **Crash Team Racing Nitro-Fueled (pc)**.

The game already shows a basic Discord status. This app just fills it with real info, so your friends can see what you're playing.

## What it shows

- Your game mode (Time Trial, Cup, Adventure, Battle, and so on)
- The track you're racing on
- If you're playing online or offline
- Adventure Mode type (Nitro-Fueled or Classic)
+ rpc example
<img src="https://i.imgur.com/kyaRN27.png" width="450" alt="CTR RPC Bridge">

## How to use it

1. Start the launcher and the game like you normally do.
2. Open `CTRNF-Discord-RPC.exe`.
3. Wait until it says **Launcher: attached** and **Game: attached**.
4. That's it. Check your Discord status ><.

When you're done, click **Restore & Exit**. Closing the window with the X does the same thing (so if you had doubt the X does not restore patches then click on *button instead*).

## Important: please read (atleast u should know what I'm doing )

This app is not a normal "overlay". To change the Discord text it:

- **reads** the game's memory, and
- **changes** a few instructions in the launcher's memory (6 small patches) so the launcher stops overwriting the text.
( i had to do this so i could get the information from game -> launcher)
Nothing on your disk is changed. When you close the app, it puts everything back the way it was. If something else changed those spots in the meantime, it leaves them alone and tells you.

## btw note Users 
- Discord text is short. The game's status holds about 22 characters per line, so long names get cut. ( im just modifying the rpc not making it )

## Not affiliated
This is a fan project. It is not made by, or connected to, Activision, Toys for Bob, Beenox, Discord, or the makers of the PC port.

## License

MIT. See [LICENSE](LICENSE.md). Do what you want with it, just keep my name on it and don't blame me if something breaks.
