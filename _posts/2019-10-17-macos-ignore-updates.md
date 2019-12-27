---
layout: default
date: 2019-10-17
title: Ignore macOS Software Updates
---

To suppress software updates in MacOS, we can use `softwareupdate`. For instance, to list updates, and then suppress Catalina and Safari 13 updates, do

$ sudo softwareupdate --list

$ sudo softwareupdate --ignore Safari13.0.4MojaveAuto

$ sudo softwareupdate --ignore "macOS Catalina"

We can reset the block using

$ sudo softwareupdate --reset-ignored

Screenshot:

![](https://cheleb.net/public/images/macos_ignore_updates.png)

Sources:

- [https://www.jamf.com/jamf-nation/discussions/33505/ignore-catalina-upgrade-prompt-in-software-update](https://www.jamf.com/jamf-nation/discussions/33505/ignore-catalina-upgrade-prompt-in-software-update)
- [https://discussions.apple.com/thread/250705858](https://discussions.apple.com/thread/250705858)
