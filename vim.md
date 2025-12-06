# Vim Cheatsheet

### Mode Switching

Command | Explanation
---|---
`i` | Enters Insert Mode before the cursor (to type text).
`a` | Enters Insert Mode after the cursor.
`o` | Enters Insert Mode on a new line below the current one.
`O` | Enters Insert Mode on a new line above the current one.
`v` | Enters Visual Mode (character-wise selection).
`V` | Enters Visual Line Mode (selects entire lines).
`Ctrl + v` | Enters Visual Block Mode (rectangular selection).
`Esc` | Exits any mode back to Normal Mode (the default mode).

### Navigation (Normal Mode)

Command | Explanation
---|---
`h` | Moves the cursor left.
`j` | Moves the cursor down.
`k` | Moves the cursor up.
`l` | Moves the cursor right.
`w` | Moves to the start of the next word.
`b` | Moves to the start of the previous word.
`e` | Moves to the end of the current word.
`0`  | Moves to the start of the line.
`$` | Moves to the end of the line.
`^` | Moves to the first non-blank character of the line.
`gg` | Moves to the first line of the file.
`G` | Moves to the last line of the file.
`:<num>` | Jumps to the specified line number (e.g., `:50`).
`%` | Jumps to the matching parenthesis, bracket, or brace.

### Editing / Deletion (Normal Mode)

Command | Explanation
---|---
`x` | Deletes the character under the cursor.
`dw` | Deletes from the cursor to the end of the word.
`dd` | Deletes the entire current line.
`d$` | Deletes from the cursor to the end of the line.
`D` | Shortcut for `d$` (Deletes to the end of the line).
`2dd` | Deletes two lines (can prefix any number).
`r<char>` | Replaces the character under the cursor with `<char>`.
`s` | Deletes the character under the cursor and enters Insert Mode.
`cc` | Deletes the current line's content and enters Insert Mode (replaces the line).
`c$` | Deletes to the end of the line and enters Insert Mode.
`cw` | Deletes to the end of the word and enters Insert Mode.
`J` | Joins the current line with the one below it.

### Copy / Paste / Undo (Normal Mode)

Command | Explanation
---|---
`yy` / `Y` | Yanks (copies) the entire current line.
`yw` | Yanks (copies) from the cursor to the end of the word.
`p` | Puts (pastes) after the cursor or on the line below.
`P` | Puts (pastes) before the cursor or on the line above.
`u` | Undoes the last change.
`Ctrl + r` | Redoes the last undone change.

### Search and Replace

Command | Explanation
---|---
`/ <pattern>` | Searches forward for `<pattern>`.
`? <pattern>` | Searches backward for `<pattern>`.
`n` | Moves to the next search result.
`N` | Moves to the previous search result.
`*` | Searches for the word under the cursor (forward).
`:s/old/new/g` | Substitutes the first occurrence of `old` with `new` on the current line.
`:%s/old/new/g` | Substitutes all occurrences of `old` with `new` throughout the file (`%` means all lines, `g` means all occurrences on each line).

### Saving and Exiting (Command Mode: `:`)

Command | Explanation
---|---
`:w` | Writes (saves) the file.
`:w <filename>` | Saves the file with a new name.
`:q` | Quits the file (only if no changes have been made).
`:wq` | Writes and quits (saves and exits).
`:x` | Equivalent to `:wq`.
`:q!` | Quits without saving (discards changes).
`:wqa` | Writes and quits all open files/windows.

### File and Window Operations

Command | Explanation
---|---
`:e <filename>` | Opens a new file in the current window.
`:sp <filename>` | Splits the window horizontally and opens `<filename>`.
`:vsp <filename>` | Splits the window vertically and opens `<filename>`.
`Ctrl + w` then `w` | Switches between split windows.

---