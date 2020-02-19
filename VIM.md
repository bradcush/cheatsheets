# Vim cheat sheet

A list of simple but more obscure commands for vim

## Terminal
* `:bo 15sp +term`: Open default shell buffer in a 15 line split window
* `<C-\><C-n>`: Exit insert mode for a specific terminal window

## Cut/copy/paste
* `:"*yiw`: Yank inner word to global clipboard register
* `:<C-r>0`: Paste contents of yank register in insert mode
