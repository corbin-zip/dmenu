# Corbin's dmenu

Based on vanilla [suckless dmenu](https://git.suckless.org/dmenu) (upstream). Customizations were folded into a single commit when the fork was cleaned up against vanilla; newer work is to land as normal commits on top, and upstream changes are merged as they come in. Feature set inspired by & originally forked from LukeSmithxyz/dmenu.

Extra stuff added to vanilla dmenu:

- reads Xresources (`dmenu.font`, `dmenu.color0`, `dmenu.color4` - ergo pywal compatible)
- alpha patch, which importantly allows this build to be embedded in transparent st
- can view color characters like emoji
- `-c` to center dmenu on screen (min width set in config.h)
- `-P` for password mode: hide user input
- `-r` to reject non-matching input
- `-of` / `-ob` for outline colors on multi-selection
- dmenu options are mouse clickable

Note: `config.h` is tracked directly; there is no `config.def.h`.

## Installation

After making any config changes that you want, just `make`, `sudo make install` it.

## Updating against upstream

```sh
git fetch upstream
git merge upstream/master
make && sudo make install
```
