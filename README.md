# vim-hexhl

This plugin provides commands to highlight all Hex colors and CSS named colors
in the current buffer.

## Install

Use the plugin manager of your choice or if running Vim 8+:

```sh
mkdir -p ~/.vim/pack/plugins/start
git clone https://github.com/rasch/vim-hexhl.git ~/.vim/pack/plugins/start/hexhl
vim "+helptags ALL" +qall!
```

## Usage

Highlight the colors.

```vim
:HexHl
```

Clear the highlights.

```vim
:HexHlClear
```

An example autocmd to enable Hex/CSS color highlighting.

```vim
augroup hexhl
  autocmd!
  autocmd BufWinEnter,Syntax,ColorScheme * HexHl
  autocmd TextChanged,TextChangedI * HexHlUpdate
augroup END
```

See the [reference manual](doc/hexhl.txt) by running `:help hexhl.txt`.

## License

Distributed under the same terms as Vim itself. See `:help license`.
