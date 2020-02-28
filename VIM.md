# Vim cheat sheet

A list of simple but more obscure commands for vim

## Terminal
* `:bo 15sp +term`: Open default shell buffer in a 15 line split window
* `<C-\><C-n>`: Exit insert mode for a specific terminal window

## Cut/copy/paste
* `:"*yiw`: Yank inner word to global clipboard register
* `:<C-r>0`: Paste contents of yank register in insert mode

## Mnemonics
A list of general mnemonics for vim key bindings

### Screen movement
* `<C-u>`: Up (Up half-screen)
* `<C-d>`: Down (Down half-screen)
* `<C-b>`: Back (Back full-screen)
* `<C-f>`: Forward (Forward full-screen)
* `<C-y>`: Yester-line (Reveal line above, next to up)
* `<C-e>`: Extra-line (Reveal line below, next to down)

### Cursor movement
* `<C-i>`: In (Move cursor forward in time)
* `<C-o>`: Out (Move cursor forward back time)
* `H`: High
* `M`: Middle
* `L`: Low

### Buffers
* `:bo`: Buffer open
* `:bd`: Buffer delete
* `:bp`: Buffer previous
* `:bn`: Buffer next
* `:sp`: Split window (Current buffer in new horizontal split window)
* `:vsp`: Buffer next (Current buffer in new vertical split window)
