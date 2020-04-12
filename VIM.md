# Vim cheat sheet

Fundamental principles, less common commands, and compound commands


## Fundamental principles
Core ideas important to understanding and using vim

### Modes
Vim is what's called a modal editor, containing many different modes
of editing where each command means something different in a given mode.

#### Normal mode
#### Insert mode
#### Visual mode
#### Visual line mode
#### Visual block mode
#### Command mode
#### Replace mode

### Speaking vim (Mnemonics)
The possibilities become exponential and obvious by combining
the concepts of built-in nouns, verbs, and modifiers.

#### Nouns
* `w`: Word
* `s`: Sentence
* `p`: Paragraph
* `b`: Block (Parenthesis)
* `B`: Big block or bracket block (Brackets)
* `t`: Tag (eg. HTML/XML)
* `(`: Parenthesis block
* `{`: Bracket block
* `'`/`"`: Quote

#### Verbs
* `v`: Visual
* `c`: Change
* `d`: Delete
* `y`: Yank (Copy)
* `r`: Replace
* `x`: Cut

#### Modifiers
* `i`: Inner
* `a`: Around (An object)

### Buffers, windows, and tab pages
Working with files in vim is slightly different that what you're used
to with your traditional editor. Buffers are the way you interact with
files and so the relationship between buffers, windows, and tab pages
is a fundamental idea one needs to understand.

#### Tab pages > windows > buffers
Tab pages can contains many windows, which can contain many buffers,
that can be open or closed, visible in a given window or hidden altogether.

### Registers, macros, and marks
Copy/paste, replaying compound actions, and marking locations

#### Registers
* `*`: Global clipboard register for unix systems (Alias `+`)
(Can depend on your specific system such as MacOS or Linux)
* `[1-9]`: History registers
* `[a-z]`: Named registers
* `[A-Z]`: Named appending registers
* `0`: Default yank register
* `"`: Last yank/cut text
* `/`: Last search pattern
* `-`: Small delete register (eg. `daw`)
* `_`: Black hole register
* `=`: Expression register

##### Read-only registers
* `:`: Last entered command
* `.`: Last inserted text
* `%`: Current filename register
* `#`: Alternate filename register (Last file edited)

#### Macros
#### Marks

## Simple commands
Simple but less commonly used commands or those in which have a
more creative mnemonic to remember it's purpose.

### Screen movement
* `<C-y>`: Yester-line (Reveal line above, next to up)
* `<C-e>`: Extra-line (Reveal line below, next to down)

### Cursor movement
* `<C-i>`: In (Move cursor forward in time)
* `<C-o>`: Out (Move cursor forward back time)

### History
* `g;`: Go (To older entry in change list)
* `g,`: Go (To newer entry in change list)

### Buffers
* `:b`: Buffer (Alias `:buffer`)
* `:bp`: Buffer previous (Alias `:bprev`)
* `:ls`: List (Open buffers) (Alias `:buffers`)

### netrw
* `i`: Toggle between file system views
* `gn`: Make directory under current position current

### Miscellaneous
* `:bo`: Bottom right (Anchors split windows commands)
* `<leader>`: Used for personalized shortcut commands
(By default mapped to `\` but often remapped to `<Space>`)


## Compound commands
Examples of useful but more complex commands

### Terminal
* `:bo 15sp +term`: Open default shell in a 15 line split window
* `<C-\><C-n>`: Exit insert mode for a specific terminal window

### Cut/copy/paste
* `:"*yiw`: Yank inner word to global clipboard register
* `<C-r>0`: Paste contents of yank register in insert mode

### Pattern matching
* `:%s/match/replacement/gc`: Replace match with replacement globally confirming each
* `:vimgrep /pattern/ **/*`: Search current pattern across all files
(Also see `:grep` for use of external grep inside of vim)
(If you're using fugitive then `:Ggrep` can be the most useful)

### Miscellaneous
* `:b0 | vsplit` (Open a buffer 0 in a split window)
(`|` in vim is used to run multiple commands consecutively if the previous succeeds)
