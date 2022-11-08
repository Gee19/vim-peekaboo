vim-peekaboo
============

![](https://cloud.githubusercontent.com/assets/700826/6095261/bb00340c-af96-11e4-9df5-9cd869673a11.gif)

Peekaboo extends `"` and `@` in normal mode and `<CTRL-R>` in insert mode so
you can see the contents of the registers.

Installation
------------

Using [vim-plug](https://github.com/junegunn/vim-plug):

```vim
Plug 'Gee19/vim-peekaboo'
```

Usage
-----

Peekaboo will show you the contents of the registers on the sidebar when you
hit `"` or `@` in normal mode or `<CTRL-R>` in insert mode. The sidebar is
automatically closed on subsequent key strokes.

You can toggle fullscreen mode by pressing spacebar.

Customization
-------------

| Config                  | Default                 | Description                                       |
| ------                  | -------                 | -----------                                       |
| `g:peekaboo_window`     | `vert bo 30new`         | Command for creating Peekaboo window              |
| `g:peekaboo_delay`      | 0 (ms)                  | Delay opening of Peekaboo window                  |
| `g:peekaboo_compact`    | 0 (boolean)             | Compact display                                   |
| `g:peekaboo_prefix`     | Empty (string)          | Prefix for key mapping (e.g. `<leader>`)          |
| `g:peekaboo_ins_prefix` | Empty (string)          | Prefix for insert mode key mapping (e.g. `<c-x>`) |
| `g:peekaboo_special`    | '"', '*', '+', '-'      | Special registers to be listed                    |
| `g:peekaboo_readonly`   | '.', '%', '#', '/', ':' | Read-only registers to be listed                  |

Differences from HEAD
-------
- Add `float` option to `g:peekaboo_window` (borrowed from #68)
- Add vim help docs & optional special or read-only registers ([Konfekt](https://github.com/Konfekt))
- Fix foldcolumn (#77)
- Fix conflict with lesspace
- Fix cmdline resize bug, special thanks to chemzqm for the help (#74 and #83)

Working on
-------
- Add vim8 popup window support
- Float changes don't respect compact boolean
- Fix conflict with repeat/dot command ([mg979](https://github.com/mg979)) (seems to break macros, disabled for now)

License
-------

MIT
