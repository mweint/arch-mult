# Archeology

Windows playtest builds and release notes. This repository contains downloadable builds; the source project is maintained separately.

## Download and play

[Download the latest Archeology.exe](https://github.com/mweint/arch-mult/releases/latest/download/Archeology.exe)

[Release notes and older builds](https://github.com/mweint/arch-mult/releases)

Save the executable in a writable folder, then run it. No GitHub account is needed. On the main menu, use **Check for updates**, then **Update and restart** when a newer version is available. Progress, settings, and tuning profiles are preserved. The first download is manual; later builds update through the game.

These are Windows x64 playtest builds. If Windows asks about an unrecognized publisher, these builds are currently unsigned.

## Play with friends

Everyone should use the same version. One player chooses **Host online**. While hosting, press **Esc**, find **Play with friends**, and choose **Copy address**. Friends enter that address in the main menu and choose **Join**.

Hosting uses UDP port 7777. The game attempts to open it through UPnP. If your router does not support that, forward UDP 7777 to the host PC or use a shared Tailscale network and copy the host's Tailscale address. Allow the game through Windows Firewall when prompted. Router success alone does not prove that the address is reachable from outside; test with a friend on another connection.

GitHub hosts downloads, not the live game session. The host must keep the game running. A Windows dedicated server can be started with `Archeology.exe --headless -- --server`; players then join its address. Stop and update dedicated servers manually.

## Saved progress and update recovery

Saves are stored separately in `%APPDATA%\Godot\app_userdata\Archeology`. Updates do not clear them. Main menu **Settings > Clear saved progress** deliberately resets your progress.

The updater keeps the previous executable beside the current one as `Archeology.exe.previous`. If an update cannot finish, it reports the error and attempts to restore the previous build. You can also download the latest executable manually. For an unwritable installation folder, move the game into a folder you own.
