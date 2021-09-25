# Dash.nvim

Query [Dash.app](https://kapeli.com/dash) within Neovim with a Telescope picker!

![demo](./images/demo.gif)

Note: Dash is a Mac-only app, so you'll only find this plugin useful on Mac.

## Usage

Show the picker with `:Dash` or `require('dash').search()`

## Install

Using Packer:

```lua
use({ 'mrjones2014/dash.nvim', requires = { 'nvim-telescope/telescope.nvim', 'nvim-lua/plenary.nvim' }, rocks = { 'xml2lua' } })
```

## Configuration

If Dash.app is installed somewhere other than `/Applications/Dash.app`, you can specify the path to use
by calling the `setup` function. Note that `~` will not be expanded, so you should use `os.getenv('HOME')`
to specify your home directory. For example:

```lua
require('dash').setup({ dashAppPath = (os.getenv('HOME') .. '/Applications/Dash.app') })
```
