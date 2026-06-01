---
title: Enable Notifications in Ghostty for Claude Code
date: 2026-06-01
tags:
  - ghostty
  - claude
  - guide
draft: false
---
# Claude Code + Ghostty Notifications

## Context

I want Claude Code to notify me whenever it needs input, permission approval, or attention during long-running tasks.

I like [cmux](https://cmux.com/), but I find them too unreliable for daily use due to memory leaks and various bugs.

## Enable Notifications in Ghostty

Add the following to your Ghostty config file:

```ini
# ~/.config/ghostty/config
desktop-notifications = true
```

Reload Ghostty or restart the application after updating the config.

Also ensure notifications are enabled in macOS:

**System Settings → Notifications → Ghostty → Allow Notifications**

## Test Ghostty Notifications

Test OSC 9 notifications:

```bash
sleep 3; printf '\e]9;Ghostty test notification\a'
```

Test OSC 777 notifications:

```bash
sleep 3; printf '\e]777;notify;Ghostty Test;OSC 777 notification\a'
```

For reliable testing, switch focus to another application while the command is waiting.

## Configure Claude Code

Open Claude Code and run:

```text
/config
```

Navigate to `Notifications` and choose `auto`.

`auto` is currently the safest option, works well for me.
