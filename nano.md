# Nano Cheatsheet

### File Operations

Command | Explanation
---|---
`nano <filename>` | Opens or creates the specified file.
`Ctrl+O` | Write Out (Saves) the current file to disk.
`Ctrl+X` | Exit Nano. (If unsaved, it will prompt to save first.)
`Ctrl+R` | Read File (Inserts) the content of another file into the current buffer.

### Search and Navigation

Command | Explanation
---|---
`Ctrl+W` | Where is (Searches) for text or a regular expression.
`Ctrl+F` | Moves forward one page (equivalent to Page Down).
`Ctrl+B` | Moves backward one page (equivalent to Page Up).
`Ctrl+A` | Moves to the beginning of the current line.
`Ctrl+E` | Moves to the end of the current line.
`Ctrl+C` | Displays the current cursor position (line, column, character offset).
`Ctrl+_` | Go To Line number (enter the number after pressing the command).

### Editing and Clipboard

Command | Explanation
---|---
`Alt+A` | Start/Stop Mark (Sets an anchor to begin text selection).
`Ctrl+K` | Cut the entire current line and stores it in the cut buffer.
`Ctrl+U` | Uncut (Pastes) the contents of the cut buffer at the cursor.
`Ctrl+D` | Deletes the character under the cursor (equivalent to the Delete key).
`Alt+6` | Copy the current line (stores it without cutting). (Alt+6)
`Ctrl+T` | Spell check the document.

### Find and Replace

Command | Explanation
---|---
`Ctrl+W` then `Ctrl+R` | Activates the Replace function (search, then prompt for replacement text).
`Alt+R` | Toggles the setting for Regular Expression Search after starting a search with `Ctrl+W`. (Alt+R)

### View and Helper Commands

Command | Explanation
---|---
`Ctrl+G` | Displays the Help screen with a list of all commands.
`Ctrl+L` | Redraws the current screen.
`Alt+U` | Undo the last operation (if available). (Alt+U)
`Alt+E` | Redo the last undone operation (if available). (Alt+E)
`Alt+A` | Toggles Smart Home key movement (beginning of non-blank text). (Alt+A)

---