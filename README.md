# manual-open.yazi

A [Yazi](https://yazi-rs.github.io/) plugin that lets you manually type a command to open selected file(s), similar to "Open with..." in GUI file managers.

## Install

```bash
ya pack -a Xiaolanshu/manual-open
```

Or clone manually into your Yazi plugins directory:

```bash
git clone https://github.com/Xiaolanshu/manual-open.yazi ~/.config/yazi/plugins/manual-open.yazi
```

## Usage

Add a keybinding in `~/.config/yazi/keymap.toml`:

```toml
[manager]
prepend_keymap = [
    { on = ["R"], run = "plugin manual-open", desc = "Open with..." },
]
```

Press the bound key, type a command (e.g. `nvim`, `mpv`, `code`), and the selected file(s) will be passed as arguments.

- If files are selected, all selected files are passed.
- If no files are selected, the currently hovered file is used.

## License

MIT
