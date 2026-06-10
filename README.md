# Corbin's dmenu

Based on vanilla [suckless dmenu](https://git.suckless.org/dmenu) (master), with my customizations in a single commit on top. Feature set inspired by LukeSmithxyz/dmenu.

Extra stuff added to vanilla dmenu:

- reads Xresources (`dmenu.font`, `dmenu.color0`, `dmenu.color4` - ergo pywal compatible)
- alpha patch, which importantly allows this build to be embedded in transparent st
- can view color characters like emoji
- `-c` to center dmenu on screen (min width set in config.h)
- `-P` for password mode: hide user input
- `-r` to reject non-matching input
- dmenu options are mouse clickable

Note: `config.h` is tracked directly; there is no `config.def.h`.

## Installation

After making any config changes that you want, just `make`, `sudo make install` it.

## Updating against upstream

```sh
git fetch upstream
git rebase upstream/master
make && sudo make install
```
