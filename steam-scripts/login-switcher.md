---
description: Steam Login Switcher
---

# Login Switcher

Save the file as a .bat file

Change the USERNAME to your "Steam Username"\
\
This script allows you to change from one account to another very quickly if you use a lot of steam accounts.

Please make sure you set up MFA for each account to unauthorised accesses from other users

Moreover, your password is stored on the machine so is at a slight risk so ensure your AV is up to date\


```batch
// @echo off
taskkill /F /IM csgo.exe taskkill /F /IM GameOverlayUI.exe taskkill /F /IM Steam.exe
timeout /t 2 start "" "D:\Steam Master Files\Steam.exe" -login USERNAME PASSWORD
exit

```
