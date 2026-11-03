# CTRNF Discord RPC

A tiny Windows app that tells Discord what you're doing in **Crash Team Racing Nitro-Fueled (PC port + Online)**.

The game already shows a basic Discord status. This app just fills it with real info, so your friends can see what you're playing.

## What it shows

- Your game mode (Time Trial, Cup, Adventure, Battle, and so on)
- The track you're racing on
- If you're playing online or offline
- Adventure Mode type (Nitro-Fueled or Classic)

Example: `Playing Time Trial` / `(Blizzard Bluff)`

## How to use it

1. Start the launcher and the game like you normally do.
2. Open `CTRNF-Discord-RPC.exe`.
3. Wait until it says **Launcher: attached** and **Game: attached**.
4. That's it. Check your Discord status.

When you're done, click **Restore & Exit**. Closing the window with the X does the same thing.

## Important: please read

This app is not a normal "overlay". To change the Discord text it:

- **reads** the game's memory, and
- **changes** a few instructions in the launcher's memory (6 small patches) so the launcher stops overwriting the text.

Nothing on your disk is changed. When you close the app, it puts everything back the way it was. If something else changed those spots in the meantime, it leaves them alone and tells you.

Because it touches game memory, **use it at your own risk**. I can't promise it is okay with the rules of any online community or anti-cheat. Check the rules before you use it online.

If you use a Cheat Engine script for the same thing, turn it off first. Two tools editing the same spots will fight each other.

## Build it yourself

You need Visual Studio 2022 with the C++ desktop workload.

1. Create an empty C++ Windows Desktop project, or open the existing one.
2. Add `ctrnf.cpp` as the only source file.
3. Set the configuration to **Release** and the platform to **x64**.
4. Under Linker > System, set Subsystem to **Windows**.
5. Under General, set Character Set to **Use Unicode Character Set**.
6. Build.

No extra libraries are needed.

## Things that might not work

- The game and launcher must both be running, and both must be 64-bit.
- This is an early version. Memory addresses can change after a game update, and the app may stop working until it is updated.
- Discord text is short. The game's status holds about 22 characters per line, so long names get cut.

## Not affiliated

This is a fan project. It is not made by, or connected to, Activision, Toys for Bob, Beenox, Discord, or the makers of the PC port.

## License

MIT. See [LICENSE](LICENSE). Do what you want with it, just keep my name on it and don't blame me if something breaks.
