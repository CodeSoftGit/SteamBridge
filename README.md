# SteamBridge
No more annoying Oculus dash. Transform your Quest device into an almost-native SteamVR headset!

## Disclaimer
You will no longer be able to play Oculus games, unless you install Revive for SteamVR.

## Installation
- Open Task Manager, go to Services and look for OVRService, right click on it and stop it. (If you want to get this done easier, there is a script that you can run in [releases](https://https://github.com/codesoft/SteamBridge/releases/))
- Go to *C:\Program Files\Oculus\Support\oculus-dash\dash\bin* in Explorer.
- Rename the original OculusDash.exe to OculusDash.exe.bak and move the replacement OculusDash.exe into the folder you just opened in Explorer.
- Go back to Task Manager, look for OVRService again, right click on it and start it.

---
## Common fixes
Here is a list of common issues and their respective fixes/workarounds!

## Headset Infinitely Loads (SteamVR doesn't launch)
This issue can occur when you do not have "File name extensions" enabled when renaming OculusDash.exe. To fix this:

- Open "File Explorer"
- Click the "View" tab (at the top)
- Enable "File name extensions"
- Follow the installation instructions

You can verify that you installed it succesfully if "OculusDash.exe.bak" is the "BAK File" type. And looks like the below screenshot.

## OpenXR Games launch, but do not appear in VR
This is a very common issue, and has to do with OpenXR prefering the use of Oculus over SteamVR. The fix is very simple:

- Open SteamVR settings (with headset connected)
- Press "Show" under "Advanced Settings"
- Open the "Developer" tab
- Click "Set SteamVR as OpenXR runtine"

<img src="https://service.viveport.com/hc/article_attachments/4423262818317/___2022-01-28___3.09.45.png" width="426" height="328" />

Source: [Viveport](https://service.viveport.com/hc/en-us/articles/4423262844813-How-to-setup-correct-OpenXR-runtime)

## Non-OpenXR Games launch, do not appear in VR
This is another very common issue, some games manually check for Oculus instead of following your preferences. A workaround can be found by using [OVR Advanced Settings](https://store.steampowered.com/app/1009850/OVR_Advanced_Settings/).

DISCLAIMER: This workaround may prevent some SteamVR games from launching, make sure to undo this fix if you are having trouble launching games.

- Install [OVR Advanced Settings](https://store.steampowered.com/app/1009850/OVR_Advanced_Settings/) and launch it.
- Open the new overlay (found next to the desktop button)
- Open the overlay settings (bottom left)
- Turn on "Autostart"
- Turn on "Force Use SteamVR (Disable Oculus API [expiremental])"
