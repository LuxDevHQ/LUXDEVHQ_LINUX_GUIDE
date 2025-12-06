# Essential Nano & Vim Commands for Total Beginners (Linux & Server Editing)

When working on **Linux** or connecting to a **remote server**, you often need to **open and edit files directly in the terminal**. This includes tasks like updating configuration files, fixing environment variables, editing server settings, or quickly changing code.

Linux provides two main terminal-based text editors: **nano** (easy) and **vim** (powerful). This cheat sheet explains both in a beginner‑friendly way.

---

#  1. Nano — The Easiest Text Editor for Beginners

Nano is simple, readable, and perfect for anyone new.

## Open or create a file
```bash
nano filename.txt
```

##  Nano Basics
| Action | Keys | Explanation |
|--------|------|-------------|
| Save file | CTRL + O | Writes your changes |
| Exit nano | CTRL + X | Asks to save if needed |
| Cut line | CTRL + K | Removes whole line |
| Paste line | CTRL + U | Pastes last cut |
| Search | CTRL + W | Find words |
| Go to line | CTRL + _ | Navigate fast |
| Undo | ALT + U | Undo changes |
| Redo | ALT + E | Redo undone changes |

---

#  2. Vim — More Powerful & Common on Servers

Vim is harder at first because it uses *modes*, but it's extremely fast once learned.

---

#  Vim Modes Explained

| Mode | Purpose |
|------|----------|
| **Normal** | Move around & issue commands |
| **Insert** | Type text normally |
| **Visual** | Select text |

---

#  Open Vim
```bash
vim filename.txt
```

---

#  Switching Modes
| Action | Key |
|--------|------|
| Enter insert mode | `i` |
| Insert at end of line | `A` |
| New line below | `o` |
| Back to normal mode | `ESC` |

---

# Saving & Exiting
| Action | Command |
|--------|----------|
| Save | `:w` |
| Quit | `:q` |
| Save & quit | `:wq` or `ZZ` |
| Quit without saving | `:q!` |

---

#  Navigation
| Action | Key |
|--------|------|
| Move left/down/up/right | `h j k l` |
| Start of line | `0` |
| End of line | `$` |
| Top of file | `gg` |
| Bottom of file | `G` |

---

#  Editing in Vim
| Action | Command |
|--------|----------|
| Delete character | `x` |
| Delete line | `dd` |
| Copy line | `yy` |
| Paste | `p` |
| Undo | `u` |
| Redo | `CTRL + r` |

---

#  Searching in Vim
| Action | Command |
|--------|----------|
| Search | `/word` |
| Next match | `n` |
| Previous match | `N` |

---

#  Which Should a Beginner Use?

###  Use **nano** for:
- Simple tasks  
- Editing configs  
- Avoiding complex shortcuts  

### Use **vim** for:
- Remote servers where nano isn’t installed  
- Advanced editing  
- Speed and power  

---

Enjoy editing confidently on Linux and servers!
