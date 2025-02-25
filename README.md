# jyba

A neovim plugin that allows to easily set up commands to run on save;

The goal of jyba is to help you to set commands to run o save by project, making it possible for you to quickly get ready for new projects you are working on, without having to make a whole new configuration to your neovim.
Make sure plenary.nvim is installed in your environment, jyba depends on it.

# Installation

Installation using lazy.nvim:

```lua
{
    "ivansantiagojr/jyba",
    dependencies = "nvim-lua/plenary.nvim",
}
```

# Usage

On your config files setup a keymap, like:

```lua
local jyba = require("jyba")


vim.keymap.set("n", "<C-m>", jyba.toggle_window)
```

Full example:

```lua
{
    "ivansantiagojr/jyba",
    dependencies = "nvim-lua/plenary.nvim",
    config = function()
        local jyba = require("jyba")
        vim.keymap.set("n", "<C-m>", jyba.toggle_window)
    end
}
```

Then:

- open the popup window with the keymap you chose (In the configuration above it is `CTRL + M`);
- enter insert mode;
- write the commands you want to run on save. Make sure to add one per line;
- after that, go back to normal mode and press the keymap to toggle the popup again.

When you toggle the window to close, your commands you already be saved.

Now, just save your buffer, and the commands you set will be executed.

# Feel free to contribute!

I recognize this plugin could use some improvements, you are welcome to suggest and/or implement them!

**TODOS**:

- add printscreens to usage steps and to commands running (maybe a short video of the flow).
