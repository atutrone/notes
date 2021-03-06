# Vim
If a file is read-only and can't be changed, use `sudo vim file` to open it as root.  

## Modes
`ESC` - Normal (Commands)  
`i` - Insert (Editing)  
`v` - Visual (Like Normal, but with selection)  
`:` - Commands.  

## General
`.` - Repeat previous command.  
`u` - UNDO.  
`CTRL` + `r` - REDO.  
`c` + `movement` - Change up to movement.  

# Inside
`command` + `i` + `character` - Do a command inside characters.  

`vi"` - Select everything inside "".  
`xi(` - Delete everything inside ().
`ci{` - Change (Delete and enter insert mode) inside {}.  

## Tabs
`:tabe FILEPATH` - Open file in new tab  
`:tabn` - Next tab  
`:tabp` - Previous tab

## Copy & Paste
Enter **visual mode** and select text.  

`y` - Copy (yank) selected.  
`d` - Cut selected.  
`p` - Paste after cursor.  

`x` - Delete selected.  

These can be combined with movements. Ex. `x2e` is delete next 2 words.  

`yy` - Copy (yank) line in **normal** mode.  
`dd` - Cut line in **normal** mode.  

## Save & Exit
`:w` - Save  
`:q` - Quit  
`:wq` - Save & Quit  
`:q!` - Cancel & Quit  

## Moving
All of these can be used in **visual** mode for selection.  

`j` - Down  
`k` - Up  
`h` - Left  
`l` - Right  

`w` - Forward one word.  
`b` - Back one word.  
`e` - End of word.  

Adding a number before one of these, will repeat the command n times. Ex. `3h` will go up 3 lines.  

`0` - Beginning of line.  
`$` - End of line.  

`%` - Jump to matching tag i.e. `)`, `}`, `]`.  

`f` + `character` - Jump **to** next character.  
`t` + `character` - Jump **before** next character.  

`*` - Next occurrence of word under cursor.  
`#` - Previous occurrence of word under cursor.  

`gg` - Beginning of file.  
`G` - End of file.  
`nG` - Jump to line n.  

## Search
`/` + `string` + `Enter` = Search for string **forwards**.  
`?` + `string` + `Enter` = Search for string **backwards**.    
`n` - Next occurrence.  
`N` - Previous occurrence.  

## Replace
`:%s/text/replacement/g` - Replace text on every line.  
`:s/text/replacement/g` - Replace text on current line.  

## Insert
`o` - Create new line **under** cursor and enter **INS** mode.  
`O` - Create new line **above** cursor and enter **INS** mode.  

`x` - Delete character.  
`X` - Backspace.  

`r` + `new character` - Change character under cursor without INS mode.  

## Multiple Inserts
`n times` + `i` + `string` + `ESC` = Multiple inserts.  

Ex. `5ifoo` + `ESC` will result in `foofoofoofoofoo`.

### Editor
`:set number` - Show line numbers.  
