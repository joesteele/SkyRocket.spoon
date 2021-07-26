# 🌄 🚀 SkyRocket.spoon

This Hammerspoon tool lets you **resize** and **move** windows by clicking + dragging them while holding down modifier keys.

This attempts to emulate such things as:

* BetterTouchTool resize/move functions
* Coderage Software's abandoned Zooom/2 software
* Linux desktop move/resize hot keys

<img alt="SkyRocket move and resize demo" src="https://github.com/dbalatero/SkyRocket.spoon/raw/master/doc/demo.gif" />

## Installation

The easiest thing to do is paste this in:

```
mkdir -p ~/.hammerspoon/Spoons
git clone https://github.com/dbalatero/SkyRocket.spoon.git ~/.hammerspoon/Spoons/SkyRocket.spoon
```

## Usage

Once you've installed it, add this to your `~/.hammerspoon/init.lua` file:

```lua
local SkyRocket = hs.loadSpoon("SkyRocket")

sky = SkyRocket:new({
  -- Which modifiers to hold to move a window?
  moveModifiers = {'cmd', 'shift'},

  -- Which modifiers to hold to resize a window?
  resizeModifiers = {'ctrl', 'shift'},
})
```

### Moving

To move a window, hold your `moveModifiers` down, then click and drag a window.

### Resizing

To resize a window, hold your `resizeModifiers` down, then click and drag a window.

### Thanks

I took initial inspiration from [this gist](https://gist.github.com/kizzx2/e542fa74b80b7563045a) by @kizzx2, and heavily modified it to be packaged up in this Spoon. I also came up with a different technique for resizing to address the low frame-rate when attempting to resize in real time.
