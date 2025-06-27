---
title: "Bypassing JavaScript Focus Detection in the Browser"
date: 2025-06-27T09:00:00+07:00
draft: false
tags: ["javascript", "english", "guide"]
---

# How to Stop Videos from Pausing When You Switch Tabs

Some sites pause videos if you switch tabs or lose focus. Here's a quick script to bypass that behavior.

## Paste This in the Console

```js
Object.defineProperty(document, 'hidden', { value: false, configurable: true });
Object.defineProperty(document, 'visibilityState', { value: 'visible', configurable: true });
document.hasFocus = () => true;

window.onblur = null;
window.onfocus = null;
document.onvisibilitychange = null;

const blockEvents = ['visibilitychange', 'blur', 'focus'];
const origAddEventListener = EventTarget.prototype.addEventListener;
EventTarget.prototype.addEventListener = function(type, listener, options) {
    if (!blockEvents.includes(type)) {
        return origAddEventListener.call(this, type, listener, options);
    }
};
```

This works for Vanta security awareness training. If my employer sees this, I pinky swear that I watched the whole thing and only tested the script for fun!
